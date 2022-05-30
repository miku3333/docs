# 缩放图片

## 基本介绍

悬浮时图片放大

## Example&Format

#### 设定图片 src

```javascript
<ScaleImage src={'http://dummyimage.com/800x450'}></ScaleImage>
```

#### 添加子元素

```javascript
<ScaleImage src={'http://dummyimage.com/800x450'}>
    <div>child</div>
</ScaleImage>
```

## API

<!--
&#124;
-->

|   属性    |   说明   |  类型  | 默认值 | 备注 |
| :-------: | :------: | :----: | :----: | :--: |
|    src    | 图片地址 | string |   -    |
|  height   |   高度   | string |  100%  |
|   width   |   宽度   | string |  100%  |
|   scale   | 缩放倍数 | number |   2    |
|   time    | 动画时间 | number |  0.5   |
|   style   |   样式   | string |   -    |
| className |   类名   | string |   -    |
