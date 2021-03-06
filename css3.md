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

####  转换属性
    + transform         应用2d、3d转换
    + transform-style   所有子元素在3d中呈现(设置在父级中)
        + flat          子元素不保留3d位置
        + preserve      子元素保留3d位置
    + transform-origin  改变转换点
    + perspective       查看3d的视距
        tips：  
            该属性给父级设置时，是以父级的某一个点位视点的，查看子元素时样式是不一样的（多个子元素）
            给每个子元素设置transform:perspevtive(800px)时,会以元素自身的某个点作为视点，呈现出来的样式是一样的


##### 2D转换(transform)
    + translate     从当前元素位置移动(如果是%,是根据自身来计算的)
    + translateX    x轴移动
    + translateY    y轴移动

    + scale         缩放元素大小，默认为1不缩放
    + scaleX        x轴缩放
    + scaleY        y轴缩放

    + rotate        旋转元素（可+-）

    + skew          元素倾斜度
    + skewX( )      表示只在X轴(水平方向)倾斜。
    + skewY( )      表示只在Y轴(垂直方向)倾斜。

##### 3D转换
    translateZ      z轴移动
    translate3d(x,y,z)

    + scaleZ        z轴缩放
    + scale3d()

    + rotateX       x轴旋转
    + rotateY       y轴旋转
    + rotateZ       z轴旋转
    + rotate3d()

##### 过渡
    + transition-property           指定要过度的css属性
        + all                       所有属性应用过度(不写默认全部)
        + none                      没有属性应用
        + 属性名                     多个用逗号隔开
    + transition-duration           设置过度需要的时间
    + transition-timing-function    设置过度时运动速度
        + linear                    匀速运动         
        + ease                      慢-->快-->慢
        + ease-in                   以慢速开始运动
        + ease-out                  以慢速结束
        + ease-in-out               以慢速开始和结束
    + transiton-delay               延迟多少秒执行
    + transiton                     复合属性
        属性、过度时间、运动速度、延迟时间

##### 动画 
    + @keyframes        定义动画
        格式： 
            @keyframes 名称 {
                form{} 或 0%
                          ...
                to{}   或 100%
            }
    + animation         将动画绑定到选择器(复合属性)
        动画名称、周期运动时间、速度、延迟执行时间、动画执行次数、下个周期是否逆向执行、动画运行状态(暂停/运行)
    
    + animation-name                动画名称
    + animation-duration            运动需要的时间

    + animation-timimg-function     运动速度
        + linear                    匀速运动         
        + ease                      慢-->快-->慢
        + ease-in                   以慢速开始运动
        + ease-out                  以慢速结束
        + ease-in-out               以慢速开始和结束

    + animation-delay               延迟执行

    + animation-iteration-count     执行次数
        + infinite                  无限次播放
        + 自定义次数n

    + animation-direction           下个周期执行方向
        + reverse                   反向执行
        + alternate                 奇数(正向)/偶数(反向)
        + alternate-reverse         奇数(反向)/偶数(正向)

    + animation-play-state          执行状态
        + paused                    暂停
        + running                   运行

##### 盒模型
    + 普通盒模型 - 默认
        box-sizing: content-box;
        元素大小 = 设置的宽高 + bordr + padding
    + 怪异盒模型
        box-sizing: border-box;
        元素大小 = 设置的宽高

##### 弹性盒模型flex
    + display           开启弹性盒模型
        flex 或 inline-flex
    + flex-direction    