# Blog

一个前端基于 Vue.js，后端基于 Node.js 的博客内容管理器

## Features

* 支持MarkDown语法编辑
* 博客页面对移动端优化
* 支持代码高亮

### 前端：Vue全家桶
* Vue.js
* Vue-cli
* Vue-Resource
* Vue-Validator
* Vue-Router
* Vuex
* Vue-loader

### 后端
* Node.js
* mongoDB (mongoose)
* Express

### 工具和语言
* Webpack
* ES6
* SASS
* Jade

### 本地测试
* 确保已有node环境
* 配置mongoDB：[官网下载](https://www.mongodb.com/download-center?jmp=nav#community)安装完成后，建立数据库文件夹。以win平台为例，在C盘下新建data文件夹，进入data文件夹新建db文件夹（这是mongoDB启动时默认的数据存储目录，如果建立在其他盘上，需要在启动时通过--dbpath参数指定目录。注意mongoDB不会自动创建这个目录，如果没有目录启动时会错误）
进入mongoDB的安装目录，一般在C:\Program Files\MongoDB\Server\3.2\bin（因版本而异）
进入bin目录后，从终端启动目录下的mongod.exe（win可以按住shift右击空白处从当前目录打开命令行）

```
.\mongod.exe
```

在控制台看到 `waiting for connections on port 27017` 表示OK

克隆远程库

```
git clone https://github.com/OrangeXC/blog.git
```

进入项目目录

```
cd blog
```

安装依赖

```
npm install
```

进入服务器所在文件夹并运行服务器

```
cd server
node www
```

打开浏览器输入http://localhost:3000/
如果一切OK，则进入博客的归档页面，登陆按钮在最下方。

> 注意
**第一次从node启动时，数据库会初始化，自动插入两个用户，分别是和'admin'，'游客'，前者有管理员权限，默认密码是111**
如果需要改动，则在第一次启动前打开server目录下的`init.js`，初始化数据放在该文件中。
推荐[Robomongo](https://robomongo.org/)作为mongoDB可视化管理工具
