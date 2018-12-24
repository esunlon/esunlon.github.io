---
layout: post
author: esunlon
date: "December 24, 2018"
img_link : https://i.loli.net/2018/12/20/5c1b489238337.jpg
excerpt_separator: <!--more-->
---

在今天的Synth Secrets教程中，我们将用Bitwig 2的Polysynth合成如下的音色：
<!--more-->
<audio src="http://f.cangg.cn:81/data/2018122414390784665671.mp3" controls="controls">  </audio>

*Synth Secrets系列是一些列教程，我们通过试着使用Massive, Sylenth和Dive等流行的软件合成器来合成一些经典的，现代的合成器声音。*

我们编写如下的MIDI音符。当你再编写这段Riff的时候，记得要调整音符的力度，而且要有一些相互重叠的音符，这样的Riff就有很高的动态。

![MIDI-Screenshot-856x378.jpg](https://i.loli.net/2018/12/24/5c207d3427a8b.jpg){:class="w3-image"}


##### Step 1

加载Polysynth插件。在oscillator选项中，我们将第一个oscillator调低两个八度，并调整成retrigger模式（保持音符的一致性），最后降低其Width。

在右边的菜单中，调整Mix到1，即只能听到Oscillator 1的声音，然后增加一些Drive，并将Glide旋钮拨至1/3左右。

试听：
<audio src="http://f.cangg.cn:81/data/2018122414393433589314.mp3" controls="controls">  </audio>

![Step-1.jpg](https://i.loli.net/2018/12/24/5c207d345ece5.jpg){:class="w3-image"}

##### Step 2

紧接着，我们调整EG旋钮，启用滤波器包络。对于FEG包络，调整Decay。对于AEG包络，A和S设置为0，然后调整DR如下图所示。

在右手边的菜单中，我们调整声道为MONO，然后激活FP功能：它只允许重叠的音符产生滑音效果。

试听：
<audio src="http://f.cangg.cn:81/data/2018122414394525517650.mp3" controls="controls">  </audio>

![Step-2.jpg](https://i.loli.net/2018/12/24/5c207d34576f0.jpg){:class="w3-image"}

##### Step 3

然后，我们增加一个滤波器，选择低通模式，将Cutoff调到最大，并将Resonce调到一半左右。点击左边的+号，增加调制。我们选择Expressions，它可以帮助我们用音符的力度，音色，压力和Releasetiao来调制滤波器的参数。

点击VEL的箭头，然后选择调制源cutoff，这样我们不同力度的音符就能有不同音色的差别。

试听：
<audio src="http://f.cangg.cn:81/data/2018122414402850754568.mp3" controls="controls">  </audio>

![Step-3.jpg](https://i.loli.net/2018/12/24/5c207d345761e.jpg){:class="w3-image"}

##### Step 4

我们继续增加调制，选择Bitwig的新S&H功能，然后用其调制滤波器的Resonace参数。S&H设置如下所示：

![Step-4.jpg](https://i.loli.net/2018/12/24/5c207d3461586.jpg){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122414405471597394.mp3" controls="controls">  </audio>

##### Step 5

最后我们来添加一些效果器 。加载Bit-8效果器，调低jitter和mix设置。这个效果器为整个音色的高频添加了一些bit-crush效果。

然后再添加Delay-1效果器，将延迟时间设置为16分音符（即是下图的2）。然后调整Feedback和Mix让其有更微妙的作用。终于完成了。

试听：
<audio src="http://f.cangg.cn:81/data/2018122414411125180784.mp3" controls="controls">  </audio>

![Step-5.jpg](https://i.loli.net/2018/12/24/5c207d3462a6f.jpg){:class="w3-image"}
