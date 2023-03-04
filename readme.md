# 企业内部培训系统

### 组织结构

```
MOOC
├── MOOC-Android -- 企业内部培训系统-移动端
├── MOOC-SpringCloud -- 后台系统接口
└── MOOC-Vue-Admin-Template -- 企业内部培训后台管理系统
```

## 相关项目

- [MOOC-SpringCloud](https://github.com/saiGou-14H/MOOC-SpringCloud)
- [MOOC-Vue-Admin-Template](https://github.com/saiGou-14H/MOOC-Vue-Admin-Template)
- [MOOC-Android](https://github.com/saiGou-14H/MOOC-Android)

## 项目简介

​		企业内部培训软件用来支持企业内部教师和员工的在线授课和学习过程。企业内部培训软件是一个基于web的多终端（PC端、移动端）应用形式，可以通过互联网进行访问。

​		提出开发企业内部培训软件的客户是某医疗卫生服务单位，该单位职工规模达到了1000人，随着信息化潮流的影响以及其医疗服务员工规模的不断增加，对于管理人员来说，如何培训医疗服务人员变得越来越复杂、繁琐，急需建立一套系统来对员工进行信息化在线培训。

​		系统架构设计采用的是B/S三层结构模式，包含用户表示层、中间层和数据库层。使用该结构模式能使项目架构更为清晰明了，因为这三层每层都分工明确，各司其职，可以让系统服务有条不紊。

​		教师端系统界面需求简洁大方美观，客户体验流畅，操作难度简单，信息到位，具备基本错误信息提示，数据输入提示，页面一致性协调原则等。

​		教师端前端主要使用html5，Vue.js语言进行详细设计，此项目前台页面采用基于vue框架实现的，采用npm方式，用Vue-cli3搭建脚手架结合Vue Router和Vuex以及vant和element-ui组件进行开发。Vue.js是一套构建用户界面的渐进式框架。与其他重量级框架不同的是，Vue 采用自底向上增量开发的设计。Vue 的核心库只关注视图层，并且非常容易学习，非常容易与其它库或已有项目整合。另一方面，Vue 完全有能力驱动采用单文件组件和Vue生态系统支持的库开发的复杂单页应用。通过Router配置路由,路由选项通过组件方式提供。通过axios 与后端接口进行交互。	

​		后端基于java语言，通过SpringCloud框架搭建项目结构，同时将系统分为划分为微服务集群（路由网关、注册中心、用户服务、班级服务、课程服务、社区服务），并结合Redis数据库实现安全验证，使用MySql数据库和Mybatics-Plus框架进行数据持久化。为规范与前端交互的规则，通过API框架-Swagger定义接口文档。

​		企业内部培训客户端用来支持企业内部教师和员工的在线授课和学习过程。该企业内部培训客户端是一个基于Android原生开发的移动端应用形式，可以通过互联网进行访问。

## 系统功能

### Android端

​		企业内部培训客户端用来支持企业内部教师和员工的在线授课和学习过程。该企业内部培训客户端是一个基于Android开发的移动端应用形式，可以通过互联网进行访问。

​		通过对学生端系统的总体需求分析，可将本系统具有浏览课程，购买课程，查看课程及学习课程，报名实践，打卡签到，查看积分流水等功能，功能简述如下图所示。

![image-20230225003240063](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/App/%E7%B3%BB%E7%BB%9F.png)

### WEB端

**教师端/管理端核心功能**

![系统](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

**1.班级模块：**

​		教师登录系统后，可对班级进行添加，删除，修改，查看班级信息和学生信息。教师可查询任意班级的学生总体学习进度及没门课程的学习进度。学习进度通过后端获取的总课程学习时长与已经学习的时长相比可得。

![image-20230225003324610](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/1.png)

点击放大镜按钮，可查看每门课程的学习进度

![image-20230225003349106](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/2.png)

**2.课程模块：**

​		教师可以新建课程(在管理员审核通过后)并且到指定班级，对课程章节进行增删改查等功能，章节拖动功能可任意改变章节序号。

![image-20230225003450429](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/3.png)

**3.咨询模块：**

​		教师登录系统后，点击课程提问可以根据班级，班级课程分类来筛选问题，对学员的问题进行回答，对问题进行采纳等功能。

![image-20230225003516372](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/4.png)

![image-20230225003523575](https://github.com/saiGou-14H/save-image/blob/main/%E4%BC%81%E4%B8%9A%E5%86%85%E9%83%A8%E5%9F%B9%E8%AE%AD%E7%B3%BB%E7%BB%9F/%E5%89%8D%E7%AB%AF/5.png)

## 项目技术栈

**前端技术栈**

| 技术               | 说明             | 链接                                                         |
| ------------------ | ---------------- | ------------------------------------------------------------ |
| Vue                | 前端框架         | [Vue.js](https://vuejs.org/)                                 |
| ElementUI          | 前端UI框架       | [Element - 网站快速成型工具](https://element.eleme.cn/#/zh-CN) |
| axios              | 前端HTTP框架     | [Axios](https://github.com/axios/axios )                     |
| vue-router         | 路由框架         | [router](https://router.vuejs.org/)                          |
| vue-admin-template | 后台管理基础模板 | [PanJiaChen/vue-element-admin: A magical vue admin https://panjiachen.github.io/vue-element-admin](https://github.com/PanJiaChen/vue-element-admin) |

**后端技术栈**

| 技术         | 说明            | 链接                                      |
| ------------ | --------------- | ----------------------------------------- |
| SpringBoot   | Web应用开发框架 | https://spring.io/projects/spring-boot    |
| SpringCloud  | 微服务框架      | https://spring.io/projects/spring-cloud   |
| MyBatis-Plus | ORM框架         | https://baomidou.com/                     |
| Redis        | 内存数据存储    | https://redis.io/                         |
| JWT          | JWT登录支持     | https://github.com/jwtk/jjwt              |
| Lombok       | Java语言增强库  | https://github.com/rzwitserloot/lombok    |
| Swagger-UI   | API文档生成工具 | https://github.com/swagger-api/swagger-ui |

**Android依赖**

```
//GSON库
implementation 'com.google.code.gson:gson:2.8.5'

//网络请求框架
implementation 'com.squareup.okhttp3:okhttp:3.10.0'

//智能刷新框架
implementation 'com.scwang.smartrefresh:SmartRefreshLayout:1.1.3'

//picasso（毕加索）图片处理框架
implementation 'com.squareup.picasso:picasso:2.5.2'

//列表选择控件
implementation 'com.contrarywind:Android-PickerView:4.1.9'

//数据级联选择控件
implementation 'com.github.gamekonglee:regionSelector:2.0'

//富文本编辑器
implementation 'jp.wasabeef:richeditor-android:1.2.0'
implementation 'com.zzhoujay.richtext:richtext:3.0.7' 
implementation 'com.github.widemouth-dz:wmrichtexteditor:2.0.4'
```

