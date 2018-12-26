---
layout: post
author: esunlon
date: "December 26, 2018"
img_link : https://f.cangg.cn:82/data/201812211036456931.jpg
excerpt_separator: <!--more-->
---
根据MDN教程，另一个简单的Web Audio API实现的合成器，
<!--more-->
<html>
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/assets/css/sks.css">
  </head>
  <body>
    <div class="container">
      <div class="keyboard"></div>
    </div>
    <div class="settingsBar">
      <div class="left">
        <span>Volume: </span>
        <input type="range" min="0.0" max="1.0" step="0.01"
            value="0.5" list="volumes" name="volume">
        <datalist id="volumes">
          <option value="0.0" label="Mute">
          <option value="1.0" label="100%">
        </datalist>
      </div>
      <div class="right">
        <span>Current waveform: </span>
        <select name="waveform">
          <option value="sine">Sine</option>
          <option value="square" selected>Square</option>
          <option value="sawtooth">Sawtooth</option>
          <option value="triangle">Triangle</option>
          <option value="custom">Custom</option>
        </select>
      </div>
    </div>
    <script src="/assets/js/sks.js"></script>
  </body>
</html>
