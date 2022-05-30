# 排行榜

## 基本介绍

排行榜组件

## Example&Format

#### 接口传值

```javascript
<RankingList config={{ api: '/api/commonHeader', userProcess: (data) => data.list }}></RankingList>
// 返回类型
// {
//     list: [
//         {
//         "id": key 值,
//         "text": 显示文本,
//         "url": 跳转链接,
//         }
//     ]
// }
```

#### 数据传值

```javascript
const data = [
    {
        id: '1111',
        text: '矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。',
        url: 'tn3270://vpdp.sl/oihmykx',
    },
    {
        id: '2111',
        text: '矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。',
        url: 'tn3270://vpdp.sl/oihmykx',
    },
    {
        id: '51972',
        text: '矿方根候劳极造级始至京任音候市何养住电下理议红见法必队每商矿保变例平往正目压备拉学包统率同称活时文马好人识心认子物构每法特委所群名代思况家选道热质制约北经务完深铁低包自委并义话细越听习件党社声东连到小子海商克更至土识色照进都接话和验己从院统派商可空写例。',
        url: 'tn3270://vpdp.sl/oihmykx',
    },
];
<RankingList initData={data}></RankingList>;
```

#### 显示标题页尾

```javascript
<RankingList header={'标题'} config={{ api: '/api/commonHeader', userProcess: (data) => data.list }}></RankingList>
```

```javascript
<RankingList footer={'页尾'} config={{ api: '/api/commonHeader', userProcess: (data) => data.list }}></RankingList>
```

#### 限制排行榜最大长度

```javascript
<RankingList maxLength={5} config={{ api: '/api/commonHeader', userProcess: (data) => data.list }}></RankingList>
```

## API

<!--
&#124;
-->

|   属性    |      说明      |  类型  |                             默认值                              |                         备注                          |
| :-------: | :------------: | :----: | :-------------------------------------------------------------: | :---------------------------------------------------: |
|  config   |    请求配置    | object | {api: '', method: 'get', params: {}, userProcess: data => data} | **`config`&#124;`initData`必传一项, config.api 必传** |
| initData  |      数据      | array  |                               []                                |         **`config`&#124;`initData`必传一项**          |
|   width   |      宽度      | number |                               250                               |
| maxLength | 排行榜最大长度 | number |                               10                                |
|  header   |      标题      | string |                                -                                |                     不为空则显示                      |
|  footer   |      页尾      | string |                                -                                |                     不为空则显示                      |
