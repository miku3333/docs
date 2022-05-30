# 归档

## 基本介绍

实现归档等功能的列表

## Example&Format

#### 接口传值

```javascript
<File config={{ api: '/api/articleList', userProcess: (data) => data.list }}></File>
// 返回类型
// {
//     list: [
//         {
//             "text": 显示文本,
//             "url": 跳转链接,
//         }
//     ]
// }
```

#### 数据传值

```javascript
const data = [
    {
        text: '节办龙去这声和办量合马影术场。',
        url: 'mid://lkae.bw/wmb',
    },
]
<File initData={data}></File>;
```

#### 每行显示 4 个

```javascript
<File eachline={4} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></File>
```

#### 显示标题

```javascript
<File header={'标题'} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></File>
```

## API

<!--
&#124;
-->

|    属性    |   说明   |  类型  |                                             默认值                                              |                         备注                          |
| :--------: | :------: | :----: | :---------------------------------------------------------------------------------------------: | :---------------------------------------------------: |
|   config   | 请求配置 | Object |                 {api: '', method: 'get', params: {}, userProcess: data => data}                 | **`config`&#124;`initData`必传一项, config.api 必传** |
|  initData  |   数据   | array  |                                               []                                                |         **`config`&#124;`initData`必传一项**          |
|   width    |   宽度   | number |                                               800                                               |
|  eachline  | 每行数量 | number |                                                2                                                |
|   header   |   标题   | string |                                                -                                                |                不传值或传空值时不展示                 |
|   footer   |   页尾   | string |                                                -                                                |                不传值或传空值时不展示                 |
| titleStyle | 标题样式 | Object | {height: '50px', lineHeight: '50px', fontSize: '32px', fontWeight: 'bold', textAlign: 'center'} |

<!--
width = "800",
eachline = 4,
header = "标题",
footer = "",
titleStyle = {
    height: '50px',
    lineHeight: '50px',
    fontSize: '32px',
    fontWeight: 'bold',
    textAlign: 'center',
}
 -->
