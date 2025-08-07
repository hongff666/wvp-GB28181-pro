# 无 callId 推流
ffmpeg -re -stream_loop -1 -i input.mp4 -c copy -f rtsp -rtsp_transport tcp "rtsp://127.0.0.1:5540/live/test?sign=25d55ad283aa400af464c76d713c07ad"

# 有 callId 推流
ffmpeg -re -stream_loop -1 -i input.mp4 -c copy -f rtsp -rtsp_transport tcp "rtsp://127.0.0.1:5540/live/test?callId=88888888&sign=25d55ad283aa400af464c76d713c07ad"

- 如果推流时使用了 callId，播放时必须带上相同的 callId