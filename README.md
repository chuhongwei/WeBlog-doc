 # 开发项目--WeBlog 博客网站
 [toc]

 ## 一、组员博客总结

| github 用户名 | 姓名   | 学号     | 项目小结                                                     |
| ------------- | ------ | -------- | ------------------------------------------------------------ |
| chuhongwei    | 褚宏伟 | 18342014 | [简单web服务开发](https://gitee.com/chuhw3/game_unity/blob/master/service/%E7%AE%80%E5%8D%95web%E6%9C%8D%E5%8A%A1%E5%BC%80%E5%8F%91%E5%B0%8F%E7%BB%93.md) |
| beilineili    | 黄进   | 18342029 |                                                              |
| zengty-2018   | 曾涛煜 | 18342007 | [服务计算作业九——前后端分离的开发](https://blog.csdn.net/Floating__dust/article/details/111489655) |
| zhanky3       | 詹科宇 | 18342124 | [服务计算hw9———简单 web 服务与客户端开发实战](https://blog.csdn.net/weixin_43963659/article/details/111475896)                                                            |
<br>



 ## 二、服务端和客户端
 ### 1. 各个仓库地址
由 github 组织管理项目仓库
 - 项目文档仓库：[https://github.com/chuhongwei/WeBlog-doc](https://github.com/chuhongwei/WeBlog-doc)
 - 服务端仓库（基于 REST API）：[https://github.com/chuhongwei/BlogServer](https://github.com/chuhongwei/BlogServer)
 - 客户端仓库（基于 Vue.js）：[https://github.com/zengty-2018/WeBlog_Client](https://github.com/zengty-2018/WeBlog_Client)
<br>



### 2. 前后端安装指南
#### ① 后端安装

 1. 利用命令go get -v github.com/chuhongwei/BlogServer将本项目clone到本地的go工作空间中。
 2. 切换到博客源代码存放位置，执行go run WriteBlog.go来调用写博客到数据库的功能，完成数据库的初始化。
 3. 切换到项目的根目录，执行go run main.go来运行服务端程序，等待客户端的请求。

可以执行以下命令启动服务端

```
go get -v  github.com/chuhongwei/BlogServer
cd $GOPATH/src/github.com/chuhongwei/BlogServer/source/Blogs
go run WriteBlog.go
cd ../..
go run main.go
```
#### ② 前端安装

```
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev
```

<br>



## 三、任务完成情况
| 任务目标                                                     | 完成情况 |
| ------------------------------------------------------------ | -------- |
| 选择合适的 API，实现从接口或资源（领域）建模，到 API 设计的过程 | √        |
| 使用 API 工具，编制 API 描述文件，编译生成服务器、客户端原型 | √        |
| 使用 Github 建立一个组织，通过 API 文档，实现 客户端项目 与 RESTful 服务项目同步开发 | √        |
| 使用 API 设计工具提供 Mock 服务，两个团队独立测试 API        | √        |
| 使用 travis 测试相关模块                                     | √        |
<br>



## 四、数据资源来源

本次项目选用的博客都拉取自 CSDN 博客网站
 - [2021年GO语言（Golang）就业班全系列](https://blog.csdn.net/weixin_40562504/article/details/108641202)
 - [B/S架构及其运行原理](https://blog.csdn.net/qq_40587575/article/details/79673478)
 - [Beego_ubuntu下golang及beego环境的全局配置](https://blog.csdn.net/weixin_43851310/article/details/88543162)
 - [Go&&阿里云服务器（Ubuntu）-- Golang项目（beego）服务器部署](https://blog.csdn.net/qq_42410605/article/details/96479892)
 - [Go - 学习/实践](https://blog.csdn.net/william_n/article/details/102893655)
 - [阿里巴巴十年Java架构师分享，会了这个知识点的人都去BAT了](https://blog.csdn.net/t4i2b10X4c22nF6A/article/details/79062764)
 - [领域驱动实践总结(基本理论总结与分析+架构分析与代码设计+具体应用设计分析V)](https://blog.csdn.net/xiaofeng10330111/article/details/105148032)
 <br>



## 五、项目要求
| 项目要求           | 实现情况                           |
| ------------------ | ---------------------------------- |
| 开发周期           | 2周                                |
| API 设计           | 参考 github v3                     |
| 资源来源           | 来自 CSDN 博客网站的真实数据       |
| 服务器端数据库支持 | boltDB                             |
| 页面数             | 5页                                |
| API 数             | 6个                                |
| API 要求           | 支持分页                           |
| 加分项             | 实现 注册/登录 API 支持 Token 认证 |
<br>



## 六、API 说明
```
//获取博客文章的简要信息
GET /articles

//根据 id 获取某篇文章的详细内容
GET /article/{id} 

//根据 id 获取文章的评论
GET /article/{id}/comments

//用户提交评论到文章中
POST /article/{id}/comments 

//用户登录
POST /user/login 

//用户注册
POST /user/register
```
