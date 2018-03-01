# Angular父子组件通信

子组件存在于父组件“体内”，避免重复制造，父子组件之间则需要数据传递等问题

## 父组件向子组件传入数据 – @Input {#父组件向子组件传入数据-input}

父组件html

```html
<angular-pagination [curPage]="curPage" (changeCurPage)="getPageData($event)"></angular-pagination>
```

标签名： angular-pagination // 子标签  selector

属性： \[pageSize\]="pageSize" ==&gt; \[子组件属性\]=“父组件属性”

通过以上方式将参数信息传递到子组件，具体的父组件中的属性值需要在父组件ts文件中创建：

```js
export class UsersComponent implements OnInit {
    public curPage = 1;    // 在父组件中定义
    constructor() {}
    ngOnInit() {}
}
```

子组件ts导入Input，使用@Input装饰器装饰需要接受父组件传递的参数即可获取父组件传递来的参数

```js
import { Component, OnInit, Output, Input, EventEmitter } from '@angular/core';

...
export class XxxxComponent implements OnInit {
    @Input('curPage') curPage;
}
```

## 子组件通知父组件数据已处理完成 – @Output、EventEmitter {#子组件通知父组件数据已处理完成-outputeventemitter}

子组件向父组件传递参数通过 `EventEmitter`传播通知父组件，使用装饰器`@Output`装饰要传递的参数,创建`EventEmitter`对象,在需要向父组件传递参数的时候使用`EventEmitter`对象将事件传播出去。

```js
import { Component, OnInit, Output, Input, EventEmitter } from '@angular/core';

...
export class XxxxComponent implements OnInit {
    @Input('curPage') curPage;

    @Output() changeCurPage: EventEmitter < Number > = new EventEmitter;

    constructor() {}

    ngOnInit() {}
}
```



