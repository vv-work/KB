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
$link = '%Video Link'

youtube-dl -o '%(playlist_index)s - %(title)s.webm' -f 'webm' $link
youtube-dl -o '%(playlist_index)s - %(title)s.m4a'-f 'bestaudio' $link

```


# powershell
```powershell
foreach($file in $files){ ffmpeg -i $file'.webm' -i $file'.m4a' -c copy $file'.mkv' }
rm *.m4a
``` 