# 翻转

## 基本介绍

实现两组件之间翻转

## Example&Format

```javascript
// 使用时使用两个div标签包裹旋转前后元素
<Flip>
    <div>
        <div style={{ width: '100%', height: '100%', background: '#ffffcc' }}>222</div>
    </div>
    <div style={{ width: '100%', height: '100%' }}>
        <div style={{ width: '100%', height: '100%', background: '#ffccff' }}>33</div>
    </div>
</Flip>
```

#### 触碰消失效果

```javascript
<Flip>
    <div>
        <div style={{ width: '100%', height: '100%', background: '#ffffcc' }}>222</div>
    </div>
</Flip>
```

## API

<!--
&#124;
-->

|   属性    |   说明   |                   类型                    | 默认值 | 备注 |
| :-------: | :------: | :---------------------------------------: | :----: | :--: |
|   width   |   宽度   |                  number                   |  400   |
|  height   |   高度   |                  number                   |  400   |
| direction |   方向   | `up`&#124;`down`&#124;`right`&#124;`left` |   up   |
|    deg    | 旋转角度 |                  number                   |   90   |
| duration  | 动画时间 |                  number                   |  0.5   |
|           |          |                                           |        |
