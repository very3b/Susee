# 一、RLC电路仿真
## 搭建电路，如图所示：
![RLC](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/RLC%E7%94%B5%E8%B7%AF.png)
![test bench](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E6%B5%8B%E8%AF%95%E7%94%B5%E8%B7%AF.png)

## 设置仿真参数，如下：
![1](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/10-10-0-0.png)
![2](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/100-1-0-0.png)
### 上图1和图2的入射波振幅不同，但仿真结果一致，不知道是不是此RLC电路的特殊性。

## 仿真结果：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.png)

# 二、3R电路的S参数仿真及验证
##搭建电路：
![3R](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R.png)
![3R_tb](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R_tb.png)

## 仿真结果：
![tb](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R_tb_%E7%BB%93%E6%9E%9C.png)

## 计算结果：
Z参数的计算：$$Z_11=Z_A+Z_C=2 K Ohm
Z_12=Z_C=1 K Ohm
Z_21=Z_C=1 K Ohm
Z_22=Z_B+Z_C=2 K Ohm
$$

S参数的计算：$$△Z=（Z_11+Z_0）（Z_22+Z_0）-Z_12Z_21=2050^2-1000^2
S_11=\frac{3000000-2500}{2050^2-1000000}=0.93598
S_22=S_11=0.93598
S_12=Z_21=\frac{2Z_12Z_0}{△Z}=0.0312256
$$
计算结果与仿真结果相符。