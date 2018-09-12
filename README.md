# Test of navigator.getDisplayMedia ScreenShare

The origin purpose of this repository is to test the implementation of `navigator.getDisplayMedia` in MS Edge.

Now the initial working implementation of getDisplayMedia() is available in the latest canary of Chromium(v70.0.3531.0). Please try out and give us feedback. You can post new Chromium bugs or add to the main tracking bug http://crbug.com/326740.

To try out: 
Start Chromium with flag --enable-experimental-web-platform-features or turn it on via chrome://flags/. 
Go to https://cdn.rawgit.com/uysalere/js-demos/master/getdisplaymedia.html.

Note that it is still WIP and not everything defined in the spec is implemented. See here for the active spec discussion topics.
