# 陌筹 StrangeRaise
# For English Version: https://xiangfm.wordpress.com/2017/06/22/strangeraise/ 
## 项目背景

大学生是一个富有想法和意见的群体，但其想法和意见的实现却往往由于“单兵作战”而显得势单力薄。陌筹希望为大学生群体提供一个开放的筹众平台，在这里他们可以发起自己的项目，招募人手、“招兵买马”，征求意见、展开讨论，利用互联网让每个大学生都能够拥有实现其想法的能力。

举例说明：小李同学从小就有一个拍电影的梦想，他有一个自己觉得不错的剧本，但也就是仅仅准备好了剧本而已。通过陌筹筹众平台，小李同学发起了这个拍摄、制作电影的项目，寻找到了合适的摄影师和演员，最终实现了他的电影梦。

总得来说，陌筹希望赋予每个大学生实现自己想法的能力。

## 功能简介

陌筹筹众平台旨在在项目的筹备阶段、宣传阶段、完成阶段为用户提供服务。

在筹备阶段，大学生用户可以通过发起项目将项目信息、所需人手、预期回报（物质或非物质）等内容发布至平台，供其他在线用户浏览、评价及支持。平台会根据标签机制为项目发起者提供合适的合作者推荐，也可以为普通用户推荐感兴趣的项目。

在宣传阶段，项目发起者可通过修改项目进行状态、发布项目日志便于其他在线用户了解项目进度和情况。

在完成阶段，平台为用户提供可信度评价机制，供用户对项目及项目成员进行评价，并收集其反馈意见。

## 前端技术介绍

### FlatUI框架（基于Bootstrap）+卡片式风格

网站整体采用扁平化风格FlatUI框架提供的控件样式，如输入框、按钮等。

<p align="center">
<img src="http://i.imgur.com/ykxFjnd.png">
Fig. 首页及项目卡片
</p>

网站主体为手写DIV+CSS，色调上与FlatUI贴合，在网站中大量采用卡片式的展示风格，如首页对项目摘要内容的展示，项目具体内容界面显示等。

<p align="center">
<img src="http://i.imgur.com/xCRJQzy.png">
Fig. 项目内容查看页
</p>

<p align="center">
<img src="http://i.imgur.com/1xrUA70.png">
Fig. 个人页
</p>

### FormValidation表单验证插件

在网站中，有多处地方需要键入内容，此时则需要对输入内容进行表单验证，保证所输入数据的有效性，同时也保护数据库不被恶意插入脏数据。

由于FlatUI是基于Bootstrap的，于是项目采用一个针对Bootstrap框架的基于jQuery的表单验证插件FormValidation，FormValidation可对一个输入框同时做多种验证，并异步显示出来。

<p align="center">
<img src="http://i.imgur.com/CYF7rTk.png">
Fig. 注册界面邮箱验证错误
</p>

<p align="center">
<img src="http://i.imgur.com/nNZNaH9.png">
Fig. 注册界面邮箱验证成功
</p>


### 多平台自适应

由于该项目为Web项目，故网站可跨平台访问浏览，因此网站应为响应式的，在不同分辨率的平台上可以做到自适应，这样可以保证浏览效果。

在前端实现时，网站使用了Bootstrap的栅栏系统，将卡片式的模块嵌入栅栏系统中，使其成为响应式，根据窗口大小显示内容。网站设置了最小宽度，既可以保证在手机上的显示效果，又能保证在电脑端将浏览器窗口缩放时，不会使文字内容溢出其所属块。

<p align="center">
<img src="http://i.imgur.com/kQygRLr.jpg">
Fig. 首页PC端、手机端效果展示
</p>

<p align="center">
<img src="http://i.imgur.com/FdBzTOz.png">
Fig. 登录模态框PC端、手机端效果展示
</p>

<p align="center">
<img src="http://i.imgur.com/cQ7tXaB.png">
Fig. 项目内容界面PC端、手机端效果展示
</p>


