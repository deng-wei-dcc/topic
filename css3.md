##### 背景填充位置 backgroun-origin
    + border-box    从边框位置开始填充
    + padding-box   从内边距位置开始填充
    + content-box   从内容开始填充

##### 背景定位 background-position
    + x(left | center | right) y(top | center | bottom)
    + x% y%
    + x(px) y(px)
##### 背景裁剪 background-clip
    + border-box
    + padding-box
    + content-box

##### 背景渐变
    + linear-gradient  线性渐变
        tips：可对角渐变
              重复渐变 - repeat-linear-gradient
        type.1：方向(默认上-->下),(颜色 [占比[范围]],)...
        type.2：角度(角度,(颜色 [占比[范围]],)...)
    + radial-gradient  径向渐变
        + 中心点
        + 形状(圆/椭圆)
        + 大小
            + closest-side
            + farthest-side
            + closest-corner
            + farthest-corner
        + (颜色 [占比[范围]],)...

##### 文本效果
    tips：结合overflow、text-overflow、white-space可实现文本溢出用省略号代替
    + text-shadow       文本阴影
        水平位移 垂直位移 模糊度 颜色
    + text-overflow
        + clip          裁剪文本
        + ellipsis      溢出用省略号代替
        + string(自定义)
    + white-space
        + nowrap        文本不换行