## 安装

#### 使用npm安装

`npm install blog-component`

## 使用

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import { ScaleImage } from "blog-component";
ReactDOM.render(
    <React.StrictMode>
        <ScaleImage src={'http://dummyimage.com/800x450'}></ScaleImage>
    </React.StrictMode>,
    document.getElementById('root')
);
```



