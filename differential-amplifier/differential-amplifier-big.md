# differential amplifier仿真
## A、大信号分析
## 1、带有源电流镜的差动对的电路图
### 首先搭建差动放大器的器件模型，注意搭建模型时不要用basic库里的器件，检测器件用analoglib库，搭建差分放大器这一模型时不要将电流源，gnd等检测器件放入，只放入能够在版图中搭建的电路。设置DC变量为Vin1，vin2=0.9V,Vdd=1.8V，Vb=0.6V，如图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-big/df-amp.jpg)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-big/%E7%94%B5%E8%B7%AF%E5%9B%BE.jpg)

## 2、各器件的参数设置
### 如图：
![M0、M1](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-big/M0%E3%80%811.jpg)
![M2](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-big/M2%E5%8F%82%E6%95%B0.jpg)
![M3、4](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier/M3%E3%80%814%E5%8F%82%E6%95%B0.jpg)

## 3、仿真设置
### 设置DC扫描变量Vin1，扫描范围0-1.8V，选择输出Vout，如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier/%E4%BB%BF%E7%9C%9F%E5%8F%82%E6%95%B0.jpg)

## 4、仿真结果
### 运行仿真后，在ADE L界面点击Results-Annotate-DC Node Voltages，可以显示每个节点的电压值，还可点击Results-Circuit Conditions，可以显示电路中器件是工作在饱和区还是线性区，仿真结果如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)

## B、小信号分析
## （1）AC仿真
## 1、调用差分放大器模型搭建仿真电路，为直观地得出幅频增益，在输入电源端采用两个Voltage gain为0.5和-0.5的vcvs受控电压源提供两个反相的交流信号，供电电压源是由一个-0.1V的vdc和一个DC输入为Vin1 V（注意此处的变量名称一定要与所在电压源名称一致，这样才能顺利进行增益分析），AC Magnitude为0.4V的vsin电压源串联得到的（此处的vdc是为了抵消在后续仿真参数设置vin=0.1V，因为只有输入变量不为零此电路才能直接得出增益），此外电路的偏置电压由V5提供，V5是一个0.9V的vdc。如图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-ac/E0.jpg)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-ac/vsin.jpg)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-ac/%E7%94%B5%E8%B7%AF.jpg)

## 2、在ADE L界面设置analyses为AC，如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-small/analyses%E5%8F%82%E6%95%B0.jpg)

## 3、在ADE L界面设置Vin1为变量，并设值0.1V，选择Vout为输出，如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-small/ADE%20L.jpg)

## 4、输出AC仿真，注意此处的输出结果可以超过1.8V，因为这是小信号模型的特例，如图：
![ttext](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-small/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)

## 5、在ADE L界面点击Result-Direct Plot-AC Gain & Phase，在schematic界面选择下图中的两条线：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-ac/%E9%80%89%E7%BA%BF.jpg)

## 6、cadence输出幅频增益，如下图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-ac/%E5%A2%9E%E7%9B%8A%E7%BB%93%E6%9E%9C.jpg)

## （2）trans仿真
## 1、在AC仿真电路的基础上将Vsin1的Amplitude设为4mV，Frequency设为10HZ，这样电路在仿真过程中输出电压不会因为超过Vdd而失真了，如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-trans/Vsin1.jpg)

## 2、仿真参数设置如图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-trans/ADE%20L.jpg)

## 3、仿真结果如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-trans/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)

## （3）stb仿真
## 1、调用df-smp搭建电路，其中iprobe是通直流，阻交流的器件，Vin1的设置如下所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/%E7%94%B5%E8%B7%AF.jpg)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/Vin1.jpg)

## 2、设置ADE L的参数值，在analyses中选择stb仿真，其选项设置如下图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/ADE%20L.jpg)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/analyses.jpg)

## 3、仿真结束后在ADE L界面点击Results-Direct Plot-Main Form，在Direct Plot Form界面点击Plot，如下图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/direct-plot-form.jpg)

## 4、输出仿真结果：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/differential-amplifier-stb/%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.jpg)
