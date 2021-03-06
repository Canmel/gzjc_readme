# EchartsMap拓展SVG

---

## 使用简介

* 在`app/echarts-map/echarts-map.component.css`中定义需要渲染地图页面的`div`的类-

* 当前`html`中:

```html
<angular-echarts-map [option]="option" [svg]="svgRoute" [selector]="echartMapArea" (clickCallBack)="mapClickCallBack($event)">
</angular-echarts-map>
```

* 在当前`component`中定义 `option`, `svg` 和选择器 `id`

```js
export class XxxxComponent implements OnInit {
    public svgRoute = "assets/svg/ningbo.svg";    // svg的路径
    public echartMapArea = "echarts-render-area";  // 提供给js的ID选择器,单页面内不重复即可
    public option; // Echarts 生成规则

    constructor() {
        // 初始化
        ...
    }
}
```

* 至此地图基本渲染完成
* 设置地图点击事件回调函数

```js
export class XxxxComponent implements OnInit {
    public svgRoute = "assets/svg/ningbo.svg";    // svg的路径
    public echartMapArea = "echarts-render-area";  // 提供给js的ID选择器,单页面内不重复即可
    public option; // Echarts 生成规则

    constructor() {
        // 初始化
        ...
    }

    // 回调函数
    mapClickCallBack(){
    }
}
```

* 其他关于`echart`的操作信息请前往官网示例 [http://echarts.baidu.com/echarts2/doc/example.html](http://echarts.baidu.com/echarts2/doc/example.html)



