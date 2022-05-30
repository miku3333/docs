# 文章列表

## 基本介绍

滚动加载无限长时间线

## Example&Format

#### 接口传值

```javascript
<TimeLine config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TimeLine>
// 返回格式
// [{
//     "id": key值,
//     "color": 颜色,
//     "datetime": 发布日期(不支持时间戳),
//     "description": 描述信息,
//     "url": 跳转地址,
// }]
```

#### 右侧显示

```javascript
<TimeLine mode={'right'} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TimeLine>
```

#### 关闭加载信息

```javascript
<TimeLine showToast={false} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TimeLine>
```

#### 自定义加载信息

```javascript
<TimeLine toast={'为您加载了${number}个新节点'} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TimeLine>
```

## API

<!--
&#124;
-->

|      属性       |     说明     |        类型         |                             默认值                              |              备注               |
| :-------------: | :----------: | :-----------------: | :-------------------------------------------------------------: | :-----------------------------: |
|     config      |   请求配置   |       object        | {api: '', method: 'get', params: {}, userProcess: data => data} |       **config.api 必传**       |
|      mode       |   左右模式   | `left`&#124;`right` |                             `left`                              |
| containerHeight |   容器高度   |       number        |                              1000                               |
| containerWidth  |   容器宽度   |       number        |                              1000                               |
|    showToast    | 显示加载信息 |       boolean       |                              true                               |
|      toast      |   提示信息   |       string        |                      加载了${number}个节点                      | ${number}代表请求返回数组的长度 |
