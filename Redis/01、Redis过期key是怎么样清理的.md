# Redis 过期的key 是怎么清理的

### 惰性清除

在访问key 时 ，如果发现key 已经过期 那么会将key删除

### 定时清理
Redis配置项hz定义了serverCron任务的执行周期，默认每次清理时间为25ms，每次清理会依次遍历所有DB，从db随机取出20个key，如果过期就删除，如果其中有5个key过期，那么就继续对这个db进行清理，否则开始清理下一个db。

### 内存不够时清理

当执行写入命令时，如果发现内存不够，那么就会按照配置的淘汰策略清理内存，淘汰策略一般有6种，Redis4.0版本后又增加了2种，主要由分为三类

第一类 不处理，等报错(默认的配置)

noeviction，发现内存不够时，不删除key，执行写入命令时直接返回错误信息。（Redis默认的配置就是noeviction）
第二类 从所有结果集中的key中挑选，进行淘汰

allkeys-random 就是从所有的key中随机挑选key，进行淘汰
allkeys-lru 就是从所有的key中挑选最近使用时间距离现在最远的key，进行淘汰
allkeys-lfu 就是从所有的key中挑选使用频率最低的key，进行淘汰。（这是Redis 4.0版本后新增的策略）
第三类 从设置了过期时间的key中挑选，进行淘汰

这种就是从设置了expires过期时间的结果集中选出一部分key淘汰，挑选的算法有：

volatile-random 从设置了过期时间的结果集中随机挑选key删除。

volatile-lru 从设置了过期时间的结果集中挑选上次使用时间距离现在最久的key开始删除

volatile-ttl 从设置了过期时间的结果集中挑选可存活时间最短的key开始删除(也就是从哪些快要过期的key中先删除)

volatile-lfu 从过期时间的结果集中选择使用频率最低的key开始删除（这是Redis 4.0版本后新增的策略）
