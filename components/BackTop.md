# 置顶按钮

## 基本介绍

同[antd 置顶按钮](https://ant.design/components/back-top-cn/), 返回顶部

## Example&Format

```javascript
<BackTop></BackTop>
```

## API

|       属性       |                             说明                              |       类型        |    默认值    | 备注 |
| :--------------: | :-----------------------------------------------------------: | :---------------: | :----------: | :--: |
|     duration     |                    回到顶部所需时间（ms）                     |      number       |     450      |
|      target      | 设置需要监听其滚动事件的元素，值为一个返回对应 DOM 元素的函数 | () => HTMLElement | () => window |
| visibilityHeight |              滚动高度达到此参数值才出现 BackTop               |      number       |     400      |
|     onClick      |                      点击按钮的回调函数                       |     function      |      -       |
