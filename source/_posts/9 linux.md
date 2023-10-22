---

title: 'linux'

date: 2023-02-03 00:00:00

---

# Linux

[TOC]

## 常用命令

```
# 更改权限
chmod -R 777 node 
# 更改文件所有者
chown -R lighthouse:lighthouse node-v16.15.0-linux-x64
```



## 保塔安装

```
# root 权限
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh ed8484bec      

外网面板地址: http://43.143.137.233:8888/nidhogg-
内网面板地址: http://10.0.16.7:8888/5da27aaa
username: fkqoiepu
password: 1607c509

```

su 报错bash: __bp_precmd_invoke_cmd: command not found

````
# 进入root权限
cd /root
ls -a
vim .bashrc
在行尾添加unset PROMPT_COMMAND
退出
source .bashrc
https://blog.csdn.net/lzsm_/article/details/126083649
````



## blog

### hexo

#### 01 nodejs安装

官网下载：https://nodejs.org/en/download/

https://nodejs.org/dist/

上传，解压

```
# tar -xvf [压缩包] -c [目标位置]
tar -xvf node-v16.15.0-linux-x64.tar.xz 
```

配置环境变量

```
# 在解压的目标位置用 ll -A找到.hasbrc
cd /home/lighthouse/
ll -Al
sudo vim .bashrc
# 最后添加
export PATH=$PATH:/home/lighthouse/node-v16.15.0-linux-x64/bin
# 退出后刷新
source .bashrc

node -v
npm -v
```

#### npm

升级

```
npm install -g npm
# 也可以指定版本
npm install -g npm@8.5.3
```

安装、卸载

```
npm un hexo-renderer-marked
npm i hexo-renderer-pandoc
```

这里还需要提一下的是`npm`默认的官网源可能会比较慢，如果想要后续的下载速度快一些，可以通过下面的方式将源设置为淘宝源。

```
npm config get registry
# 查看原来的源
npm config set registry https://registry.npm.taobao.org
# 修改为淘宝源
npm config get registry
# 查看现在的源
```



#### 02 安装hexo

```
npm install hexo-cli -g
```

创建blog目录

```
hexo init [目录] 
```

git 托管

```
git init

----------------------------------------------------------------
如果报错
    hint: Using 'master' as the name for the initial branch. This default branch name
    hint: is subject to change. To configure the initial branch name to use in all
···
执行
git config --global init.defaultBranch main
################################################################
如果报错
	bash: git: command not found
执行
yum install -y git
----------------------------------------------------------------

git config --global user.name 'rebort-snow'
git config --global user.email '745406531@qq.com'
```

配置ssh

```
https://blog.csdn.net/qq_40047019/article/details/122898308
```

在博客目录的_config最后面完善

```
deploy:
  type: 'git'
  repo: 'git@github.com:rebort-snow/rebort-snow.github.io.git'
  branch: main
```

安装插件

```
npm install hexo-deployer-git --save
```

#### 01 基本指令

1. 745406531@qq.com
2. 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
3. hexo clean # 清理缓存
4. hexo g # 生成文件
5. hexo s # 本地预览
6. hexo d # 上传git仓库
7. hexo clean & hexo g && hexo d
8. git status
9. git add .
10. git branch -M main
11. git commit -m "first commit"
12. git push
13. 链接:http://43.143.137.233:32352/down/5wgjlNLi3jw1.git/index 提取码:ZNxc25

#### 02 [文章加密](https://blog.csdn.net/wwlk123/article/details/124436871)

 1.  博客目录下安装插件

     ```
     npm install hexo-blog-encrypt
     ```

 2.  添加_config.yml配置:

     ```	YML
     encrypt:
       enable:true
     ```

 3.  文章设置加密字段：

     ```markdown
     ---
     title:       
     date:
     password:
     message:
     ---
     
     ---
     title:        # 标题
     date:		 # 日期
     password:	  # 密码
     message:	 # 密码提示信息
     ---
     ```



#### 03 文章局部HTML代码不渲染



### butterfly

#### 01 安装:



#### 1 butter无法显示图片

- 图床需要有ssl证书，可在freessl获取(csr自己设置，CDN自动验证，大概10min)
- [解决hexo引入图床，手机和web不显示图片的问题 - 简书 (jianshu.com)](https://www.jianshu.com/p/5b58ecce6443)

<img src="http://nidhogg-110.cn/image-20221106185159998.png" alt="image-20221106185159998" style="zoom: 67%;" />

<img src="http://nidhogg-110.cn/image-20221106185216478.png" alt="image-20221106185216478" style="zoom: 80%;" />

![image-20221107193612000](http://nidhogg-110.cn/image-20221107193612000.png)



#### 2 底部透明

修改/home/lighthouse/blog/node_modules/hexo-theme-butterfly/source/css/_layout下的footer.styl文件

![image-20221123160159212](http://nidhogg-110.cn/image-20221123160159212.png)



## python

### step1安装依赖以及环境

```
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel gcc-c++
```

### step2下载python3.6

```
wget https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tgz
```

### step3安装Python3

解压python3.tgz

```
tar -xvf Python-3.8.2.tgz
```

创建python3的文件路径

```
mkdir /usr/local/python3
```

### step4编译（在解压的文件夹下）

```
cd Python-3.8.2/
./configure --prefix=/usr/local/python3
```

### step5安装（在解压的文件夹下 ）

```
make
make install
##先make再make install
```

### step6：创建新版本软连接

　①修改旧版本

```
mv /usr/bin/python /usr/bin/python_bak
```

　②创建新的软连接

```
ln -s /usr/local/python3/bin/python3 /usr/bin/python
```

　③检查python的版本

```
python -V
```

### step7：配置pip3

将/usr/local/python3/bin加入PATH

```
vim ~/.bash_profile

# .bash_profile

# Get the aliases and functions
if [ -f ~/.bashrc ]; then
        . ~/.bashrc
fi

# User specific environment and startup programs

PATH=$PATH:$HOME/bin:/usr/local/python3/bin

export PATH
```

保存退出后，执行以下命令，让上一步修改操作立即生效

```
source ~/.bash_profile
```

如果没有配置成功执行以下代码

```
# 进入usr/bin目录
cd /usr/bin

# 查看pip前缀的文件
ll pip*
 
# 删除pip文件
c
 
# 重新设置pip文件
ln -sf /usr/local/python3/bin/pip3 /usr/bin/pip
 
# 可以再补加一个pip3命令
ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3

```

### step8：更新pip3 版本

查看当前pip3版本信息

```
pip3 -V
pip -V

pip3 install --upgrade pip
```

### python系统命令

#### os.system('')

```
os.system('command')

```

#### os.popen('')

```
# os.popen()返回状态值 0:执行成功
f=os.popen('cd /home/lighthouse')
# f记录命令值
print(f)
```

执行多行系统命令

```
os.popen("cd /home/lighthouse/demo/test/cl && hexo clean && hexo g && hexo d")

注意：
1. 命令被分号“;”分隔，这些命令会顺序执行下去；
2. 命令被“&&”分隔，这些命令会顺序执行下去，遇到执行错误的命令停止；
3. 命令被双竖线“||”分隔，这些命令会顺序执行下去，遇到执行成功的命令停止，后面的所有命令都将不会执行;
```

