# css3-Radar（css3 雷达效果）

## 效果展示

 ![image](https://github.com/jaikensai888/css3-Radar/image/raderlive.gif)

## 介绍

    简单的雷达图扫描图形，模拟了目标点，目标掉点的运行轨迹在y=x的直线上随机运动；

## 主要技术总结

### Gradients(渐变)

> background 下可以使用多个渐变，使用,隔开

- Linear-Gradients(线性渐变)

>该实例使用在（扫描器）

```用法总结
Linear-Gradients(agree,firstColor,secondColor，...moreColor)

Linear-Gradients（45deg，rgba（红色，绿色，蓝色，透明率）20%，rgba（红色，绿色，蓝色，透明率）80%）

- 最后百分号为从上到下，纯色的开始的位置；

- 还有一组repeat的用法就是重复使用

```

- Radial-Gradient（径向渐变）

>该实例使用在画雷达图

```用法总结

background: radial-gradient(center, shape size, start-color, ..., last-color);

center 中心点
shape 形状，circle，ellipse
size：形状，系统有固定；

```

### Animation动画

> 该实例使用在（扫描旋转，目标点消失动画）

- @keyFrames 声明动画

```用法总结
1.开始结束
from{
cssStyle
}
to{
cssStyle
}
2.百分比进程
10%{
}
20%{
}

```

- 引用

```用法总结
在css中直接使用Animation:动画名称，持续时间，是否无线循环；
其他Animation的参数全部都是用来调整时间的（参考文档）；
```

### transform（变形）

> 该实例使用在扫描图层旋转

- 引用

```旋转用法总结
1.在css中直接使用
2.transform-origin：bottom right （变形依赖的中心店）
3.transform：rotate（30deg） 旋转角度
```