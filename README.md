## Blog

fork from [My Blog](https://github.com/ZHENFENG13/My-Blog) , 该作者是在 [Tale](https://github.com/otale/tale) 博客系统基础上进行修改的。

`Tale` 使用了轻量级 mvc 框架 `Blade` 开发，默认主题使用了漂亮的 `pinghsu` 。

`My-Blog` 使用的是 Docker + SpringBoot + Mybatis + thymeleaf 打造的一个个人博客模板。

## 根据原项目修改记录
1. 将spring boot的版本从`1.5.1.RELEASE`修改为`2.2.5.RELEASE`
2. tale.sql中添加创建DATABASE操作
3. 将MySQL驱动版本指定为5.1.47
4. 將原有的druid依赖为1.1.23
5. 升级pagehelper到1.2.5
6. 升级后会去t_contents中查询favicon.ico数据，但是原始建表语句中不包含此语句导致不能成功登录，现零时为t_contents添加一条slug为`favicon.ico`的数据(后期有空再优化)
> 2020-12-24零时修改一版，后续有空再继续升级包括但不限于模块拆分、引入微服务及其他更符合当下使用的框架...

## 启动流程
1. 获取对应Maven依赖
2. 执行resources/sql/tale.sql
3. 根据自身情况修改application-jdbc.properties中关于数据库的配置信息
4. 启动项目
5. 访问client：http://localhost:8081/
6. 访问admin：http://localhost:8081/admin/login  user:admin,password:123456

## 功能如下：

 博客首页：
 ![](img/index.png)

 归档：
 ![](img/metas.png)

 友链：
 ![](img/links.png)
 
 关于：
 ![](img/about.png)
 
 搜索：
 ![](img/search.png)
 
 **后台管理**
 
 管理登录：
 ![](img/admin-login.png)
 
 管理首页：
 ![](img/admin-index.png)
 
 发布文章：
 ![](img/admin-publish.png)
 
 文章管理：
 ![](img/admin-article.png)
 
 页面管理：
 ![](img/admin-pages.png)
 
 分类标签：
 ![](img/admin-category.png)
 
 文件管理：
 ![](img/admin-upload.png)
  
 友链管理：
 ![](img/admin-links.png)
   
 系统设置：
 ![](img/admin-setting.png)
 
## 开源协议

[MIT](./LICENSE)

## 感谢

[ZHENFENG13](https://github.com/ZHENFENG13)
[otale](https://github.com/otale)
