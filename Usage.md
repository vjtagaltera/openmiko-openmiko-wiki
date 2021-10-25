The configuration by default provides 3 output streams:

- 1920x1080 H264
- 1920x1080 JPG over HTTP (MJPEG)
- 640x360 H264

There are some jagged edges on the 640x360 stream that I haven't been able to figure out yet.

The streams can be accessed using the following URLs:

- rtsp://IP:8554/video3_unicast
- rtsp://IP:8554/video5_unicast
- http://IP:8080/?action=stream
- http://IP:8080/?action=snapshot
