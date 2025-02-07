# RenderTransforms和RenderTransformOrigin

在WPF和Avalonia中，RenderTransformOrigin是不同的：如果应用了`RenderTransform`，请注意Avalonia中RenderTransformOrigin的默认值是`RelativePoint.Center`，而在WPF中默认值是`RelativePoint.TopLeft`\(0, 0\)。在像Viewbox这样的控件中，相同的代码将导致不同的渲染行为：

**在WPF中：** ![WPF](https://files.gitter.im/AvaloniaUI/Avalonia/cDrM/image.png)

**在Avalonia中：** ![Avalonia](https://files.gitter.im/AvaloniaUI/Avalonia/KGk7/image.png)

在AvaloniaUI中，要获得相同的缩放变换，我们应该指定`RenderTransformOrigin`为`Visual`的`TopLeft`部分。

