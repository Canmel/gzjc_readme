# HTTP服务

## HTTP使用简介

封装好的Http服务在app/service/http.service.ts中

* 在要使用的组件或服务的的ts中导入HttpService

```js
import { HttpService } from '../service/http.service';
```

* 在要使用的组件ts中添加`providers`或服务中直接导入

```js
@Component({
    selector: 'angular-users',
    templateUrl: './users.component.html',
    styleUrls: ['./users.component.css'],
    providers: [HttpService,]
})
```



