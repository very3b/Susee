# NAND与NOR的virtuoso仿真
## 一、NAND的仿真
### 1.搭建电路
 搭建NAND的电路,其中电源vdc=1.5v，负载cap的capacitance=100f，两输入端选用vpulse，其中V1和V2的参数如下：
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%871.png)
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%872.png)
 电路搭建如图所示：
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%873.png)

### 2.仿真设置
 check and save后，打开ADE L窗口，在analyses一栏中进行如下设置：
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%874.png)

### 3.设置输入输出
 点击ADE L窗口中的outputs→setup，添加两输入和输出端，分别命名为Vin1、vin2、vout，如图：
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%875.png)

### 4.运行仿真
 点击simulation→netlist and run，输出结果图后，右键→split current strip→trace，将三条曲线分开显示：
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%876.png)

## 二、NOR的仿真
### 1.设置
 NOR的仿真可参考NAND的仿真流程，其具体设置和仿真结果见下图：
#### vin1
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%877.png)
#### vin2
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%878.png)
#### 电路图
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%879.png)
#### 仿真结果
![Alt text](https://github.com/very3b/Susee/blob/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/NAND%E4%B8%8ENOR%E7%9A%84virtuoso%E4%BB%BF%E7%9C%9F/%E5%9B%BE%E7%89%8710.png)
