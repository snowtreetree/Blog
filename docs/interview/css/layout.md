# 圣杯布局&双飞翼布局

三栏布局，两边盒子固定宽度，中间自适应。

圣杯布局在两边的盒子较大时，会出现布局乱掉的问题。双飞翼解决了圣杯布局的这个问题。

## 区别

- 圣杯布局是通过父容器的的内边距实现，双飞翼通过margin实现。
- 双飞翼布局给中间的盒子增加了`子盒子`。
- 双飞翼布局不用设置相对布局，以及left/right

## 圣杯布局实现

- float+position
- flex
- calc
