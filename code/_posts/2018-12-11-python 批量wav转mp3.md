---
layout: post
author: esunlon
date: "December 11, 2018"
img_link : https://i.loli.net/2018/12/11/5c0f87bae2513.png
excerpt_separator: <!--more-->
---
#### Dependencies：

1. libav or ffmpeg，这里我选了[ffmpeg](https://www.ffmpeg.org/)，ffmpeg是一个综合的音视频处理库，参考[安装教程](http://blog.gregzaal.com/how-to-install-ffmpeg-on-windows/)。

2. pydub, 安装直接pip install pydub，注意：安装pydub之前要安装好libav或者ffmpeg。引用作者的原文：
 <!--more-->

   >  You can open and save WAV files with pure python. For opening and saving non-wav files -- like mp3 -- you'll need ffmpeg or libav.

#### 示例程序

```
import os
import glob
from pydub import AudioSegment

video_dir = '/home/johndoe/downloaded_videos/'  # Path where the videos are located
extension_list = ('*.mp4', '*.flv')

os.chdir(video_dir)
for extension in extension_list:
    for video in glob.glob(extension):
        mp3_filename = os.path.splitext(os.path.basename(video))[0] + '.mp3'
        AudioSegment.from_file(video).export(mp3_filename, format='mp3')
```

遭了，python的glob库没用过，赶紧翻[PSL](https://docs.python.org/3/library/glob.html)。

>  glob — Unix style pathname pattern expansion

#### 第一次尝试

```

import os
import glob
from pydub import AudioSegment

extension = '*.wav'

for audio in glob.glob(extension):       mp3_filename = os.path.splitext(os.path.basename(audio))[0] + '.mp3'
        AudioSegment.from_file(audio).export(mp3_filename, format='mp3')
```

由于我只转码wav文件，所以替换掉了示例代码中的第一个for循环，**it worked!**

![](https://i.loli.net/2018/12/11/5c0f2f871e896.png){:class="w3-image"}
