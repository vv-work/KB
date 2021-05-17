# Media files convertation

## List

- ScreenToGif
- Youtube-dl
- ffmbeg
- giftowebp
- imgtowebp

## FFMPEG

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

