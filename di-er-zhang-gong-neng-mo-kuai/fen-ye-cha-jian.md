# 分页组件

## 使用简介

* 当前组件中的`html`中

```html
<angular-pagination [pageSize]="pageSize" [totalNum]="totalCount" [curPage]="curPage" [totalPage]="totalPage" (changeCurPage)="getPageData($event)"></angular-pagination>
```

* 在当前组件`ts`中添加

```
export class UsersComponent implements OnInit {
    public totalCount; // 总数据条数
    public pageSize; // 每页数据条数
    public totalPage; // 总页数
    public curPage; // 当前页码

    constructor() {
        this.curPage = 1;
        this.entity = new User;
        this.loggerService.logDebug('loaded User');
    }
}
```



