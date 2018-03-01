# HTTP服务

## HTTP使用简介

封装好的Http服务在app/service/http.service.ts中

* 在要使用的组件的ts中导入HttpService

```
import { HttpService } from '../service/http.service';
```

* 在要使用的组件ts中添加`providers`

```js
@Component({
    selector: 'angular-users',
    templateUrl: './users.component.html',
    styleUrls: ['./users.component.css'],
    providers: [UserService, ErrorFormTipsService, HttpService, LoggerService]
})
```



