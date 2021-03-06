# HTTP服务

---

## HTTP使用简介

封装好的`Http`服务在`app/service/http.service.ts`中

* 在要使用的组件或服务的的ts中导入`HttpService`

```js
import { HttpService } from '../service/http.service';
```

* 在要使用的组件ts中添加`providers`或服务中直接导入

```js
@Component({
    selector: 'angular-users',
    templateUrl: './users.component.html',
    styleUrls: ['./users.component.css'],
    providers: [HttpService]
})
```

* 在`constructor`中添加`httpService`

```js
constructor(private httpService: HttpService) {}
```

* 使用

```js
this.httpService.get(Urls.USERS, {
    pageNo: pageNo
});
```

### HttpService 方法

```js
get(url: string, params: any): Promise < Object >
post(url: string, params: any): Promise < Object >
put(url: string, params: any): Promise < Object >
delete(url: string, params: any): Promise < Object >
```

### HttpService 请求异常

以上请求异常会调用,集中处理

```js
private handleError(error: any): Promise < any >
```



