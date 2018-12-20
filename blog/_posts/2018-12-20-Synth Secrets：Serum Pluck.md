---
layout: post
author: esunlon
date: "December 20, 2018"
img_link : https://i.loli.net/2018/12/20/5c1b489238337.jpg
excerpt_separator: <!--more-->
---
今天的教程中，我们将会使用Serum，一个非常流行的波表合成器。今天我们制作一个舞曲中很流行的Pluck音色，咋眼一看，调制矩阵好像很复杂，我们来一步步拆解。
<!--more-->

*Synth Secrets系列是一些列教程，我们通过试着使用Massive, Sylenth和Dive等流行的软件合成器来合成一些经典的，现代的合成器声音。*

音色试听：
<audio src="http://f.cangg.cn:81/data/2018122015344734977429.mp3" controls="controls">  </audio>

##### Step 1

打开Serum并在OSC A中加载Digtial项下的Dist 8Bit Fwap波形。


![SS1011.jpg](https://i.loli.net/2018/12/20/5c1b35370d2c4.jpg){:class="w3-image"}


在OSC A的操作界面，将Unison设置为4，detune旋钮设置为0.10。

![SS2.png](https://i.loli.net/2018/12/20/5c1b3519ccf87.png){:class="w3-image"}

然后打开OSC B并选择DIgital下的Crush Wub波形。

![SS3033-165x132.jpg](https://i.loli.net/2018/12/20/5c1b352fe5920.jpg){:class="w3-image"}

将Unison调到3，并且调整Detune到0.16。

![SS4.png](https://i.loli.net/2018/12/20/5c1b351a618ed.png){:class="w3-image"}

演奏并录制一个4小节的Loop如下图，建议有一些持续的长的音符，方便后面演示我们的调制效果。

![SS5055.jpg](https://i.loli.net/2018/12/20/5c1b35354b1a5.jpg){:class="w3-image"}

听起来是这样的：
<audio src="http://f.cangg.cn:81/data/2018122015352689667007.mp3" controls="controls">  </audio>

##### step 2

我们开始设计LFO。点击LFO 1，然后改变其波形。你可以随意创建波形，但我们这里选择这样：

![SS6.png](https://i.loli.net/2018/12/20/5c1b351aba037.png){:class="w3-image"}

注意这里的设置：

- Trip： On
- Rate: 1/8
- SMOOTH: 50

SMOOTH设置为50，保证LFO调制时的杂音最小。

将LFO链接到滤波器的Cutoff参数上。

![SS7.png](https://i.loli.net/2018/12/20/5c1b351f6d7d4.png){:class="w3-image"}

打开滤波器（Filter）功能，并链接OSC　A，B，调整LFO对cutoff的调制范围和深度。

![SS8.png](https://i.loli.net/2018/12/20/5c1b351a1133a.png){:class="w3-image"}

你录制的MIDI现在应该跟着LFO调动了，花点时间调整LFO的波形和调制范围，深度，根据你自己的品味进行实验吧。

试听：
<audio src="https://f.cangg.cn:82/data/201812201536056416.mp3" controls="controls">  </audio>

##### step 3

回到LFO区域，选择LFO2。这次使用默认的波形，并调整RATE到1/2。

![SS9.png](https://i.loli.net/2018/12/20/5c1b351b01959.png){:class="w3-image"}

将LFO2链接到OSC A和B的WT POS，并调整调制范围。

![SS10.png](https://i.loli.net/2018/12/20/5c1b351e6e665.png){:class="w3-image"}

播放你录制的Loop。每半个小节可以听到音色明显的变化。现在我们调整一下WT          POS被调制的范围。

![SS11.png](https://i.loli.net/2018/12/20/5c1b351e6e5ba.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/201812201536298233.mp3" controls="controls">  </audio>

##### step 4

接下来我们再增加一个LFO。实现内部的侧链功能。

LFO 3设置为如下图的样子：

![SS12.png](https://i.loli.net/2018/12/20/5c1b351b0c953.png){:class="w3-image"}

将LFO3链接到OSC A和B的Level旋钮上。将Level调低至26%的大小。调制范围至100%：

![SS13.png](https://i.loli.net/2018/12/20/5c1b3534cd39f.png){:class="w3-image"}

LFO3给整体的音色带来一种律动感的吸抽效果。

试听：
<audio src="https://f.cangg.cn:82/data/201812201536465859.mp3" controls="controls">  </audio>

##### Step 5

在Serum的主窗口选择Matrix。

![SS14-660x280.png](https://i.loli.net/2018/12/20/5c1b353353e61.png){:class="w3-image"}

这个矩阵图表示了我们之前的连线逻辑。增加一个调制，选择Env2，然后在DESTINATION中选择Fx>Verb Wet。并调整AMOUNT如下图所示。

![SS15.png](https://i.loli.net/2018/12/20/5c1b35354d313.png){:class="w3-image"}

然后转到Env2窗口，设置它的ADSR如下图所示：

![SS16.png](https://i.loli.net/2018/12/20/5c1b3535f0832.png){:class="w3-image"}

然后切换到Fx标签，选择Reverb效果器。

![SS17-660x471.png](https://i.loli.net/2018/12/20/5c1b353730180.png){:class="w3-image"}

Env2调制Reverb效果器的Mix比例，每次音符开始的时候就起作用。进一步，我们可以调整Env2的ADSR来控制变化的效果。调整Reverb中的Low Cut设置来衰减低频的浑浊信号。

试听：
<audio src="https://f.cangg.cn:82/data/201812201537017428.mp3" controls="controls">  </audio>

##### step 6

最后一步是添加EQ效果器，切除低频的信号并增加高频信号。基本搞定了。

![SS18-660x278.png](https://i.loli.net/2018/12/20/5c1b3535cd225.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/201812201537165396.mp3" controls="controls">  </audio>
