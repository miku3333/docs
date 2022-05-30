# 留言板

## 基本介绍

滚动加载无限长留言板

## Example&Format

#### 接口传值

```javascript
<MessageBoard config={{ api: '/api/articleList', userProcess: (data) => data.list }}></MessageBoard>
// 返回结构
// {
//     list: [
//         {
//             id: key值,
//             url: 跳转链接,
//             deg: 旋转角度(若不传值, 则设定随机角度),
//             color: 背景颜色(若不传值, 则设定随机颜色),
//             datetime: 日期,
//             description: 详细信息
//         }
//     ]
// }
```

#### 数据传值

```javascript
const data = [
    {
        "id": 15386,
        "datetime": "1992-01-22  01:08:13",
        "description": "矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。",
        "url": "tn3270://vpdp.sl/oihmykx",
    },
    {
        "id": 15386,
        "datetime": "1992-01-22  01:08:13",
        "description": "矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。",
        "url": "tn3270://vpdp.sl/oihmykx",
        "color": "#CCFFFF",
    },
    {
        "id": 15386,
        "datetime": "1992-01-22  01:08:13",
        "description": "矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。",
        "url": "tn3270://vpdp.sl/oihmykx",
        "color": "#CCFFFF",
        "deg": 0
    }
]
<MessageBoard initData={data}></MessageBoard>
```

#### 不显示加载信息

```javascript
<MessageBoard showToast={false} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></MessageBoard>
```

#### 设定随机角度与随机颜色

```javascript
<MessageBoard degRange={15} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></MessageBoard>
```

```javascript
<MessageBoard colorList={['ffffff', 'ff0000']} config={{ api: '/api/articleList', userProcess: (data) => data.list }}></MessageBoard>
```

## API

<!--
&#124;
-->

|      属性       |     说明     |  类型   |                             默认值                              |                         备注                          |
| :-------------: | :----------: | :-----: | :-------------------------------------------------------------: | :---------------------------------------------------: |
|     config      |   请求配置   | object  | {api: '', method: 'get', params: {}, userProcess: data => data} | **`config`&#124;`initData`必传一项, config.api 必传** |
|    initData     |     数据     |  array  |                               []                                |         **`config`&#124;`initData`必传一项**          |
|    showToast    | 显示加载信息 | boolean |                              true                               |
|      toast      |   提示信息   | string  |                      加载了${number}篇文章                      |            ${number}代表请求返回数组的长度            |
| containerHeight |   容器高度   | number  |                               550                               |
|    eachLine     |   每行数量   | number  |                                4                                |
|    itemSize     |   元素大小   | number  |                               200                               |
|     margin      |   边框大小   | number  |                               36                                |
|      scale      |   缩放倍数   | number  |                               1.2                               |
|    colorList    | 随机颜色列表 |  array  |          ['#F3F3F3', '#FFFFCC', '#FFCCFF', '#CCFFFF']           |
|    degRange     | 随机旋转角度 | number  |                               30                                |
