# 2.5.0

完善撤回功能

# 2.4.5

修复撤回功能bug

# 2.4.4

优化二级颜色选择器交互逻辑

# 2.4.3

修复save()导出base64无效问题

# 2.4.2

registerTool函数更名为toolRegister，但保持了registerTool的可用性

修复ie只支持整数rgb的bug

修复ie自定义事件无法重复init引发的bug

# 2.4.1

修复pc端滑块失效问题

# 2.4.0

为颜色选择器提供了二级选择，现在所有颜色可以往黑度或白度偏移

# 2.3.5

发布至npm

# 2.3.3

更新文档
更新customTool demo

# 2.3.2

延迟resize，防止频繁触发resize导致canvas多次重绘

# 2.3

由于直接暴露了frontCanvasCtx和mainCanvasCtx,frontCanvasShow控制将变得无意义，所以删除了此选项且删除了mainCanvas的事件监听，frontCanvas将默认显示且无法关闭(非破坏性更新，对工具无影响)

新增接口函数：mousemoveFn 为类似橡皮工具绘制鼠标移动标识 不同于drawMoveFn接口只在drawStartFn触发后触发 当检测到此函数时在画布层隐藏鼠标光标

为笔刷，直线，橡皮增加了鼠标移动标识，pc上将更容易分辨笔刷和橡皮的大小(移动端后续考虑支持touch范围 省去手动调节大小)

当没有可用撤销时撤销按钮将变灰

# 2.2

新增多边形工具

# 2.1

新增直线工具

完善自定义工具相关文档

# 2.0.1

更换了橡皮擦逻辑
由原来的圆形分割为多个矩形使用clearReac擦除改为使用canvas合成接口 globalCompositeOperation = 'destination-out' 解决了移动端橡皮擦性能问题

ios点击无法画线问题 (原因为ios lineTo等于moveTo时不进行绘制)

# 2.0

重构代码

全新的工具引入方式 更好的组件化

同时兼容触摸事件 鼠标事件
统一了鼠标触发事件响应方式完全等于触摸事件暴露给绘制工具

支持自定义绘制工具

更好的绘制性能

新增全局撤销功能

颜色选择器 大小选择器解耦组件化

# 1.0.1

修改样式

# 1.0

canvas 画板

画笔工具 支持大小、颜色自定义 橡皮工具 支持大小自定义