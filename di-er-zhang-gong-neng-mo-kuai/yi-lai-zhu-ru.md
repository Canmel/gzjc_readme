# 依赖注入

## 依赖注入简介

* **注入器\(Inject\)**:就像制造工厂，提供了一些列的接口用于创建依赖对象的实
* **Provider**：用于配置注入器，注入器通过它来创建被依赖对象的实例，Provider把标识映射到工厂方法中，被依赖的对象就是通过该方法创建的
* **依赖\(Dependence\)**：指定了被依赖对象的类型，注入器会根据此类型创建对应的对象

## 依赖注入

* 在要注入的组件或服务

> import {Injectable} from "@angular/core";
>
> @Injectable\(\)
>
> export class LoggerService {
>
> }

* 构造函数中注入所依赖服务

```js
export class ContactService{
  //构造函数中注入所依赖服务
  constructor(private _logger:LoggerService){}
  getCollections(){
    this._logger.log('获取联系人...')
  }
}
```

* 在组件providers元数据中注册服务

```js
providers:[LoggerService,ContactService]
```



