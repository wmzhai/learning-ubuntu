# ssh配置

SSH服务器，可以通过SSH协议来访问远程服务器，代替telnet和ftp。
但是ubuntu默认是不启用root用户也不允许root远程登录的。
所以需要先启用root用户

## 启用root用户

```
sudo passwd root      //修改密码后就启用了。
```
 
## 安装配置OpenSSH server
```
$ sudo apt-get install openssh-server
$ sudo vi /etc/ssh/sshd_config
```

找到PermitRootLogin no一行，改为PermitRootLogin yes,

重启 openssh server
```
$ sudo service ssh restart
```

然后尝试密码登录
```
ssh root@ip
```

## 添加公钥 

如果是mac，需要安装`ssh-copy-id`
```
brew install ssh-copy-id
```

然后就可以用ssh key登录了
```
ssh root@ip
```






 
