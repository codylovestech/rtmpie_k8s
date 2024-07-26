# Rtmpie live in kubernetes
This is a kubernetes yaml to install the rtmpie in a k8s 


--

## Test the Stream
```bash
ffmpeg -stream_loop 100 \
-re -i test.mp4  -c:v libx264 \
-x264opts keyint=30:min-keyint=30:scenecut=-1 -tune zerolatency \
-s 1280x720 -b:v 1400k -bufsize 2800k \
-f flv "rtmp://localhost/live/test?key=36117624b8e547028d2aec40d1c5b035"
```


