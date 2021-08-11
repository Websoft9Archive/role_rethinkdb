## 产品化

#### 默认的管理员账号密码是什么？

账号为 admin，默认没有密码，可以通过如下两种方式初始化一个密码
```
# 先创建再启动服务
rethinkdb create --initial-password 123456 -d /data/rethinkdb
rethinkdb serve 

# 创建服务时初始化密码
rethinkdb serve --initial-password 123456 -d /data/rethinkdb
```

#### 如何重置密码？

登录web界面，在【Data explorer】下输入所需的命令清空密码
```
r.db('rethinkdb').table('users').get('admin').update({password: false})
```

#### 如何开启远程访问？
```
sudo sed -n "s/^#bind=/bind=0.0.0.0/g" /etc/rethinkdb/instances.d/instance.conf
```

#### 如何启用认证机制？

#### 29015 端口有什么用途？

#### 是否自带图形化界面？

自带web图形化界面，但无密码访问机制

#### 是否自带服务？

RethinkDB 安装完成后，在 /etc/init.d 下生成了一个 rethinkdb 的脚本， 支持 /etc/init.d/rethinkdb stop | start | restart  
另外，在Ubuntu下默认生成了基于上面脚本的服务。  

但官方也建议[Full support for systemd](https://rethinkdb.com/docs/start-on-startup/)
