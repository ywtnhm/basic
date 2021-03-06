# basic

> Gradle搭建的 SpringBoot + Vue 前后端分离（含移动端）且合并打包的基本框架

## 子项目说明

```
tool    后端工具子项目
common  后端通用子项目
server  后端Api接口子项目
web     WEB端Vue子项目
webapp  移动端Vue子项目
```

## 搭建时环境

```
JDK: Java SE Development Kit 8u131
IDE: IntelliJ IDEA 2017.1.5
Gradle: v4.0.1
Node.js: v6.11.0 LTS
Vue-CLI: 2.8.2
```

## 开发调试

```
一、先运行server子项目的, 启动SpringBoot.
二、再运行 web/webapp 子项目的npmDev任务, 启动node的开发服务器.
三、当 web/webapp 子项目有请求需要调用SpringBoot后台, 加上/api前缀去请求即可代理从node的开发服务器http://localhost:3000/api/xxxx或http://localhost:8000/api/xxxx代理到http://localhost:8080/api/xxxx.
四、而在开发前台页面时候（对web/src或webapp/src目录下的文件修改）, 应该访问http://localhost:3000或http://localhost:8000, 而不是8080端口, 访问3000或8000端口, 即可看到页面修改的即时效果.
```

## 打包发布

```
运行server子项目的build任务, 即可完成打包. 打包的jar包已经包含web子项目和webapp子项目的输出内容.
```

## 备注

```
默认不需要安装Node, web子项目和webapp子项目中配置了自动安装Node, 版本v6.11.0 LTS, 如不想使用该配置请自行修改并配置Node.
```
