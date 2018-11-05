# 2018/9/25 入职

企业邮箱:huang.zhenyou@puscene.com

信息系统门户管理平台:http://info-sso.mwee.cn

JIRA账号：huang.zhenyou

JIRA密码：Ss152...

工号：05304





#### VPN申请



#### 新东西：

* 华为CarbonData
* RDS	 





# 2018/9/26

####  集群资源CDH

* 读账号：readonly   passwd：Readonly
* 操作号：admin    passwd: mwee123456





#### RDBReader模式

* [RDB和AOF的流程](https://blog.csdn.net/a1007720052/article/details/79126253)



#### SparkSession不能解析

导入：spark-sql_2.11-2.2.0.jar



#### vpn账号

* 服务地址：https://vpn.9now.net:10621
* 用户名：huang.zhenyou@puscene.com
* 密码：Ss...



# 2018/9/27





# 2018/9/28

#### 堡垒机

> ssh -i id_rsa huang.zhenyou@fortress.mwbyd.cn
>
> 用户名为:huang.zhenyou
> 密码为:d279d52ee44d96e78a43
> 堡垒机使用方式见:http://wiki.mwbyd.cn/pages/viewpage.action?pageId=6334750
> 如有疑问请联系石豪,邮箱:shi.hao@puscene.com



## 2018/9/29

#### Azkaban

* 账号：azkaban 
* 密码：azkabans





## 2018/10/10

#### dataX实现hive的update





## 2018/10/11

#### 增量导涉及覆盖update的情况

* mysql的日期函数
* impala



#### 集群安全

* Kerberos 

#### 所遇问题：

1、HQL子查询别名问题

     HQL的书写，select * from (select * from table) ;
    
     执行此HQL，应该会报错：ql.Driver (SessionState.java:printError(960)) - FAILED: ParseException line 48:52 cannot recognize input near '<EOF>' '<EOF>' '<EOF>' in subquery source
    
     此时，修改HQL为select * from (select * from table) a，执行成功。
---------------------
作者：xiaoL_clo 
来源：CSDN 
原文：https://blog.csdn.net/dxl342/article/details/50896046?utm_source=copy 
版权声明：本文为博主原创文章，转载请附上博文链接！







## 2018/10/15

#### 增加分区

```
alter table my_partition_test_table if not exists add partition (p_hour='2017113003', p_city='573', p_loctype='MHA');
```



#### 删除分区

```
ALTER TABLE my_partition_test_table DROP IF EXISTS PARTITION (p_loctype='MHA');
```