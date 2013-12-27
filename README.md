# GKM
An event based, Global Keyboard and Mouse listener.

Tested on Windows 7, but should work on Linux and Mac OS X as well (untested).

[![NPM](https://nodei.co/npm-dl/gkm.png)](https://nodei.co/npm/gkm/)

## Why?
Node didn't have any global keyboard and mouse listener available at the time.

## Requirements
GKM depends on [JNativeHook](https://code.google.com/p/jnativehook/), which runs on Java. Thus you will need to have a JVM available and more importantly, java availble on your PATH.

## Getting started
Install gkm via node.js package manager:

    npm install gkm --save

Then require the package in your code:

```javascript
var gkm = require('gkm');

// Listen to all key events (pressed, released, typed)
gkm.events.on('key.*', function(data) {
    console.log(this.event + ' ' + data);
});

// Listen to all mouse events (click, pressed, released, moved, dragged)
gkm.events.on('mouse.*', function(data) {
	console.log(this.event + ' ' + data);
});
```

## License
The code is licensed under the MIT license (http://opensource.org/licenses/MIT). See license.txt.