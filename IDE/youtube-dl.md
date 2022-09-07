# yt-dlp

## Best Downloading options


### Download one vidoe

```bash
yt-dlp -f "bv*[height<=1080][ext=mp4]+ba[ext=m4a]" -o "%(playlist_index)s - %(title)s [%(id)s].%(ext)s" --embed-thumbnail
```

```bash
yt-dlp -f "bv*[height<=1080][ext=mp4]+ba[ext=m4a]" -o '%(playlist_index)s - %(title)s [%(id)s].%(ext)s'  --embed-thumbnail  https://www.youtube.com/c/SebastianLague/playlists

```

```bash

yt-dlp --cookies "B:\Lib\Proj\MyIDE\youtube.com_cookies.txt" -f "bv*[height<=1080][ext=mp4]+ba[ext=m4a]" --embed-thumbnail 
```

### Donlaod Playlist
```bash
yt-dlp --cookie "j:\Lib\Proj\MyIDE\youtube.com_cookies.txt" -f "bv*[height<=1080][ext=mp4]+ba[ext=m4a]" -o '%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s'  --embed-thumbnail  https://www.youtube.com/c/SebastianLague/playlists

```


```bash
yt-dlp -f "bv*[height<=1080][ext=mp4]+ba[ext=m4a]" -o '%(playlist_index)s - %(title)s.%(ext)s'  r_It_X7v-1E --embed-thumbnail  
```

## Cookie

To avoid blurry parts and download mature music

```powershell
youtube-dl --cookie B:\Lib\Proj\MyIDE\yt-cookies.txt -x --audio-format "mp3" https://www.youtube.com/watch?v=anEMXOyCCqc
```
