# Installation Guide

> This page explains how to install RTCMultiConnection v3.

* Youtube Video: [NPM install](https://www.youtube.com/watch?v=EtsiYEW_T8Y) or [Other Videos](https://www.youtube.com/watch?v=EtsiYEW_T8Y&list=PLPRQUXAnRydKdyun-vjKPMrySoow2N4tl)

Or fetch latest code via github:

```sh
git clone https://github.com/muaz-khan/RTCMultiConnection.git ./RTCMultiConnection
cd RTCMultiConnection
sudo npm install --save-dev
```

Or wget/TAR:

```sh
mkdir RTCMultiConnection-v3
cd RTCMultiConnection-v3
wget http://dl.webrtc-experiment.com/rtcmulticonnection-v3.tar.gz
tar -zxvf rtcmulticonnection-v3.tar.gz
ls -a
```

* [rtcmulticonnection-v3.tar.gz](http://dl.webrtc-experiment.com/rtcmulticonnection-v3.tar.gz)

To TEST:

```sh
node server.js
```

## Stop Old Processes

Check all processes running on port `9001` and stop process by `id`:

```sh
lsof -n -i4TCP:9001 | grep LISTEN
kill process-ID
```

Or stop all processes on a specific port. (It may require `sudo` privileges):

```sh
fuser -vk 9001/tcp
```

Now open: `https://localhost:9001/`

## Keep running server in background

```sh
nohup nodejs server.js > /dev/null 2>&1 &
```

Or:

```sh
nohup nodejs server.js &
```

Or use `forever`:

```sh
npm install forever -g
forever start server.js
```

To auto-start `server.js` on system-reboot (i.e. when Mac/Linux system shuts down or reboots):

```sh
npm install forever-service

cd __path to your npm install__
forever-service install ncustomAppName --script server.js
```

Commands to interact with `service ncustomAppName Start`:

```
- "sudo service ncustomAppName start" Stop
- "sudo service ncustomAppName stop" Status
- "sudo service ncustomAppName status" Restart - "sudo service ncustomAppName restart"
```

More info about `forever-service` [here](http://stackoverflow.com/a/36027516/552182).

# Other Documents

1. [Getting Started guide for RTCMultiConnection](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/getting-started.md)
2. [Installation Guide](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/installation-guide.md)
3. [How to Use?](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/how-to-use.md)
4. [API Reference](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/api.md)
5. [Upgrade from v2 to v3](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/upgrade.md)
6. [How to write iOS/Android applications?](https://github.com/muaz-khan/RTCMultiConnection/tree/master/docs/ios-android.md)
7. [Tips & Tricks](https://github.com/muaz-khan/RTCMultiConnection/blob/master/docs/tips-tricks.md)

## Twitter

* https://twitter.com/WebRTCWeb i.e. @WebRTCWeb

## License

[RTCMultiConnection](https://github.com/muaz-khan/RTCMultiConnection) is released under [MIT licence](https://github.com/muaz-khan/RTCMultiConnection/blob/master/LICENSE.md) . Copyright (c) [Muaz Khan](http://www.MuazKhan.com/).
