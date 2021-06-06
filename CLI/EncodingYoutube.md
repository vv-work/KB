# My solution

```powershell
cd 'B:\Lib\Proj\PS\YT-Loader\'
. .\Manager.ps1
YT-Init
```

```powershell
. 'B:\Lib\Proj\PS\YT-Loader\YTTools.ps1'
DownloadPlaylist "address"
```

# ffmpeg

### Add audio with audio rencoding
```powershell
 ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac output.mp4
 ```

    ### Copy audio without rencoding
    ```powershell
    ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv
    ```

### Replacing audio stream
```powershell
ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -map 0:v:0 -map 1:a:0 output.mp4
```


# youtube-dl



## Download arcive
Use download-archive feature. With this feature you should initially download the complete playlist with `--download-archive /path/to/download/archive/file.txt` F

    youtube-dl --download-archive archive.txt "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

will download the complete `PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re` playlist and create a file `archive.txt`. Each subsequent run will only download new videos if any:

## Download best audios of best playlist
```powershell
$link = '%Video Link'

youtube-dl -o '%(playlist_index)s - %(title)s.webm' -f 'webm' $link
youtube-dl -o '%(playlist_index)s - %(title)s.m4a'-f 'bestaudio' $link

```


```powershell
foreach($file in $files){ ffmpeg -i $file'.webm' -i $file'.m4a' -c copy $file'.mkv' }
rm *.m4a
``` 

# To get only info about playlist
--flat-playlist
#if you downloading playlist
--yes-playlist
# to download video only
-f "webm"
# to download audio onlie
-x --audio-format "mp3"
# Download audio from playlist
youtube-dl			-x --audio-format "mp3"

# Getting file names
 youtube-dl --get-filename -o '%(playlist_index)s - %(title)s' $link

# Create Folder
$folder = youtube-dl --get-filename --playlist-items 1  -o '%(playlist)s' $link
mkdir $folder
cd $folder

 # Download all webm
youtube-dl -o '%(playlist_index)s - %(title)s.webm' -f 'webm' $link
# Download all m4a
youtube-dl -o '%(playlist_index)s - %(title)s.m4a' -f 'm4a'  $link
