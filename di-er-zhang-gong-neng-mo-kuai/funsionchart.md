# FunsionChart

## FunsionChart 使用简介

* 在需要使用`Funsioncharts`的`html`页面,使用`fusioncharts`标签,并向`fusioncharts`组件传递参数

```html
<fusioncharts [width]="chart.width" [height]="chart.height" [type]="chart.type" [dataFormat]="chart.dataFormat" [dataSource]="chart.dataSource">
            </fusioncharts>
```

* 在`ts`中定义这些需要传递的参数

```
export class HomeComponent implements OnInit {

    constructor() {}
    
    ngOnInit(): void {
		this.getColumn2dData();
		this.getMscombi2dData();
		this.getColumn3dData();
		this.getMscombi3dData();
		this.getPie2dData();
		this.getPie3dData();
		this.getLine2dData();
		this.getLine3dData();
	}
}
```



