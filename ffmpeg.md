# ffmpeg

## Resize video

Resizing video while preserving aspect ration:

```
# Scale width maintain aspect ratio.
# If this doesn't work try 724 instead of 720
ffmpeg -i input.mov -filter:v scale=720:-1 -c:a copy output.mp4
```

https://superuser.com/questions/624563/how-to-resize-a-video-to-make-it-smaller-with-ffmpeg
