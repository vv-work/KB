# Media files convertation

## List

- ScreenToGif
- Youtube-dl
- ffmbeg
- giftowebp
- imgtowebp

## FFMPEG

### Split Audio

Split audio into the equal 30 min parts

```powershell
ffmpeg -i .\ADHD-Relief.mp3 -f segment -segment_time 3000 -c copy ADHDRelief%03d.mp3
```

### Main

`-i StickAround.mp4`
Input file is StickAround.mp4

`-f gif` 
Format we wan't output into


`-ss 61.0` 
We want to start reading  from 61 second.

`-t 2.5`
We wan't to read only 2.5 seconds

### Mp4ToGif

Command:

```powershell 
ffmpeg -ss 61.0 -t 2.5 -i StickAround.mp4 -f gif StickAround.gif 
```

### Crop the video
`ffmpeg -i ForEugene.mp4 -filter:v 'crop=iw-840' 'EugeneCrop.mp4'`