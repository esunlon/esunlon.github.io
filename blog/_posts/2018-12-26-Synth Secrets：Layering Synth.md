---
layout: post
author: esunlon
date: "December 26, 2018"
img_link : https://i.loli.net/2018/12/20/5c1b489238337.jpg
excerpt_separator: <!--more-->
---
在今天的Synth Secretes教程中，我们将研究一下合成器的音色叠加技术，简单来说就是创造一种由三种不同合成器组成的音色，每个合成器都负责特定的频谱范围，这样我们就能得到一个非常宏大，饱满的合成器音色。
<!--more-->

*Synth Secrets系列是一些列教程，我们通过试着使用Massive, Sylenth和Dive等流行的软件合成器来合成一些经典的，现代的合成器声音。*

这是今天制作的Loop：

<audio src="http://f.cangg.cn:81/data/2018122615435042997030.mp3" controls="controls">  </audio>

MIDI音符及节奏模式如下：

![MIDI-660x289.png](https://i.loli.net/2018/12/26/5c232e1925983.png){:class="w3-image"}

##### Step 1

我们先来制作Sub（重低音部分）。加载Logic的EXS24插件，默认设置就是一个正弦波。然后调整ENV2的Attack喝Release，消除''吱吱""的杂音。

新增MIDI音符F#0，再频谱上观察peak应该再60Hz左右(40~60Hz一般是Sub部分的好位置，当然这也是很有主观性的)。然后创建一个与上图一样的MIDI模式，但注意Mute掉第一个音符，因为它和底鼓的位置有些冲突。

![Step-1.1-Sub-MIDI-660x304.png](https://i.loli.net/2018/12/26/5c232e194d1d4.png){:class="w3-image"}

然后用EQ，切除掉190Hz往上和30Hz往下的信号。然后用LFO Tool雕琢该部分的音量包络，防止过长的Release和其他底鼓冲突。

![Step-1.2-EXS24-660x477.png](https://i.loli.net/2018/12/26/5c232e19cd67b.png){:class="w3-image"}

![Step-1.3-Processing-660x964.png](https://i.loli.net/2018/12/26/5c232e19c51cf.png){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122615411567625739.mp3" controls="controls">  </audio>

##### Step 2

现在来考虑低中频层。我们使用U-he的Repro-5来设计音色。Repro-5有着非常温暖而模拟味十足的音色。将Sub轨道的MIDI音频拷贝到Repro-5的轨道，然后unmute第一个音符，并且调高此音符2个八度到F#2。

这部分的音色设计很直接。将Osc A的Octave调低到0，Osc B的波形调成三角波，调低Octave到0，Frequency到-12（这样将声音在次基础上调低更低的一个八度）。将滤波器的截止频率调整到19.50，然后将滤波器包络的深度调高到59.50，增加更深的包络调制。

![Step-2.1-Repro-5-660x419.png](https://i.loli.net/2018/12/26/5c232e19dbd26.png){:class="w3-image"}

为了得到一个更紧实的声音，将滤波器的Sustain调低，音量菠萝的Sustain调到0。效果器方面，添加Soft Clip Distortion，调高amount，调低Mix。然后用Velvet Tape Saturation的Dark模式带来更厚实的过载。

使用EQ切掉130Hz以下的声音给Sub部分腾出空间，然后也切掉3k以上的信息，这个部分只考虑低中频层。最后用压缩控制以下动态。

![Step-2.2-Lower-midrange-bass-processing-660x819.png](https://i.loli.net/2018/12/26/5c232e19c9578.png){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122615415413635027.mp3" controls="controls">  </audio>

##### Step 3

下一个音色由 Steinberg的Retrologue 2来合成，任何拥有3个振荡器的数字模拟合成器都可以胜任此工作。

首先拷贝上个步骤的MIDI音符到新的音轨，打开全部3个振荡器，都选锯齿波。将Osc 2的Coarse pitch调高3个半音，Osc 3的pitch调低1个八度，Coarse pitch调高7个半音，这刚好是一个小三和弦的音程关系。

![Step-3-Retrologue-660x549.png](https://i.loli.net/2018/12/26/5c232e19dd83d.png){:class="w3-image"}

打开Noise generator然后调整音量，这可以增加一些高频的闪烁感。在滤波器区域，调高包络的调制深度，然后调低Cutoff，调高Resonance到25左右。然后加如一些Tube distortion。

将滤波器的包络设置成中等Decay和短的Sustain，在音量包络中设置成高Sustain和中等Release，这意味着当截止频率很低的时候，演奏的音色会很短促，随着我们打开滤波器，音量包络会介入，创造很戏剧性的长音符。

试听：
<audio src="http://f.cangg.cn:81/data/2018122615421923352931.mp3" controls="controls">  </audio>

###### Step 4

对和弦层的处理，先用EQ低切250Hz。然后用CA-2A压缩，设置压缩reduction为5dB，当滤波器打开时，介入压缩，让声音动态减少一些。然后加载Ozone 7的Imager，打开Steroize控制并调高到13.2，在Band3和4的部分增加宽度，然后将2k以上的部分拓宽。

![Step-4-Chord-Sound-Processing-660x369.png](https://i.loli.net/2018/12/26/5c232e19a7fb4.png){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122615430921835524.mp3" controls="controls">  </audio>

##### Step 5

现在对和弦层进行发送Bus处理。首先在Bus轨道加入Stereo Delay，设置左右声道Delay Time为8分音符。调整双声道的Crossfeed和Low Cut，给整体带来ping pong delay的效果。

![Step-5.1-Stereo-Delay-1.png](https://i.loli.net/2018/12/26/5c232e19a62d4.png){:class="w3-image"}


为了让延迟的效果更整洁一些。我们将和弦层发送到另外一个Bus，然后Mute掉这个Bus轨道。这样做的目的是将Bus轨道用作侧链触发信号。返回到延迟Bus，我们增加一个压缩器在延迟效果后面，设置很快的Attack和Relese，然后引入Mute的Bus轨道来侧链压缩。

![Step-5.1-Stereo-Delay-2.png](https://i.loli.net/2018/12/26/5c232e24e915c.png){:class="w3-image"}

![Step-5.1-Stereo-Delay-3-660x436.png](https://i.loli.net/2018/12/26/5c232e24d32da.png){:class="w3-image"}

在压缩之后，用LFO Tool来duck底鼓，避免两者在混音中打架。

新增一个Bus，载入 Valhalla的Vintage Verb，然后根据自己的品味调整一些细节。

![Step-5.2-Chord-Verb-660x332.png](https://i.loli.net/2018/12/26/5c232e24d737a.png){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122615432993394559.mp3" controls="controls">  </audio>

##### Step 6

最后，我们来统一处理三个层的音色。首先加入Native Instruments的Solid Bus Comp，设置4dB的Gain reduction，Ratio设置为2，中量的Attack和Release设置。这样的压缩设置很好的将三层音色“粘”再一起。最后再和弦层加入一些滤波器自动化来创造一些移动效果，整体就完成了。

![Step-6.1-Group-compression-660x242.png](https://i.loli.net/2018/12/26/5c232e24df167.png){:class="w3-image"}

![Step-6.2-Automation-660x162.png](https://i.loli.net/2018/12/26/5c232e24ab0af.png){:class="w3-image"}

试听：
<audio src="http://f.cangg.cn:81/data/2018122615435042997030.mp3" controls="controls">  </audio>
