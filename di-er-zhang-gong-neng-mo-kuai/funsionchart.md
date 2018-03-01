# FunsionChart

## FunsionChart 使用简介

* 在需要使用`Funsioncharts`的`html`页面,使用`fusioncharts`标签,并向`fusioncharts`组件传递参数

```html
<fusioncharts [width]="chart.width" [height]="chart.height" [type]="chart.type" [dataFormat]="chart.dataFormat" [dataSource]="chart.dataSource">
            </fusioncharts>
```

* 在`ts`中定义这些需要传递的参数

```js
export class HomeComponent implements OnInit {
    public chart: object;

    constructor() {}

    ngOnInit(): void {
        // 初始化图表的参数信息
        this.chart = {};
        ...
    }
}
```

### 至此已经可以渲染一个简单的Funsionchart的图标

关于FunsionChart的详细配置信息，请前往官

---

网查看详细配置

funsionchart： [https://www.fusioncharts.com/](https://www.fusioncharts.com/)

