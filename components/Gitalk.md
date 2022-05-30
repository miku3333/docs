# 评论区

## 基本介绍

评论区, 需要特殊配置, [详情参考](https://segmentfault.com/a/1190000018072952)

## Example&Format

```javascript
<GitalkComponent
    options={{
        clientID: '739e7694f0010709d990', // GitHub Application Client ID
        clientSecret: 'd57f65922295a2045fd65e59f7a32a855ac1f0a0', // GitHub Application Client Secret
        repo: 'talk', // 存放评论的仓库
        owner: 'miku3333', // 仓库的创建者，
        admin: ['miku3333'], // 如果仓库有多个人可以操作，那么在这里以数组形式写出
    }}
/>
```

## API

<!--
&#124;
-->

|  属性   |    说明     |  类型  | 默认值 |                          备注                           |
| :-----: | :---------: | :----: | :----: | :-----------------------------------------------------: |
| options | gitalk 配置 | object |   -    | [详情参考](https://segmentfault.com/a/1190000018072952) |
