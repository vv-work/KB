#  and Audio video Encoding


# ffmpeg

## Add audio with audio rencoding
```powershell
 ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac output.mp4
 ```

## Copy audio without rencoding
```powershell
ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv
```

# Replacing audio stream
```powershell
ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -map 0:v:0 -map 1:a:0 output.mp4
```


# youtube-dl

## Download best audios of best playlist
```powershell
youtube-dl -o '%(playlist_index)s - %(title)s.m4a'--playlist-start 26 -f 'bestaudio'  https://www.youtube.com/playlist?list=PLX2vGYjWbI0QvLHla7C_Z_s3q1Oi461o4

youtube-dl -o '%(playlist_index)s - %(title)s.webm'--playlist-start 26 -f 'webm'  https://www.youtube.com/playlist?list=PLX2vGYjWbI0QvLHla7C_Z_s3q1Oi461o4
```


# powershell
```powershell
foreach($file in $files){ ffmpeg -i $file'.webm' -i $file'.m4a' -c copy $file'.mkv' }
rm *.m4a
``` 