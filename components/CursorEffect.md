# 鼠标特效

## 基本介绍

点击或移动鼠标时触发特效

## Example&Format

#### 绑定指定区域

```javascript
<div id='content'></div>
<CursorEffect element={document.querySelector('content')}></CursorEffect>
```

#### 气泡特效

```javascript
<CursorEffect type="bubble"></CursorEffect>
```

#### emoji 特效

```javascript
<CursorEffect type="emoji"></CursorEffect>
```

#### 尘埃特效

```javascript
<CursorEffect type="dust"></CursorEffect>
```

#### 拖影特效

```javascript
<CursorEffect type="ghost"></CursorEffect>
```

#### 雪花特效

```javascript
<CursorEffect type="snow"></CursorEffect>
```

#### 弹性特效

```javascript
<CursorEffect type="springy"></CursorEffect>
```

#### 点击时触发

```javascript
<CursorEffect trigger="click"></CursorEffect>
```

#### 移动时触发

```javascript
<CursorEffect trigger="move"></CursorEffect>
```

#### 同时触发

```javascript
<CursorEffect trigger="both"></CursorEffect>
```

## API

|  属性   |   说明   |                                   类型                                    |              默认值               |                          备注                          |
| :-----: | :------: | :-----------------------------------------------------------------------: | :-------------------------------: | :----------------------------------------------------: |
| element | 绑定节点 |                             () => HTMLElement                             |           () => window            |
|  type   |   种类   | `bubble`&#124;`emoji`&#124;`dust`&#124;`ghost`&#124;`snow`&#124;`springy` |              `snow`               |
| trigger |  触发器  |                      `click`&#124;`move`&#124;`both`                      |              `click`              | type 为`ghost`&#124;`springy`不支持`click`&#124;`both` |
| number  | 特效数量 |                                   array                                   |              [3, 5]               |          index0 代表最小值, index1 代表最大值          |
|  emoji  |  emoji   |                                   array                                   |     ["😀", "😂", "😆", "😊"]      |          type 为`emoji`&#124;`springy`时使用           |
| colors  | 颜色种类 |                                   array                                   | ["#D61C59", "#E7D84B", "#1B8798"] |                  type 为`dust`时使用                   |
