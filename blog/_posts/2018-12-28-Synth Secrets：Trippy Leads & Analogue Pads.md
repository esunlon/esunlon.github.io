---
layout: post
author: esunlon
date: "December 28, 2018"
img_link : https://i.loli.net/2018/12/20/5c1b489238337.jpg
excerpt_separator: <!--more-->
---
我们今天的Synth Secrets将会讨论如何在Ableon中进行声音设计，然后制作一种具有迷幻色彩的techno lead，和一种温暖，模拟味儿十足的Pad音色。最后设计到讨论如何用一些插件如Sonnox的VoxDoubler来给音色带来额外的深度和立体声效果。
<!--more-->
*Synth Secrets系列是一些列教程，我们通过试着使用Massive, Sylenth和Dive等流行的软件合成器来合成一些经典的，现代的合成器声音。*

![ableton-live-10-standard-download-e1519469302178-1400x479.jpg](https://i.loli.net/2018/12/28/5c25d253e2a9a.jpg){:class="w3-image"}

试听效果：
<audio src="https://f.cangg.cn:82/data/201812281546123562.mp3" controls="controls">  </audio>

下图是本次使用的MIDI音符。这个Loop是在F#小调（pad部分持续演奏F#）。

![MIDI-Screengrab-856x284.jpg](https://i.loli.net/2018/12/28/5c25d253bd479.jpg){:class="w3-image"}

##### Step 1

我们先开始制作一段简单的Beat，试听如下：

<audio src="https://f.cangg.cn:82/data/201812281546444762.mp3" controls="controls">  </audio>

然后插入Ableton的Analog插件，调整Osc1和2的Shape为锯齿波，并调高Osc1高出1个八度。然后调整两个振荡器的Detune向相反的方向，让声音更宽。最后打开噪音振荡器，调整音量和color带给整个音色很模拟的味道。

![Step-1-856x235.jpg](https://i.loli.net/2018/12/28/5c25d253c2d2e.jpg){:class="w3-image"}

##### Step 2

接下来我们来构建音色的包络部分。将滤波器的cutoff旋钮转到0，然后激活滤波器的包络，调大调制深度。调整attack并减小decay和sustain。

在Master控制区域，我们添加vibrato和unision detune全局效果，这样可以让音色更肥厚，更富有表情。然后调整voicing至monophonic，现在我们可以编排一段Clip，通过自动化滤波器的cutoff带来一些能量和运动感。

试听：
<audio src="https://f.cangg.cn:82/data/201812281547031685.mp3" controls="controls">  </audio>

![Step-2.1-856x237.jpg](https://i.loli.net/2018/12/28/5c25d253c399a.jpg){:class="w3-image"}

![Step-2.2.jpg](https://i.loli.net/2018/12/28/5c25d253e123b.jpg){:class="w3-image"}

![Step-2.3-856x98.jpg](https://i.loli.net/2018/12/28/5c25d253a045a.jpg){:class="w3-image"}

##### Step 3

下一步我们添加EQ，切掉一部分低频，添加Saturator增加攻击感，具体方法是，调高drive和depth但是调低output，以避免增加过多的音量。

我们在先将信号发送到载有Valhalla VintageVerb的Return轨道，然后再设置一个Return轨道，加载Sonnox 的VoxDoubler，这个插件主要用来处理人声，但是用再合成器音色上也不错。

选择Aux模式，将会锁定发送100%的信号，然后我们调整VoxDoubler的timing和pitch选项，为整个Lead增加一个新的声部。这种效果就像一个时间很短的延迟，但是聪明多了。然后调高Tone设置，增加一些高频Boost。添加EQ，切掉部分低频，衰减中频使得Return轨道的信号不会和源信号有太多的冲突。最后我们自动化VoxDoubler的timing让整个音色再时间上有运动感。

试听：
<audio src="https://f.cangg.cn:82/data/201812281554571598.mp3" controls="controls">  </audio>

![Step-3.1-856x229.jpg](https://i.loli.net/2018/12/28/5c25d253c188a.jpg){:class="w3-image"}

![Step-3.2-856x972.jpg](https://i.loli.net/2018/12/28/5c25d253e032e.jpg){:class="w3-image"}

![Step-3.3-856x111.jpg](https://i.loli.net/2018/12/28/5c25d253b5294.jpg){:class="w3-image"}

![Step-3.4-856x567.jpg](https://i.loli.net/2018/12/28/5c25d253db9a6.jpg){:class="w3-image"}

##### Step 4

现在开始制作Pad音色。继续加载一个新的含有Analog的轨道。然后编写MIDI音符：8个小节长的F#3音符。我们的目标是设计一个温暖而又模拟味十足的pad音色，所以调低Osc1和Osc2一个八度，并调整detune，然后打开噪声振荡器。

选择低通滤波器，增加一点点Reso，这样我们调整cutoff时会又一些有趣的音色变化。同样的，调大滤波器包络调制深度，调大attack然后调低decay和sustain。

返回到振荡器控制区域，我们添加一个音高包络，这样可以生成一种巧妙的滑音效果。然后打开vibrato和unison detune，通过自动化vibrato的Rate参数，进一步提高了音色的趣味性。

试听：
<audio src="https://f.cangg.cn:82/data/201812281555211469.mp3" controls="controls">  </audio>

![Step-4.1-856x243.jpg](https://i.loli.net/2018/12/28/5c25d2640ec41.jpg){:class="w3-image"}

![Step-4.2-856x152.jpg](https://i.loli.net/2018/12/28/5c25d264048ee.jpg){:class="w3-image"}

![Step-4.3-856x112.jpg](https://i.loli.net/2018/12/28/5c25d264066e3.jpg){:class="w3-image"}

##### Step 5

开始对Pad音色进一步雕琢。加入EQ切除低频，防止滤波器的共振峰占用过多的空间。

然后添加Sonnox VoxDoubler，这次我们选择Widen功能。Widen给信号增加了两个新的单声道声部信号，我们将其平移到左右声道的最两边。把Mix和Width设置的比较高。

抬高Pitch和Timing设置，增加效果的分离度，调高Tone设置增加高频的闪烁感。最后发送一些pad信号到我们之前设置的混响轨道增加空间感。

试听：
<audio src="https://f.cangg.cn:82/data/201812281555456380.mp3" controls="controls">  </audio>

![Step-5.1-856x576.jpg](https://i.loli.net/2018/12/28/5c25d26427d77.jpg){:class="w3-image"}

![Step-5.2-856x968.jpg](https://i.loli.net/2018/12/28/5c25d26429cc2.jpg){:class="w3-image"}

##### Step 6

最后，我们添加一段打击乐Loop。跟之前一样，用VoxDoubler的Widen模式增加宽度，调低Depth设置让节奏紧凑一些。然后调低Pitch和Timing控制。

试听（未处理）：
<audio src="https://f.cangg.cn:82/data/201812281556019363.mp3" controls="controls">  </audio>
试听（处理后）：
<audio src="https://f.cangg.cn:82/data/201812281556337140.mp3" controls="controls">  </audio>

![Step-6-856x964.jpg](https://i.loli.net/2018/12/28/5c25d2643020f.jpg){:class="w3-image"}
