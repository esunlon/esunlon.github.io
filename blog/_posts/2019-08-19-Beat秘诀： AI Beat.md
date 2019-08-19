---
layout: post
author: esunlon
date: "August 19, 2019"
img_link : https://i.loli.net/2018/11/30/5c00f6c876eed.jpg
excerpt_separator: <!--more-->
---

Google推出的Magenta Studio让机器学习在音乐生成应用方向更进了一步，直接官网下载桌面版（https://magenta.tensorflow.org/studio），我们今天就让**“他”**来制作一段鬼马的AI Beat。
<!--more-->

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0011%205-Audio.wav" controls="controls">  </audio>


### Melody

这里我选取了Magenta Studio的Generate组件来直接生成MIDI文件：

![11.gif](https://i.loli.net/2019/08/19/CUVjDMx1eiXa4hB.gif){:class="w3-image"}

Variations表示生成的MIDI文件数量，Temperature则表示生成旋律的复杂性和随机性（最上面可以选择生成鼓或旋律的MIDI文件）。

直接导入到Ableton Live中，选取合适的音色，这里我选择了生成的一段比较鬼马的旋律：

![12.PNG](https://i.loli.net/2019/08/19/pQdq2FlvPuxAj9K.png){:class="w3-image"}

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0001%205-Audio.wav" controls="controls">  </audio>

可以看出这是一段B大调的旋律，然后用一大堆的效果器处理成了像笛子亦或吉他的音色：

![13.PNG](https://i.loli.net/2019/08/19/32eAKhGWsM4BPwC.png){:class="w3-image"}

![14.PNG](https://i.loli.net/2019/08/19/C79dczVsnZ6FR8b.png){:class="w3-image"}

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0002%205-Audio.wav" controls="controls">  </audio>

最后的Cabinet预设，Sit in the Mix让这段旋律听起来就像从一个小喇叭里面发出来的声音。

### Drums

剩下的就跟AI没关系了，当然，Magenta Studio的Drumfy模块也可以根据MIDI文件自动生成鼓的MIDI文件，相当厉害。我这里是自己编写了一段Hip-Hop风格的节奏：

![21.PNG](https://i.loli.net/2019/08/19/5LQYBpcDhUgTRVj.png){:class="w3-image"}

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0003%205-Audio.wav" controls="controls">  </audio>

Nothing Fancy Here，对鼓组直接压缩和添加Drum Room混响效果。

### Chords

由于旋律的音符比较多，节奏相对比较复杂，这里添加的一段用钢琴演奏且节奏Shuffle的和弦，围绕着B Major来写：

![31.PNG](https://i.loli.net/2019/08/19/DvK76aiqhsNfVe5.png){:class="w3-image"}

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0004%205-Audio.wav" controls="controls">  </audio>

可以看到，音符被放置的错落有致，并且偏离网格线，来模拟真人弹奏的效果。

用EQ切掉低频，然后添加混响和延迟效果：

![32.PNG](https://i.loli.net/2019/08/19/pHj7K5Mq1bEIdJ8.png){:class="w3-image"}

![33.PNG](https://i.loli.net/2019/08/19/VRJuWef9qr4ZBsP.png){:class="w3-image"}

### Bass

Bass这里用了类似Trap的音色，然后调高了Distortion，然声音更硬了一些：

![41.PNG](https://i.loli.net/2019/08/19/bk5W4DO3R7JAlc9.png){:class="w3-image"}

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0005%205-Audio.wav" controls="controls">  </audio>

处理方面，用EQ切掉超低频，然后用侧链压缩给底鼓让出位置：

![42.PNG](https://i.loli.net/2019/08/19/ZrpoS5jRMsliGE2.png){:class="w3-image"}

### Mixing

来，合奏一下，听起来差极了。。。

试听：

<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0010%205-Audio.wav" controls="controls">  </audio>

Balance好音量和声像后快速的混一下：

![51.PNG](https://i.loli.net/2019/08/19/27TXADw5BJN6fds.png){:class="w3-image"}

这边没用OTT，不想让声音变得很塑料，凑合听吧：

试听：
<audio src="http://shaoqisama.oss-cn-beijing.aliyuncs.com/blog20190819/0011%205-Audio.wav" controls="controls">  </audio>

本次用到得采样链接：http://23.105.205.48:8000/f/b9ea18041e1943b0a3fb/?dl=1