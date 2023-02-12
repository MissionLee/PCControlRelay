# 开发笔记

## 目标

- 一个APP（手机网页），里面是一个简单的画面，放置几个按钮，有按下，弹起两个状态
- 一个后台应用
    - APP操作发送给PLC进行操作
    - PLC状态变化同步到APP上
    - Redis高速缓存
    - Mysql持久化记录
- PLC控制程序
    - 简单的通过内存点位映射，操作继电器开关
    - 物理闭合 优先于 APP分，这样能用上两个开关

## 20230212
- 学习了一下Snap7的一些知识，原则上可以用来进行PLC控制，后续需要时间
- 1.创建了新项目 PCControlRealy
    - ⭐直接用idea的项目快捷创建，选择下面的模块
    - SpringWeb
    - JDBC Api
    - MyBatis Framework
    - MySQL Driver
    - Spring Data Redis
- 2.项目加入git管理（直接对接我的github账户）
  - 在首目录下
  - git init
  - git add .
  - git remote add origin git@github.com:MissionLee/PCControlRelay.git
  - git branch -M main
  - git push -u origin main
  - 后续直接使用idea的git功能，不再用命令行了
- 3.同一个目录下创建一个用于前端开发的文件夹 WebPage,初始化一个vue项目
  - 前端vue框架选择了 VUESTIC
  - npm install vuestic-ui
  - 