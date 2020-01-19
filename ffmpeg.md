# ffmpeg

## Resize video

Resizing video while preserving aspect ration:

```
# Scale width maintain aspect ratio
ffmpeg -i input.avi -filter:v scale=720:-1 -c:a copy output.mkv
```

https://superuser.com/questions/624563/how-to-resize-a-video-to-make-it-smaller-with-ffmpeg
