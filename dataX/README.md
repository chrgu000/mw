# 阿里DataX



## DataX简介

* [网址](https://www.imooc.com/article/15640)



## 安装部署

* ##### [DataX下载地址](http://datax-opensource.oss-cn-hangzhou.aliyuncs.com/datax.tar.gz)

* 安装python2.7.5

* 验证服务

  ```shell
  # 在C:\app\datax\bin下执行
  $ python datax.py ../job/job.json
  ```

* [参考网址](https://blog.csdn.net/baidu_30851231/article/details/79863779)



## CMD编码设置

1. 运行CMD；

2. 输入 CHCP，回车查看当前的编码；

3. 输入CHCP 65001，回车；



## 配置文件

> 使用如下命令查看我们具体需要的配置文件样例
> python datax.py -r {YOUR_READER} -w {YOUR_WRITER}

```json
# 我现在需要的是从sqlserver读入，写到mysql
$ python datax.py -r mysqlreader -w mysqlwriter
# 输出如下
{
    "job": {
        "content": [
            {
                "reader": {
                    "name": "mysqlreader",
                    "parameter": {
                        "column": [],
                        "connection": [
                            {
                                "jdbcUrl": [],
                                "table": []
                            }
                        ],
                        "password": "",
                        "username": "",
                        "where": ""
                    }
                },
                "writer": {
                    "name": "mysqlwriter",
                    "parameter": {
                        "column": [],
                        "connection": [
                            {
                                "jdbcUrl": "",
                                "table": []
                            }
                        ],
                        "password": "",
                        "preSql": [],
                        "session": [],
                        "username": "",
                        "writeMode": ""
                    }
                }
            }
        ],
        "setting": {
            "speed": {
                "channel": ""
            }
        }
    }
}
```



#### 配置字段

```json
# 必选字段
"jdbcUrl":["jdbc:mysql://127.0.0.1:3306/datax?characterEncoding=utf8"]
"username":"root"
"password":"123"
"table":"tablename"
"column":["id", "name"]
"writeMode":"insert/replace/update"	
```



#### mysqlWriter针对Mysql类型转换列表

| DataX 内部类型 | Mysql 数据类型                                       |
| -------------- | ---------------------------------------------------- |
| Long           | int, tinyint, smallint, mediumint, int, bigint, year |
| Double         | float, double, decimal                               |
| String         | varchar, char, tinytext, text, mediumtext, longtext  |
| Date           | date, datetime, timestamp, time                      |
| Boolean        | bit, bool                                            |
| Bytes          | tinyblob, mediumblob, blob, longblob, varbinary      |

