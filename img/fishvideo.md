The original from Dea/Matt was media1.mp4, a +3 min long video.

Based on https://stackoverflow.com/a/42827058/323100 I trimmed it down to 30 seconds
Based on https://superuser.com/a/624564 I rescaled it to HD resolution
Based on https://superuser.com/a/268986 I removed the audio

```bash
ffmpeg -ss 00:00:05 -i media1.mp4 -to 00:00:35 -filter:v scale=1080:-2 -an fishvideo.mp4
```

This reduced the video from 252 MB to 7 MB.

I then took out the first frame of the video based on this: https://stackoverflow.com/a/44073745/323100

```bash
ffmpeg -i fishvideo.mp4 -vf "select=eq(n\,0)" -q:v 3 fishvideo.png
```

Then I added it to the presentation with the code shown in https://tex.stackexchange.com/a/195828/828
