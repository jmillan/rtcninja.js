# `rtcninja` Module API


## `rtcninja()` function

By calling the library as a function it performs the WebRTC check in the browser. This function MUST be called before attempting to use the library.

It returns `true` if the browse supports WebRTC.


## `rtcninja.hasWebRTC()` function

Returns `true` if the browser supports WebRTC.


## `rtcninja.called` read attribute

Returns `true` if `rtcninja()` was already called.


## `rtcninja.version` read attribute

Returns a String with the version of the library.

```javascript
rtcninja.version

=> "X.Y.Z"
```


## `rtcninja.debug`

Provides access to the [debug](https://github.com/visionmedia/debug) module.


## `rtcninja.getUserMedia(constraints, successCallback, errorCallback)` function

Provides a wrapper over the native `navigator.(webkit|moz)getUserMedia` function. As a feature, if WebRTC is not supported this function fires the given `errocCallback` instead of throwing an error.


## `rtcninja.Connection` class

Provides access to the [`rtcninja.Connection`] class, which wrappes a native `(webkit|moz)RTCPeerConnection`.


## `rtcninja.RTCSessionDescription` class

Wrapper for the native `RTCSessionDescription` class.


## `rtcninja.RTCIceCandidate` class

Wrapper for the native `RTCIceCandidate` class.


## `rtcninja.MediaStreamTrack` class

Wrapper for the native `MediaStreamTrack` class.


## `rtcninja.attachMediaStream(element, stream)` function

Sets the given `stream` (of type `MediaStream`) as the source of the <video> or <audio> element pointed by `element`.

Returns the `element` itself.


## `rtcninja.closeMediaStream(stream)` function

Closes the given `stream` (of type `MediaStream`).
