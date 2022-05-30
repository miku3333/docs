# 文章列表

## 基本介绍

滚动加载无限长列表

## Example&Format

```javascript
<ArticleList config={{ api: '/api/articleList', userProcess: data => data.list }}></ArticleList>
// 返回格式
// [{
//     "id": key值,
//     "imgUrl": 图片url,
//     "tag": [标签],
//     "datetime": 发布日期(不支持时间戳),
//     "title": 标题,
//     "description": 描述信息,
//     "pv|1000-9999": 点击数,
//     "url": 跳转地址,
//     "mainTag": {
//         "text": 主标签文字,
//         "url": 主标签跳转地址,
//     }
// }]

```

## API

<!--
&#124;
|   属性   |   说明   |  类型  | 默认值 |             备注              |
| :------: | :------: | :----: | :----: | :---------------------------: |
| | | | |
 -->

|       属性        |     说明     |                             类型                             |                默认值                |              备注               |
| :---------------: | :----------: | :----------------------------------------------------------: | :----------------------------------: | :-----------------------------: |
|      config       |   请求配置   |                            object                            | {api: '', method: 'get', params: {}, userProcess: data => data} |            **config.api必传**             |
|  containerHeight  |   容器高度   |                            number                            |                 1000                 |
|  containerWidth   |   容器宽度   |                            number                            |                 1000                 |
|    itemHeight     |  item 高度   |                            number                            |                 200                  |
|  mainTagPosition  |  主标签位置  | leftTop &#124; leftBottom &#124; rightTop &#124; rightBottom |               leftTop                |
| scaleImageOptions | 缩放图片配置 |                            object                            |                  {}                  |
|     showToast     | 显示加载信息 |                           boolean                            |                 true                 |
|       toast       |   提示信息   |                            string                            |        加载了${number}篇文章         | ${number}代表请求返回数组的长度 |
