---
layout: post
author: esunlon
date: "January 04, 2019"
img_link : https://i.loli.net/2018/12/20/5c1b489238337.jpg
excerpt_separator: <!--more-->
---

本次合成器秘诀教学，我们将会用U-He的模拟建模合成器插件Repro-1制作一段Subby House Bass音色：
<audio src="https://f.cangg.cn:82/data/20190141626505722.mp3" controls="controls">  </audio>
<!--more-->
##### Step 1

我们首先载入Repro-1。我们先用默认预设音色录制如下的Baseline MIDI音符：

![Screen-Shot-2017-07-31-at-14.14.30.png](https://i.loli.net/2019/01/04/5c2f0a19ad03e.png){:class="w3-image"}

请注意音符的节奏性和旋律性。虽然很简单，但是音符长短时值的变化带给整体乐句向前运动的效果。音符的跨度基本都在半音之内，这样在听感上更强调律动。

试听：
<audio src="https://f.cangg.cn:82/data/20190141604137535.mp3" controls="controls">  </audio>

#####  Step 2

在Mix Secton，我们先只打开Osc A，先专注于一个振荡器的音色设计：

![Screen-Shot-2017-07-31-at-14.18.01-19.png](https://i.loli.net/2019/01/04/5c2f0a19edd9f.png){:class="w3-image"}

将Osc A 的波形（Shape）设置为方波（Square Wave）：

![Screen-Shot-2017-07-31-at-14.23.15.png](https://i.loli.net/2019/01/04/5c2f0a1a39c7c.png){:class="w3-image"}

然后将Osc A的OCTAVE调低一个八度，这个声部我们将用来塑造整体音色的Sub部分，方波可以很好的完成这个工作，提供强有力的低频声音。

试听：
<audio src="https://f.cangg.cn:82/data/20190141605489237.mp3" controls="controls">  </audio>

##### Step 3

然后我们转而关注Osc B，请按照如下设置，为整个音色添加高音部分：

![Screen-Shot-2017-07-31-at-14.24.54.png](https://i.loli.net/2019/01/04/5c2f0a1a3ad39.png){:class="w3-image"}

在Mixer中平衡A和B的音量：

![Screen-Shot-2017-07-31-at-14.26.26.png](https://i.loli.net/2019/01/04/5c2f0a1a3868e.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141606301371.mp3" controls="controls">  </audio>

##### Step 4

仔细聆听后，我们发现音色的高频部分有些刺耳，所以使用4-pole/24dB斜率的低通滤波器处理：

![Screen-Shot-2017-07-31-at-14.30.04.png](https://i.loli.net/2019/01/04/5c2f0a1a39671.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141618105249.mp3" controls="controls">  </audio>

为了让音色有趣一些，我们使用滤波器的包络调制CUTOFF，如下设置：

![Screen-Shot-2017-07-31-at-14.32.24-1.png](https://i.loli.net/2019/01/04/5c2f0a1a38a74.png){:class="w3-image"}

进一步，我们来设置包络的具体参数：

![Screen-Shot-2017-07-31-at-14.38.38-1.png](https://i.loli.net/2019/01/04/5c2f0a1a3a24c.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141618307156.mp3" controls="controls">  </audio>

##### Step 5

听起来我们制作的音色已经足够棒，但还是缺少些模拟的厚重感。Repro-1的FEEDB模式很好的解决了这个问题，在MIXER中打开：

![Screen-Shot-2017-07-31-at-14.39.02-1.png](https://i.loli.net/2019/01/04/5c2f0a1a3973b.png){:class="w3-image"}

然后调整左边的混入量，我感觉70%的设置比较不错：

![Screen-Shot-2017-07-31-at-14.43.05.png](https://i.loli.net/2019/01/04/5c2f0a1a34044.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141618443379.mp3" controls="controls">  </audio>

##### Step 6

基本快完成了，让我们再添加一些自动化参数带来更多的变化。

设置一个快速的LFO调制滤波器的cutoff，然后链接到MIDI键盘的调制轮上，方便我们制作自动化调制。

![Screen-Shot-2017-07-31-at-14.45.51-1.png](https://i.loli.net/2019/01/04/5c2f0a6df0b09.png){:class="w3-image"}

请试听我们制作的调制效果：
<audio src="https://f.cangg.cn:82/data/20190141620522998.mp3" controls="controls">  </audio>

##### Step 7

一个很好的Bassline处理技巧是，加入厚重的磁带过载来让整体的Low end更加肥厚：

![Screen-Shot-2017-07-31-at-14.51.30-1.png](https://i.loli.net/2019/01/04/5c2f0a6e344f7.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141621315384.mp3" controls="controls">  </audio>

然后使用EQ来调整低频。Neve的31102非常的丝滑和具有音乐性。我们使用高通滤波器切掉45Hz以下的低频。然后再用一个Low shelf cut衰减掉Ampex tape过载带来的多余隆隆声，最后再用一个high shelf提升高频，并给声音增加一些临场感。

![Screen-Shot-2017-07-31-at-14.53.33-1.png](https://i.loli.net/2019/01/04/5c2f0a6e16fd1.png){:class="w3-image"}

试听：
<audio src="https://f.cangg.cn:82/data/20190141626171076.mp3" controls="controls">  </audio>

最后就是加入侧链压缩让底鼓凸显出来。

试听：
<audio src="https://f.cangg.cn:82/data/20190141626341644.mp3" controls="controls">  </audio>
