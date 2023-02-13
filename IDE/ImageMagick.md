#
Image Magick


## Downscale all images in folder

```ps
$jpgs =  $(ls *.jpg); foreach($j in $jpgs){magick convert $j.Name -resize 512x512 $j.Name}
```
`magick StoreLogo.scale-150.png -resize 63x63 StoreLogo.scale-125.png`	
