---
title: 6-HTML标签-音视/频
date: 2021-08-09
---

## &lt;audio&gt;
&lt;audio&gt; 标签定义声音，比如音乐或其他音频流。
**实例**
一段简单的 HTML 5 音频
``` bash
<audio src="someaudio.wav">
您的浏览器不支持 audio 标签。
</audio>
```
**提示**：可以在开始标签和结束标签之间放置文本内容，这样老的浏览器就可以显示出不支持该标签的信息。

| 属性 | 值 | 描述 |
| --- | --- | --- |
| autoplay | autoplay | 音频就绪后马上播放 |
| controls | controls | 显示控件 |
| loop | loop | 音频结束时重新播放 |
| muted | muted | 规定视频输出应该被静音 |
| preload | preload | 音频在页面时加载并预备播放 |
| src | *url* | 要播放的音频链接 |


## &lt;video&gt;
**实例**
一段简单的 HTML5 视频
``` bash
<video src="movie.ogg" controls="controls">
您的浏览器不支持 video 标签。
</video>
```

| 属性 | 值 | 描述 |
| --- | --- | --- |
| autoplay | autoplay | 如果出现该属性，则视频在就绪后马上播放。 |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。 |
| height | pixels | 设置视频播放器的高度。 |
| loop | loop | 如果出现该属性，则当媒介文件完成播放后再次开始播放。 |
| muted | muted | 规定视频的音频输出应该被静音。 |
| poster | URL | 规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像。 |
| preload | preload | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。
如果使用 "autoplay"，则忽略该属性。 |
| src | url | 要播放的视频的 URL。 |
| width | pixels | 设置视频播放器的宽度。 |













