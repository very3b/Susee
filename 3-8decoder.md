# 3-8译码器的仿真
## 一、原理：所谓译码器就是将一组输入码转换成另一组输出码的逻辑电路。对于3-8译码器，以74--138为例，其有三个使能输入端，一个高电平输入有效，其余两个低电平输入有效；8个输出端，均是低电平输出有效。其真值表如下：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/%E7%9C%9F%E5%80%BC%E8%A1%A8.jpg)

## 二、搭建3-8译码器器件电路，其中电源vdc=1.2v，反相器和nand的p、pb端接vdd，G、Gb端接gnd，如下图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/%E7%94%B5%E8%B7%AF%E5%9B%BE.png)

## 三、搭建3-8译码器的仿真电路，输出端接cap=100pf的负载。输入端高电平是1.2v，低电平0v。各输入端的电源参数如下图所示(一般电流源都在analogLib库中调用)：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/A.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/B.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/C.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/G1.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/G2A.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/G2B.png)

## 四、设置仿真参数，在outputs中选择所有输入输出端口，如图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/%E5%8F%82%E6%95%B0.png)

## 五、运行仿真，结果如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/3-8decoder-tb/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.png)