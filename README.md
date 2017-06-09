Automated operational platform
====

##环境需求：
 * python >=2.5
 * mysql >5.1
 * nginx >1.2

##python模块：
 * django >=1.4.5
 * flup
 * paramiko
 * django-excel-response
 * MySQL-python

##主要功能
 * 服务器的资源统计
 * svn的在线发布(功能很简单,无法看到分支,无法选择版本号)
 * 脚本的批量执行 针对分组的脚本执行(需要先设置好分组，然后分组跟脚本绑定)

##安装部署
* 修改aopproject/settings.py 设置数据库类型，账号密码
* 运行python manage.py syncdb    进行创建数据库表结构  期间添加管理员账号
* 开启服务器:python manage.py runfcgi method=prefork host=127.0.0.1 port=9001
* 配置nginx转发到127.0.0.1:90001端口
* nginx配置文件参考：

