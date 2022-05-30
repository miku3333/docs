# 日历

## 基本介绍

可在日历中加入每日事件, 也可单独展示日历组件

## Example&Format

```javascript
<Calendar monthConfig={{ api: '/api/calendar/month', userProcess: data => data.days }}></Calendar>
// monthConfig返回类型
// {
//     "days|-31": [{
//         "task": [{
//             "type": "warning" || "success" || "error",
//             "content": 内容
//         }]
//     }]
// }

// yearConfig返回类型
// {
//     "months|12": [{
//         "task": [{
//             "type": "warning" || "success" || "error",
//             "content": 内容
//         }]
//     }]
// }
```

## API

|        属性         |                                                       说明                                                        |                                       类型                                       |                                                    默认值                                                     |             备注             |
| :-----------------: | :---------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------: | :--------------------------: |
|     monthConfig     |                                                   月份请求配置                                                    |                                      object                                      |                        {api: '', method: 'get', params: {}, userProcess: data => data}                        | **若传值则 config.api 必传** |
|     yearConfig      |                                                   年份请求配置                                                    |                                      object                                      |                        {api: '', method: 'get', params: {}, userProcess: data => data}                        | **若传值则 config.api 必传** |
|   dateCellRender    |                                  自定义渲染日期单元格，返回内容会被追加到单元格                                   |                        function(date: moment): ReactNode                         |                                                       -                                                       |                              |
| dateFullCellRender  |                                     自定义渲染日期单元格，返回内容覆盖单元格                                      |                        function(date: moment): ReactNode                         |                                                       -                                                       |                              |
|    defaultValue     |                                                  默认展示的日期                                                   |                          [moment](http://momentjs.com/)                          |                                                       -                                                       |                              |
|    disabledDate     | 不可选择的日期，参数为当前 value，注意使用时[不要直接修改](https://github.com/ant-design/ant-design/issues/30987) |                         (currentDate: moment) => boolean                         |                                                       -                                                       |
|     fullscreen      |                                                   是否全屏显示                                                    |                                     boolean                                      |                                                     true                                                      |                              |
|    headerRender     |                                                  自定义头部内容                                                   | function(object:{value: moment, type: string, onChange: f(), onTypeChange: f()}) |                                                       -                                                       |                              |
|       locale        |                                                    国际化配置                                                     |                                      object                                      | [(默认配置)](https://github.com/ant-design/ant-design/blob/master/components/date-picker/locale/example.json) |                              |
|        mode         |                                                     初始模式                                                      |                              `month` &#124; `year`                               |                                                    `month`                                                    |
|   monthCellRender   |                                   自定义渲染月单元格，返回内容会被追加到单元格                                    |                        function(date: moment): ReactNode                         |                                                       -                                                       |                              |
| monthFullCellRender |                                      自定义渲染月单元格，返回内容覆盖单元格                                       |                        function(date: moment): ReactNode                         |                                                       -                                                       |                              |
|     validRange      |                                                设置可以显示的日期                                                 |         [[moment](http://momentjs.com/), [moment](http://momentjs.com/)]         |                                                       -                                                       |                              |
|        value        |                                                     展示日期                                                      |                          [moment](http://momentjs.com/)                          |                                                       -                                                       |                              |
|      onChange       |                                                   日期变化回调                                                    |                             function(date: moment）                              |                                                       -                                                       |                              |
|    onPanelChange    |                                                 日期面板变化回调                                                  |                       function(date: moment, mode: string)                       |                                                       -                                                       |                              |
|      onSelect       |                                                 点击选择日期回调                                                  |                             function(date: moment）                              |                                                       -                                                       |                              |
