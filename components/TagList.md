# 标签列表

## 基本介绍

用于展示各种异色标签

## Example&Format

#### 接口传值

```javascript
<TagList config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TagList>
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
<TagList initData={data}></TagList>;
```

#### 添加标题

```javascript
<TagList title="title title" config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TagList>
```

#### 添加右侧按钮

```javascript
<TagList title="title title" rightButton={text: 'test', url: 'http://example.com'} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></TagList>
```

## API

<!--
&#124;
-->

|    属性     |   说明   |  类型  |                                             默认值                                              |                                          备注                                           |
| :---------: | :------: | :----: | :---------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------: |
|   config    | 请求配置 | object |                 {api: '', method: 'get', params: {}, userProcess: data => data}                 |                  **`config`&#124;`initData`必传一项, config.api 必传**                  |
|  initData   |   数据   | array  |                                               []                                                |                          **`config`&#124;`initData`必传一项**                           |
|    width    |   宽度   | number |                                               800                                               |
|  eachline   | 每行数量 | number |                                                2                                                |
|    title    |   标题   | string |                                                -                                                |                                 不传值或传空值时不展示                                  |
| titleStyle  | 标题样式 | object | {height: '50px', lineHeight: '50px', fontSize: '32px', fontWeight: 'bold', textAlign: 'center'} |
| itemHeight  | 标签高度 | number |                                               50                                                |
|  itemStyle  | 标签样式 | object |                                      {textAlign: 'center'}                                      |
| firstColor  |   主色   | string |                                             #f5f5f5                                             |
| secondColor |   副色   | string |                                             #ffffff                                             |
| hoverColor  |  悬浮色  | string |                                             #edac96                                             |
| rightButton | 右侧按钮 | object |                                                -                                                | 需要标题存在,{text: 'test', url: 'http://example.com'}, text 代表名称, url 代表跳转地址 |
