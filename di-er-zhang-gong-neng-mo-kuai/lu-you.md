# Angular路由

## 路由使用简介

### Base href {#articleHeader2}

在`index.html`中定义根路径，告诉angular路由，应用程序的根目录是 `/`

```html
<html>
  <head>
    <base href="/">
    <title>Application</title>
  </head>
  <body>
    <app-root></app-root>
  </body>
</html>
```

定义一个路由`app-routing.module.ts`中：

```js
{
        path: 'maps',        // 路径名称
        component: BaiduMapComponent        // 组件类型名称
}
```





创建子路由可以查看 \[创建子路由\]\([https://segmentfault.com/a/1190000009265310](https://segmentfault.com/a/1190000009265310)\)

