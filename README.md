# a-frame-video-test
placing videos in space

## running
you must use a simple localhost server as you need to serve local .mp4 assets

amazingly, safari as support for .m3u8 video streams as src in video elements, but not chrome... but still, video streams dont work in webvr in safari, could be the cross domain error tho.

## getting .m3u8 streams
since `.m3u8` streams expire, use `youtube-dl` to find a current link.

1. choose a format, like 91 for low quality
```
youtube-dl --list-formats https://www.youtube.com/watch?v=21X5lGlDOfg
```

2. will yield a https://xx.m3u8 link
```
youtube-dl -f 93 -g https://www.youtube.com/watch?v=21X5lGlDOfg
```
