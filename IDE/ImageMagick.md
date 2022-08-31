# Image Magick


## Downscale all images in folder

```ps
$jpgs =  $(ls *.jpg); foreach($j in $jpgs){magick convert $j.Name -resize 512x512 $j.Name}
```
