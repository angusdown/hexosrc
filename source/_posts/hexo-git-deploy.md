## git hook方式
### 本地
本地部署工具

`npm install hexo-deployer-git --save`

在hexo站点配置文件_config.yml中添加deploy参数：
```
  - type: git
    repo: git@vps-ip:/home/git/hexo.git
```

### 服务端
服务端添加用户

`adduser git`

设置用户权限，在/etc/sudoers中增加如下内容：
```
## Allow root to run any commands anywhere
root    ALL=(ALL)     ALL
git   ALL=(ALL)     ALL //添加一行git用户权限
```
同时增加git用户对相关文件夹的读写权限：
```
chown git:git -R /home/git
chown git:git -R /var/www/html
```
然后将本地ssh公钥上传，并在服务端建立网页共享git库。
```
mkdir /home/git/.ssh && cd /home/git/.ssh
vim authorized_keys
mkdir /home/git/hexo.git
cd /home/git/hexo.git
git init --bare
```
接着配置hooks

`vim hooks/post-receive`

添加如下内容：
```
#!/bin/bash
git --work-tree=/var/www/html --git-dir=/home/git/hexo.git checkout -f
```
设置权限

`chmod +x post-receive`

