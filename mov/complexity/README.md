The single frames were generated with CTVox, the key-frames are [here](control03_thresholded_.sb)

I removed the coordinate arrows (bottom left) and the Bruker logo (top right) with [Fiji](https://fiji.sc) and saved out the single frames again as PNG images.

With ImageMagick I made the (white) background of the single frames transparent and rescaled the images to HD width.

```bash
mogrify -format png -fuzz 5% -transparent "#FFFFFF" -resize 1080 *.png
```

Afterwards I ran all the images through [TinyPNG](https://github.com/kyleduo/TinyPNG4Mac) to reduce their file size.