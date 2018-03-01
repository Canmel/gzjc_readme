# Angular父子组件通信

子组件存在于父组件“体内”，避免重复制造，父子组件之间则需要数据传递等问题

## 父组件向子组件传入数据 – @Input {#父组件向子组件传入数据-input}

#### 父组件html

```html
<angular-pagination [pageSize]="pageSize" [totalNum]="totalCount" [curPage]="curPage" [totalPage]="totalPage" (changeCurPage)="getPageData($event)"></angular-pagination>
```

标签名： angular-pagination // 子标签  selector

属性： \[pageSize\]="pageSize" ==&gt; \[子组件属性\]

