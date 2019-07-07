# 一、原理
由于nmos的沟道电流Id主要受到栅极电压和源漏间电压的影响，所以以栅极电压为参数，探讨在恒定的栅极电压下，沟道电流和源漏间电压的关系即是nmos的输出特性。
# 二、搭建电路
由于衬底一般与源极相连，所以设定Vbs=0，且接地。在栅极输入端接上电压源Vgs，漏极接入电压源Vds，注意此处两电压源的DC参数输入字母而不是给定的数字，这样才是可变电压。如下图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-%E7%94%B5%E8%B7%AF.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-vds.png)
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-vgs.png)

# 三、选择仿真模式
检查电路并check and save后点击ADE L,进入仿真界面，首先选择仿真模式，在analysis中选择DC仿真，并进行如下设置：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-choosing%20analysis.png)

# 四、设置变量
选择variables，设置变量，并任意给定初始值，此初始值对后续操作无影响，只是必须环节而已。如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-design%20variables.png)

# 五、设置参数
点击Tools-Parametric analysis，进行如下参数设置：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-parametric%20analysis.png)

# 六、选择输出结果
参数设置结束后，在参数设置页面点击绿色仿真图标，完成仿真后在仿真界面点击Result-direct plot-main form，然后在弹出窗口选择电流，点击OK后在电路原理图中点击漏极所连电源的下方节点（电流的正负方向与所选节点有关），如图：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos-direct%20plot%20form.png)

# 七、输出仿真结果
在仿真结果窗口按快捷键v即可产生一条垂线，根据此线得出数据，进行后续计算，如图所示：
![text](https://github.com/dailiuyao/markdown-photos/blob/master/nmos-analog/nmos%E4%BB%BF%E7%9C%9F%E7%BB%93%E6%9E%9C.png)