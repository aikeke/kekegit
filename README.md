#mysql
文件：数据冗余和不一致性，数据访问困难，数据孤立，完整性问题，原子性问题，并发访问异常，安全性问题

DBMS：层次模型，网状模型，关系模型（特点）

文件：
表示层：文件
逻辑层：文件系统结构为物理层：存储引擎
物理层:元数据 数据：数据块

关系模型（结构化数据模型）
E-R：实体-关系模型
对象关系模型：基于对象的数据模型
半结构化数据模型：XML（扩展标记语言）

关系：关系代数运算

SQL：结构化查询语言


70年
system R：SQL

ANSI：ansi-sql

DML：数据操作语言
	insert select delete update

DDL：数据定义语言
	create drop alter
DCL：数据控制语言
	grant revoke（权限）
RDB对象：库，表，索引，视图，用户，存储过程，存储函数，触发器，事件调度器
	约束
		域约束:数据类型约束
		外键约束：引用完整性约束
		主键约束：某字段能唯一标识此字段所属的实体，并且不允许为空
			一张表只能有一个主键
		唯一性约束：每一行的某字段都不允许出现相同值，可以为空
			一张表可以有多个
		检查性约束：


数据存储和查询
存储管理器
	权限及完整性管理器
	事务管理器
	文件管理器
	缓冲去管理器
查询管理器
	DML解释器
	DDL解释器
	查询执行引擎

单进程
	多线程
		守护线程
		应用线程
		
关系运算
投影：指输出指定属性
选择：指数出符合条件的行
自然选择：具有相同名字的属性上所有取值相同的行
笛卡儿积：（a+b）（c+d）
并：集合运算


SQL查询语句：
 SQL86，89，92，99，93，08
SQL语言的组成部分
 DDL
 DML
 完整性定义语言：DDL的一部分功能
 试图定义
 事务控制
 嵌入式SQL和动态SQL：
 授权：DCL

使用程序设计语言如何与RDBMS交互
 嵌入式SQL：
 动态SQL：程序设计语言使用函数（）或者方法与RDBMS服务器建立连接，并进行交互；通过
建立连接向sql服务器发送查询语句，并将结果保存至变量中而后进行处理；

MYSQL插件式存储引擎
5.5.8（默认）：MYISAM不支持事务适合数据查询
5.5.8后（默认）：InnoDB 适合在线事务处理

用户连接请求——连接管理器——线程管理器——用户模块——命令分发模块—

表管理器：负责创建、读取或修改表定义文件：维护表描述符高速缓存：管理表锁：
	表结构定义文件

表修改模块：表的创建删除重命名移除更新或插入之类的操作
表维护模块：检查修改备份恢复优化（整理碎片）及解析

行：定长，变长

文件中记录组织：
	堆文件组织：一条记录可以放在文件中的任何地方：
	顺序文件组织：根据“搜索码”值顺序存放
	散列文件组织：

表结构定义文件，表数据文件

表空间：

数据字典：data dictionary 
	关系的元数据：
		关系的名字
		字段名字
		字段的类型和长度
		视图
		约束

		用户名字，授权，密码
		
缓冲区管理器：
	缓存置换策略
	被钉住的块		

mysql server (mysqld,mysql)
mysql cluster(不怎么用)
mysql proxy(代理,读写分离)
mysql migration tloolkit (移植工具)
mysql embedded server (嵌入)

percona

mysql安装
专用软件包管理器包
通用二进制格式包
源代码

mysql密码修改
mysqladmin -u username -h hostname password 'new-pass' -p
mysql>set password for 'username'@'host'=password('new_psaa');
mysql>update mysql.user set password=password('new_pass') where condition;

mysql安装
源码安装mysql

























