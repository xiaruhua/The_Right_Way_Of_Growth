<h1 align="center">《The Right Way Of Growth》V1.10</h1>



## 备注

状态        | 含义
--------- | -------
🈳️ | 当前未开始总结
🚗 | 总结中
🧀️ | 目前仅供参考未修正和发布
✅ | 总结完毕
🔧 | 查漏补缺修改中

## 目录

- PHP
  + 基础
    * [数组处理函数](https://www.php.net/manual/zh/book.array.php)
    * [魔术方法](https://www.php.net/manual/zh/language.oop5.magic.php)
    * [预定义变量](https://www.php.net/manual/zh/reserved.variables.php)
    * [接口与抽象类的区别](https://github.com/mikouhero/The_Right_Way_Of_Growth/blob/master/PHP/%E5%9F%BA%E7%A1%80/02%E3%80%81%E6%8E%A5%E5%8F%A3%E4%B8%8E%E6%8A%BD%E8%B1%A1%E7%B1%BB.md)
    * static、self与$this的区别
    * 传值与引用
    * include、require、include_once、require_once 的区别
    * 类的静态调用与实例化调用
    * 会话管理
    
  + 进阶
    * 回调与闭包
    * PHP运行模式
        - CGI
        - Fastcgi模式
        - 模块模式
        - php-cli模式
    * GC机制
    * php.ini 配置
    * php-fpm.conf 配置
    * php与nginx的通信方式
    * php-fpm与nginx 优化
    * php 内存管理
        
  + 框架思想
    * 服务容器
    * 中间件
    * 门面（facade）
    * 控制反转与依赖注入
    * Pipeline 
    * 路由
    * ORM


- MySQL 
  + 引擎
    * InnoDB
    * MyISAM
    * Memory
    * Archive
    * Blackhole\CSV\Federated\merge\NDB
  + 事务
    * 原子性（Atomicity）
    * 一致性（Consistency）
    * 隔离性（Isolation）
      - READ UNCOMMITTED:未提交读
      - READ COMMITTED：提交读/不可重复读
      - REPEATABLE READ：可重复读(MYSQL默认事务隔离级别)
      - SERIALIZEABLE：可串行化
    * 持久性（Durability）
    * 事务并发执行的问题
    * MVCC (多版本并发控制)    
  + 索引
    * 索引的基础知识
    * 索引提高检索速度
    * 建立表结构时添加的索引
      - 主键唯一索引
      - 唯一索引
      - 普通索引
      - 联合索引
    * 覆盖索引
    * 索引下推
    * 回表
    * 最左匹配原则
    * 依据是否聚簇区分
      - 聚簇索引
      - 非聚簇索引
    * 索引底层数据结构
      - hash索引
      - b-tree索引
      - b+tree索引
      - 有序数组索引
      - 跳表
      
  + 优化器
    * IO 成本
    * 单表查询的成本
    * 多表查询的成本
    * index dive   
    
  + Explain 
    * id 
    * select_type
    * table 
    * type 
    * possible_key 
    * key 
    * rows
    * filtered   
  + 锁
    * 悲观锁与乐观锁
    * 共享锁与排他锁
    * 行锁与表锁
    * 意向锁（InnoDB特有）
    * 死锁
    * 间隙锁
    * 
    
  + log日志
    * redo log（物理日志）
    * undo log 
    * bin log
  + 分表
    * 垂直分表
    * 水平分表
    
  + MySQL常见优化方式
    * 优化的范围
        - 应用程序
        - 数据库优化
    * 优化维度
        - 硬件
        - 系统配置 
        - 数据库表结构
        - SQL 及索引
    * 优化工具
        - 数据库层面
        - 系统层面
    * 数据库优化
        - SQL 优化方向
        - 架构优化方向
        - 数据库参数优化
        - 存储引擎层
        - SQL 层
  * 存储过程
  
  * 常见问题
    * 一条SQL语句执行得很慢的原因有哪些？  
    * MySQL的Limit性能问题
    * drop、delete与truncate分别在什么场景之下使用？
    * rowid 是什么？
    * SQL 约束
    * 如何正确地显示随机消息？
    * 为什么表数据删掉一半，表文件大小不变？
    * checkpoint 是什么？
        
  + 主从配置
    
- Linux
- Nginx

- Redis 
  + 常见用途

  + Redis的基础数据结构
- 设计模式
  + 概念
  
- 数据结构 
  + 数组
  + 堆/栈
  + 树
  + 队列
  + 链表
  + 图
  + 散列表
- 算法 
  + 算法分析
    * 时间复杂度/空间复杂度/正确性/可读性/健壮性
  + 算法实战
    * 排序算法 
   
- 安全 

- 架构










