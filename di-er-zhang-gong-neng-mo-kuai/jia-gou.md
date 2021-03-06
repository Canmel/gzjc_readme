## 基本架构介绍

本系统涉及前端框架为`Angular4` 以及 一部分的`Jquery` 和一点 `Bootstrap`

---

## Angular4

> angular是一个比较完善的前端MVC框架，包含了模板，数据双向绑定，路由，服务，过滤器，依赖注入等等所有的功能，基本上只要你做web开发，angular都会提供一个，换句话说，相对于一些其它的只关注前端某一方面的框架来说，学习angluar这么一个框架，往框架里填东西，基本上可以搞定前端开发的所有问题

### 配置

Angular的开发环境配置需要`Node.js`和`npm`的支持,首先需要安装`node`和 `npm`

#### 安装Node.js {#一安装nodejs}

> 官方网址：[https://nodejs.org/en/download/](https://nodejs.org/en/download/)

#### 安装Angular CLI 脚手 {#二全局安装angular-cli-脚手架工具}

安装npm

> npm install -g @angular/cli

安装`cnpm`,国内直接装经常会出问题，所以设置为淘宝镜像地址会更好。

> npm install -g cnpm --registry=[https://registry.npm.taobao.org](https://registry.npm.taobao.org)

若安装失败后重新安装先清除缓存

> npm uninstall -g @angular/cli   //卸载angular/cli /
>
> npm cache clean  //清除缓存
>
> cnpm install -g @angular/cli    //重新安装

检查cli是否安装成功

> ng -v //查看版本能否正常显示

### angular-cli的使用

#### 安装第三方插件

> npm install  // 或者 cnpm

#### 启动项目

> ng serve  // 默认端口 4200

#### `angular-cli`命令

> ng g c componentName   // 新建组件    ng generate component componentName
>
> ng g cl className            // 新建class   ng generate class className
>
> ng g s serviceName          // 新建服务    ng generate service serviceName
>
> ng g e enumName             // 新建枚举    ng generate enum enumName
>
> ng g d directiveName        // 新建指令    ng generate directive directiveName
>
> ng g p pipeNmae               // 新建管道    ng generate pipe pipeName
>
> ng g m mouduleName      // 新建模块    ng generate module moduleName

### 文件结构

* node\_moudles  `package.json`中列举的所有第三方模块都放在其中
* src  应用代码位于`src`文件夹中
* e2e 点对点测试

---

其他目录信息可在 [https://www.angular.cn/guide/quickstart\#src](https://www.angular.cn/guide/quickstart#src) 中查看

