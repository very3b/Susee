## 问题描述：Z0=50Ω，f=5000MHz，Zl=25+j75Ω。求串联支节l1和l2
## （1）设定起始点，点击下图中Toolbox中的DATAPOINT，选择Keyboard，分别设置实部虚部为25和75。(如果有频率要求，必须先设定工作频率)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/smith/1.png)

## (2) 由于支节处Zin的实部为50，即通过原点的电阻圆。所以首先从负载向电源旋转(顺时针串联线)，到此单位圆的交点的电长度即为l1的长度。由于交点有两个，以上面的那个为例。读出l1=0.031λ。读出该点的输入阻抗为51.097+j113.018。
![2](https://github.com/dailiuyao/markdown-photos/blob/master/smith/2.png)
![3](https://github.com/dailiuyao/markdown-photos/blob/master/smith/3.png)

## (3) 求支节长度l2。新建一个圆图。由于短路支节的负载为0，因此设定起始点为0。

## (4) 由于支节点后面的输入阻抗为51.097+j113.018，并且支节是串联的。因为为了达到匹配(50)，支节的阻抗应为-j113.018。从起始点向电源(顺时针)串联线同时读数，当输入阻抗为j113.018时，点击鼠标左键。读数l2=0.184λ。
![4](https://github.com/dailiuyao/markdown-photos/blob/master/smith/4.png)