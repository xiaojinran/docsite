#### git介绍
- Git（读音为/gɪt/）是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。 [1]  Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。（来自百度百科：[https://baike.baidu.com/item/GIT/12647237?fr=aladdin](https://baike.baidu.com/item/GIT/12647237?fr=aladdin)）
#### 代码库概念
-  在配置管理中，一般有3个库的概念，开发库、受控库、产品库

- **开发库**是开发人员修改代码的地方。
- **受控库**是测试版本代码存放的地方。
- **产品库**是测试通过版本存放的地方。
#### Hello World
*通过一个简单的项目，了解如何使用git同步项目的代码和文档。*
 1. 登录github[新建一个repo仓库](https://github.com/new)，即项目仓库
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/2020042010200476.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpYW9qaW5yYW4=,size_16,color_FFFFFF,t_70)
 2. 获取项目地址
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200420102110270.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpYW9qaW5yYW4=,size_16,color_FFFFFF,t_70)
 3. 得到项目的git地址后，通过git客户端进行clone，这里使用linux cli命令行

```bash
~ git clone https://github.com/xiaojinran/helloworld.git
Cloning into 'helloworld'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
```
 4. 在本地目录新建文件或者文档后，通过git add提交到本地仓库
- 新建一个文档
```bash
~ cat >HelloWorld.html <<EOF
> <p>HellWorld,Welcome github,Hoping you enjoy it!!!</p>
> EOF
~ ls
HelloWorld.html  README.md
```
- 提交并确认到本地仓库

```bash
git add .
git commit

Add HelloWorld.html
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Your branch is ahead of 'origin/master' by 1 commit.
#   (use "git push" to publish your local commits)
#
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       new file:   HelloWorld.html
```


 5. 使用git push提交到github账户

```bash
 ~ git push origin
```
- 输入账号和密码

```bash
Username for 'https://github.com': xiaojinran
Password for 'https://xiaojinran@github.com': 
Counting objects: 4, done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 344 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/xiaojinran/helloworld.git
   9b5f7fd..8afe9f8  master -> master
```

 6. 登录github.com，即可查到项目已经被更新了
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200420104153757.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpYW9qaW5yYW4=,size_16,color_FFFFFF,t_70)

#### 托管项目产品文档
 -  如果你的项目产品文档是静态的，可以托管在github上面，具体配置如下：
 1. 打开项目设置
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200420104901390.png)
 2. 设置托管分支和目录
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200420105049998.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpYW9qaW5yYW4=,size_16,color_FFFFFF,t_70)
 3. 访问产品文档地址
[https://xiaojinran.github.io/helloworld/HelloWorld.html](https://xiaojinran.github.io/helloworld/HelloWorld.html)
  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200420105444641.png)
#### 小结
- 一个简单的对github的使用，希望能帮助入门的开发者或者文件管理者了解代码仓库的概念，github提供了非常多的有用的工具，比如通知机制、回调机制等，希望大家可以多多发掘。
