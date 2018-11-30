# Test of navigator.getDisplayMedia ScreenShare

The origin purpose of this repository is to test the implementation of `navigator.getDisplayMedia` in MS Edge.

Now the initial working implementation of getDisplayMedia() is available in the latest canary of Chromium(v70.0.3531.0). Please try out and give us feedback. You can post new Chromium bugs or add to the main tracking bug http://crbug.com/326740.

To try out: 

启用实验性平台：
Start Chromium with flag --enable-experimental-web-platform-features or turn it on via chrome://flags/. 
Go to https://cdn.rawgit.com/uysalere/js-demos/master/getdisplaymedia.html.

Note that it is still WIP and not everything defined in the spec is implemented. See here for the active spec discussion topics.

getDisplayMedia可以在Edge和chrome70+版本使用，都需要HTTPS源

不能实现任何分辨率、帧率控制。

- Edge可以设置constraints的width/height/framerate等参数，但并不能做到任何限制。
- chrome只能设置{audio:false,video:true}或{video:true}，不能设置其他参数（注意：audio要么为false,要么不设置）。

- 该MediaStream对象将只有一个MediaStreamTrack用于捕获的视频流; 没有MediaStreamTrack对应于捕获的音频流。

getDisplayMedia用法：

```angular2html
Edge: navigator.getDisplayMedia.then().catch()

Chrome: navigator.mediaDevices.getDisplayMedia.then().catch()

```


Edge和Chrome对于同一个操作的报错类型不完全相同，
详见[Edge和Chrome 70上 getDisplayMedia 接口研究](https://192.168.120.100:9001/blog/post/chrou/Screen-Capture)。
