# 走马灯

## 基本介绍

轮播图组件

## Example&Format

#### 接口传值

```javascript
<Carousel config={{ api: '/api/articleList', userProcess: (data) => data.list }}></Carousel>
// 返回类型
// {
//     "list": [
//         {
//             "id": key值,
//             "imgUrl": 图片地址,
//             "url", 跳转链接,
//             "title": 文字信息
//         }
//     ]
// }
```

#### 数据传值

```javascript
const data = [
    {
        id: 13006,
        imgUrl: 'http://dummyimage.com/800x450',
        title: '部必清体间新清影节管着立查。',
        url: 'mailto://dtwdxnyz.com/esugqoq',
    },
    {
        id: 12963,
        imgUrl: 'http://dummyimage.com/800x450',
        title: '对过离立气着工南候声感机。',
        url: 'http://ggoparh.re/tpjekbe',
    },
    {
        id: 14262,
        imgUrl: 'http://dummyimage.com/800x450',
        title: '节办龙去这声和办量合马影术场。',
        url: 'mid://lkae.bw/wmb',
    },
]
<Carousel initData={data}></Carousel>;
```

#### 展示文字(默认)

```javascript
<Carousel config={{ api: '/api/articleList', userProcess: (data) => data.list }}></Carousel>
```

#### 展示图片

```javascript
<Carousel config={{ api: '/api/articleList', userProcess: (data) => data.list }}></Carousel>
```

#### 渐显

```javascript
<Carousel config={{ api: '/api/articleList', userProcess: (data) => data.list }}></Carousel>
```

## API

|      属性      |                                说明                                 |                 类型                  |                                        默认值                                        |                         备注                          |
| :------------: | :-----------------------------------------------------------------: | :-----------------------------------: | :----------------------------------------------------------------------------------: | :---------------------------------------------------: |
|     config     |                              请求配置                               |                object                 |           {api: '', method: 'get', params: {}, userProcess: data => data}            | **`config`&#124;`initData`必传一项, config.api 必传** |
|    initData    |                                数据                                 |                 array                 |                                          []                                          |         **`config`&#124;`initData`必传一项**          |
| showSideButton |                            展示侧边按钮                             |                boolean                |                                         true                                         |
|     width      |                                宽度                                 |                number                 |                                         1000                                         |                                                       |
|     height     |                                高度                                 |                number                 |                                         200                                          |                                                       |
|      time      |                  自动播放间隔, 当为 0 时不自动播放                  |                number                 |                                          0                                           |                                                       |
|      type      |                             轮播图类型                              |         `text` &#124; `image`         |                                        `text`                                        |                                                       |
|    autoplay    |                            是否自动播放                             |                boolean                |                                        flase                                         |                                                       |
|  contentStyle  |                              内容样式                               |                Object                 | {color: '#fff', textAlign: 'center', background: '#364d79', verticalAlign: 'middle'} |                                                       |
|  dotPosition   |         面板指示点位置，可选 `top` `bottom` `left` `right`          |                string                 |                                       `bottom`                                       |                                                       |
|      dots      | 是否显示面板指示点，如果为 `object` 则同时可以指定 `dotsClass` 或者 | boolean &#124; { className?: string } |                                         true                                         |                                                       |
|     easing     |                              动画效果                               |                string                 |                                       `linear`                                       |                                                       |
|     effect     |                            动画效果函数                             |        `scrollx` &#124; `fade`        |                                      `scrollx`                                       |                                                       |
|  afterChange   |                           切换面板的回调                            |           function(current)           |                                          -                                           |                                                       |
|  beforeChange  |                           切换面板的回调                            |          function(from, to)           |                                          -                                           |                                                       |
