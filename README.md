<div  align="center">
  <img src="https://images.vrm.cn/2018/12/21/TIM截图20181221111148.png" width = "620" height = "500" alt="preview" align=center />
</div>

# 适用于vue的城市选择组件

[在线Demo](https://gzhiyi.top/cn-region-picker/)

基本功能：

1. 支持全选、反选以及全部清空。
2. 支持按拼音筛选。
3. 勾选省份将会勾选省份下所有城市。
4. 返回数据可灵活处理。

## 安装

``` bash
npm install cn-region-picker
# 或者
yarn add cn-region-picker
```

## 用法

组件引入：
```javascript

// import包
import CnRegionPicker from 'cn-region-picker'

// use
Vue.use(CnRegionPicker)
```

使用：

```html
<cn-region-picker
  v-model="pickCity"
  placeholder="城市"
>
</cn-region-picker>

<!-- 省略代码 -->
data () {
  return {
    pickCity: []
  }
}
```

选择返回的数据：

```json
[{
  "cityIndex": 37,
  "id": "210200",
  "name": "大连市",
  "pinYin": "dalian",
  "shortName": "大连"
}, {
  "cityIndex": 41,
  "id": "210600",
  "name": "丹东市",
  "pinYin": "dadong",
  "shortName": "丹东"
}]
```

## 属性

| 参数       | 说明    |  类型  |  默认值  |
| --------   | -----   | ---- |  ----  |
| placeholder| -    | String | 选择城市 |
| showClose| 是否显示input框清空按钮   | Boolean | true |
| clickModal| 是否点击遮罩关闭弹层   | Boolean | true |
| inputClass| 替换预设的输入框样式   | String | null |
| inputWidth| input框宽度   | Number | 200 |

## 本地运行

```bash
npm install
npm run dev
```

## 已更新

#### 1.1.1

1. 增加过度效果、调整按钮样式、调整排序字母样式。
2. 增加npm搜索关键字。

#### 1.1.3

1. 增加关闭弹层按钮、增加输入框清空按钮。
2. 增加输入框样式替换、增加输入框宽度属性。
3. 增加点击遮罩关闭事件。

#### 1.1.4

1. 修复bug：字母选择会重置勾选项的问题。
2. 增加input框关闭图标大小。
3. 更新checkbox样式。

#### 1.1.5

1. 增加默认城市，对应默认传入必须为数组，结构和选择的一致。
2. 优化了关闭按钮布局。
