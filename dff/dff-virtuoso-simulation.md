# S-R latch,flip-flop的原理图仿真
## A、仿真范围
### S-R latch 意为锁存器，与非门的锁存器是低电平改变输出状态，即若低电平在s端，则锁存器的次态均为1，若低电平在r端，则锁存器的次态均为0。
### 触发器有同步式SR触发器和D类触发器，D类简称DFF，其分为同步式、主从式等。在这里我们做同步式和主从式的仿真。

## B、仿真步骤
### 一、SR锁存器
### 原理：SR锁存器分为与非门和或非门两种，这里采用与非门式，低电平输入有效，当s端输入低电平，r端输入高电平时次态为1；当r端输入低电平、s端输入高电平时次态为0；当两端均输入高电平时，输出端状态不变。
### 1、搭建SR锁存器电路，其中信号源S与R均选用vpwl，输出端负载选择100pf电容,电源电压VDC为1.2v。
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/SRlatch-tb/SRlatch%E7%94%B5%E8%B7%AF.jpg)

### 2、信号源设置
#### S端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/SRlatch-tb/SRlatchS%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

#### R端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/SRlatch-tb/SRlatchR%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

### 3、check and save后选择ADE L，在analysis中进行如下设置，然后选择S、R作为输入端，Q、QB作为输出端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/SRlatch-tb/SRlatch%E4%BB%BF%E7%9C%9F%E5%8F%82%E6%95%B0.jpg)

### 4、仿真结果
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/SRlatch-tb/SRlatch%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)
### 二、同步式SR触发器
### 原理：当同步式SR触发器的使能输入端为高电平，输入端S＋R=1时，输出端与输入端信号一致；当S=R=1时，输出端信号不变；当使能输入端为0时，触发器处于锁存状态，输出端信号不变。
### 1、搭建同步式SR触发器电路，信号源选择vpwl，电源电压1.2v,输出端负载选择100pf的电容。
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRff%E7%94%B5%E8%B7%AF.jpg)

### 2、信号源S、R、En的设置：
#### S端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRffS%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

#### R端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRffR%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

#### En端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRffEn%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

### 3、check and save后选择ADE L，在analysis中进行如下设置，然后选择S、R、En作为输入端，Q、Q'作为输出端：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRff%E4%BB%BF%E7%9C%9F%E5%8F%82%E6%95%B0.jpg)

### 4、仿真结果如下：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/synSRff-tb/synSRff%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.png)

### 三、同步式dff
### 原理：同步式dff的特点在于当En是高电平时，Q与D的状态一致；当En是低电平时，Q保持上次En时D的数据。
### 1.搭建dff电路，其中信号源D和信号源En均选择vpwl，输出端的负载仍选择100pf的电容。
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/syndff-tb/syndff%E7%94%B5%E8%B7%AF.png)

### 2.信号源D与En的设置：
#### D
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/syndff-tb/D%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)
#### En
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/syndff-tb/En%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

### 3.check and save后选择ADE L，在analysis中进行如下设置，然后选择D、En作为输入端，Q、Q'作为输出端：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/syndff-tb/syndff%E4%BB%BF%E7%9C%9F%E5%8F%82%E6%95%B0.jpg)

### 4.运行仿真，如图所示：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/syndff-tb/syndff-tb%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.png)

### 四、主从式dff
### 原理：当En输入高电平时，此时主触发器处于同步式触发器的输入状态，Qm与D的状态一致，但从触发器是封闭的；当En输入低电平时，主触发器处于锁存状态，Qm不变，从触发器的En端输入高电平，从触发器将处于同步式SR触发器的输入状态，此时Qm的信号将传递至从触发器Qs输出端。
### 1、搭建电路，电源选择vpwl，输出端的负载电容选择100pf.
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/msdff-tb/msdff%E7%94%B5%E8%B7%AF.png)

### 2、输入D端、En端参数。
#### D端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/msdff-tb/msdffD%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

#### En端
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/msdff-tb/msdffEn%E7%AB%AF%E8%BE%93%E5%85%A5.jpg)

### 3、check and save后选择ADE L，在analysis中进行如下设置，然后选择D、En作为输入端，Qm、Qm1、Qs、Qs'作为输出端：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/msdff-tb/msdff%E4%BB%BF%E7%9C%9F%E5%8F%82%E6%95%B0.jpg)

### 4、运行仿真，结果如图所示：
![Alt text](https://github.com/dailiuyao/markdown-photos/blob/master/msdff-tb/msdff%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)


