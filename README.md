## cctv-info
> CCTV, RTSP, RPi 3/4

### History
- 2019/12/09 [How to cook RTSP on your website in 2020, or why the boars will not have a chance to run away](https://habr.com/en/company/flashphoner/blog/479008/)
- 2019/07/25 [gstreamer and rtsp server with raspivid](https://www.raspberrypi.org/forums/viewtopic.php?t=246815)
- 2019/07/24 [Connect Raspberry Pi to IP Cameras – All You Need to Know](https://reolink.com/connect-raspberry-pi-to-ip-cameras/)
- 2019/04/15 [Live video streaming over network with OpenCV and ImageZMQ](https://www.pyimagesearch.com/2019/04/15/live-video-streaming-over-network-with-opencv-and-imagezmq/)
- 2019/02/16 [Cameradar hacks its way into RTSP videosurveillance cameras](https://golangexample.com/cameradar-hacks-its-way-into-rtsp-videosurveillance-cameras/)
- 2018/11/01 [RTSP Video, Kafka, and Microservices](https://adaickalavan.github.io/portfolio/rtsp_video_streaming/)
- 2018/01/14 [RTSP in HTML5 with low latency](https://linkingvision.com/rtsp_in_html5_with_low_latency)
- 2019/12/05 [Raspberry Pi Hardware Accelerated RTSP Camera](https://codecalamity.com/raspberry-pi-hardware-accelerated-h264-webcam-security-camera/)
- 2014/12/26 [Raspivid v Gst-rpicamsrc (Updated)](https://sparkyflight.wordpress.com/tag/gst-rpicamsrc/)


### History (Korean)
- 2019/09/06 [GStreamer: RTSP Server 구축(gst-rtsp-server)](https://argc.tistory.com/346)
- 2018/10/18 [Raspberry Pi 3: RTSP Server 설정](https://imsoftpro.tistory.com/53)
- 2014/07/27 [GStreamer RTSP with RPi](https://aery.tistory.com/entry/GStreamer-RTSP-with-RPi)

### Information
- libs.garden: [Go/RTSP](https://libs.garden/go/rtsp)
- [Real Time Streaming Protocol 2.0 (RTSP)](https://tools.ietf.org/id/draft-ietf-mmusic-rfc2326bis-33.html)
- [Raspberry Pi/Camera streaming](https://wiki.marcluerssen.de/index.php?title=Raspberry_Pi/Camera_streaming)
- [Raspberry PI RTSP Guide](https://www.stev.org/post/raspberrypisimplertspserver)


### Stackoverflow
- [Use an IP-camera with webRTC](https://stackoverflow.com/questions/23461914/use-an-ip-camera-with-webrtc)
- [curl/libcurl/API/Examples/rtsp.c](https://curl.haxx.se/libcurl/c/rtsp.html)


### Open Source
- [**Streamedian/html5_rtsp_player**](https://github.com/Streamedian/html5_rtsp_player)
- [ossrs/go-oryx](https://github.com/ossrs/go-oryx) - The go-oryx is SRS++, focus on real-time live streaming cluster.
- [gihad/streamer](https://github.com/gihad/streamer) - Converting Streams into HLS for playback on Chromecast devices using FFMPEG + NGINX
- [gihad/streamer](https://github.com/gihad/streamer) - Converting Streams into HLS for playback on Chromecast devices using FFMPEG + NGINX
- [Ullaakut/WebRTCCTV](https://github.com/Ullaakut/WebRTCCTV) - WebRTCCTV is a signaling server & webapp able to stream from RTSP cameras using WebRTC


### Open Source (Golang)
- [djwackey/dorsvr](https://github.com/djwackey/dorsvr) - Go RTSP Streaming Server
- [**rsfreitas/go-rtsp**](https://github.com/rsfreitas/go-rtsp) - A golang RTSP implementation
- [beatgammit/rtsp](https://github.com/beatgammit/rtsp) - rtsp implementation in Go
- [behrat/rtsp-proxy](https://github.com/behrat/rtsp-proxy) - rtsp-proxy
- [deepch/rtsp](https://github.com/deepch/rtsp) - Golang rtsp implement
- [lsowen/cam-record](https://github.com/lsowen/cam-record) - Golang server to record RTSP stream (such as security cameras) using gst-launch
- [deepch/rtsp_client](https://github.com/deepch/rtsp_client) - rtsp client
- [barnybug/go-cast](https://github.com/barnybug/go-cast) - A command line tool to control Google Chromecast devices.


### Open Source (Raspberry Pi)
- [lulop-k/kurento-rtsp2webrtc](https://github.com/lulop-k/kurento-rtsp2webrtc) - This example shows how to transform a RTSP feed or an HTTP feed into a low latency WebRTC stream in a simple and seamless manner.
- [Anonymousdog/displaycameras](https://github.com/Anonymousdog/displaycameras) - System for displaying RTSP feeds from IP cameras on the Raspberry Pi
- [florian-asche/RaspberryPiStreamingCamera](https://github.com/florian-asche/RaspberryPiStreamingCamera) - RaspberryPi RTSP Streaming Camera
- [**mpromonet/v4l2rtspserver**](https://github.com/mpromonet/v4l2rtspserver) - RTSP Server for V4L2 device capture supporting HEVC/H264/JPEG/VP8/VP9
- [iizukanao/node-rtsp-rtmp-server](https://github.com/iizukanao/node-rtsp-rtmp-server) - RTSP/RTMP/HTTP hybrid server
- [**thaytan/gst-rpicamsrc**](https://github.com/thaytan/gst-rpicamsrc) - GStreamer element for the Raspberry Pi camera module
- [**GStreamer/gst-rtsp-server**](https://github.com/GStreamer/gst-rtsp-server) - RTSP server based on GStreamer
- [neilyoung/receipt5.md](https://gist.github.com/neilyoung/8216c6cf0c7b69e25a152fde1c022a5d) - How to make a Raspberry Pi an RTSP streamer



### Commands
```
npm install git://github.com/Streamedian/html5_rtsp_player.git

cd gst-rtsp-server/examples
./test-launch --gst-debug=3 "( rpicamsrc bitrate=8000000 awb-mode=tungsten preview=false ! \
    video/x-h264, width=640, height=480, framerate=30/1 ! h264parse ! rtph264pay name=pay0 pt=96 )"
./test-launch "( rpicamsrc preview=false bitrate=2000000 keyframe-interval=15 ! \
    video/x-h264, framerate=15/1 ! h264parse ! rtph264pay name=pay0 pt=96 )"

tcpflow port 8554
```

