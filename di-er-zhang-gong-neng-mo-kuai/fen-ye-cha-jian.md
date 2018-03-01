# 分页组件

## 使用简介

* 当前组件中的`html`中

```html
<angular-pagination [pageSize]="pageSize" [totalNum]="totalCount" [curPage]="curPage" [totalPage]="totalPage" (changeCurPage)="getPageData($event)"></angular-pagination>
```

* 在当前组件`ts`中添加



