# 导航栏

## 基本介绍

通用导航栏

## Example&Format

#### 接口传值

```javascript
<CommonHeader config={{ api: '/api/commonHeader', userProcess: (data) => data.list }}></CommonHeader>
// 返回类型
// 树状结构
// {
//     list: [
//         {
//             "key": key值,
//             "title": 名称,
//             "url": 跳转链接,
//             "disabled": 是否关闭,
//             "type": 节点类型
//             "children": [
//                 {
//                     "key": key值,
//                     "title": 名称,
//                     "url": 跳转链接,
//                     "disabled": 是否关闭,
//                     "children": [

//                     ]
//                 }
//             ]
//         }
//     ]
// }
```

#### 数据传值

```javascript
const data = [
    {key: '1', title: '首页'},
    {key: '2', title: '个人中心', disabled: true},
    {
        key: '3', title: '列表', type: 'menu', disabled: false,
        children: [
            {
                title: '充值',
                data: [
                    {key: '4', title: '商城'},
                    {key: '5', title: '支付宝', disabled: true},
                    {key: '6', title: '微信', disabled: false},
                ]
            },
            {
                title: '反馈',
                data: [
                    {key: '7', title: '客服'},
                    {key: '8', title: '邮件', disabled: true},
                    {key: '9', title: '电话', disabled: true},
                ]
            },
            {
                title: '加入我们',
                data: [
                    {key: '11', title: '招聘'},
                ]
            },
        ]
    },
    {key: '12', title: '友情链接', type:'link', url:'https://www.baidu.com'},
]
<CommonHeader initData={data}></CommonHeader>
```

## API

|   属性   |   说明   |  类型  |                             默认值                              |                         备注                          |
| :------: | :------: | :----: | :-------------------------------------------------------------: | :---------------------------------------------------: |
|  config  | 请求配置 | Object | {api: '', method: 'get', params: {}, userProcess: data => data} | **`config`&#124;`initData`必传一项, config.api 必传** |
| initData |   数据   | array  |                               []                                |         **`config`&#124;`initData`必传一项**          |
|  height  |   高度   | number |                               50                                |                                                       |
