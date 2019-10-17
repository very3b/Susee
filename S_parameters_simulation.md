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
## 搭建电路：
![3R](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R.png)
![3R_tb](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R_tb.png)

## 仿真结果：
![tb](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/3R_tb_%E7%BB%93%E6%9E%9C.png)

## 计算结果：
Z参数的计算：
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn.gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(1).gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(2).gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(3).gif)  


S参数的计算：
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(4).gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(5).gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(6).gif)  
![](https://github.com/dailiuyao/markdown-photos/blob/master/RLC_S_simulation/%E5%85%AC%E5%BC%8F/CodeCogsEqn%20(7).gif)  
计算结果与仿真结果相符。