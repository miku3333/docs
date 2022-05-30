# 个人信息面板

## 基本介绍

个人信息面板

## Example&Format

#### 接口传值

```javascript
<InfoWrap config={{ api: '/api/userInfo' }}></InfoWrap>
// 返回类型
// {
//     "imgUrl": 头像 url 地址,
//     "name": 姓名,
//     "profile": 个人简写,
//     "tagList": [{
//     "name": 标签名,
//     "num|1-100": 标签数字,
//     "url": 标签跳转链接,
//     }],
//     "githubUrl": github 链接(以下链接不为空则显示图标),
//     "weiboUrl": 微博链接,
//     "twitterUrl": twitter 链接,
//     "wechatUrl": 微信链接,
//     "qqUrl": qq 链接,
//     "facebookUrl": facebook 链接,
//     "instagramUrl": instagram 链接,
//     "zhihuUrl": 知乎链接,
// }
```

#### 数据传值

```javascript
const data = {
    userId: 10120,
    imgUrl: 'http://dummyimage.com/400x400',
    name: '周桂英',
    profile: '相他打展果红任压命委省可等须金风许商。',
    tagList: [
        {
            name: '法代法',
            url: 'mailto://ungn.fr/staxfatp',
        },
        {
            name: '是农存',
            url: 'cid://yceqlsksqp.gf/hbyvks',
        },
        {
            name: '走改名',
            url: 'nntp://ydiknha.fk/jkpdir',
        },
        {
            name: '类深',
            url: 'tn3270://vroyi.sl/poh',
        },
        {
            name: '置比',
            url: 'cid://nykanwdp.io/emzmg',
        },
    ],
    githubUrl: 'https://github.com/lerrua/remote-jobs-brazil',
    weiboUrl: 'https://baidu.com',
    zhihuUrl: 'https://zhihu.com',
};
<InfoWrap initData={data}></InfoWrap>;
```

## API

<!--
&#124;
-->

|    属性    |   说明   |  类型  |                             默认值                              |                         备注                          |
| :--------: | :------: | :----: | :-------------------------------------------------------------: | :---------------------------------------------------: |
|   config   | 请求配置 | object | {api: '', method: 'get', params: {}, userProcess: data => data} | **`config`&#124;`initData`必传一项, config.api 必传** |
|  initData  |   数据   | object |                               {}                                |         **`config`&#124;`initData`必传一项**          |
| avatarSize | 头像大小 | number |                               200                               |
|   width    |   宽度   | number |                               500                               |
|   height   |   高度   | number |                              1000                               |
