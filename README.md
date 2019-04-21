# twemoji pngs

## svgs

This repository contains the v2 [twemoji](https://github.com/twitter/twemoji) svgs processed by Inkscape with
```
for a in *.svg; do ./inkscape --verb=FitCanvasToDrawing --verb=FileSave --verb=FileQuit ; done
```

Which means each file has a computed bounding box in the resulting `svg`. This is important for use with some tools (e.g. specific versions of Imagemagick) which clip the original twemoji files incorrectly when converting to raster formats.

Since it's rather time consuming to do the above and given the generous free license for `twemoji` (thanks, Twitter!), I've made this repo available so you don't have to repeat the effort.

## pngs

A common task with suitably fixed up `svg` files is to rasterize them to `.png` and the pngs in this repo are the result of:

```
for a in *.svg;do convert -background none -bordercolor none -density 4800 -border 540 $a `echo $a | sed 's/svg/png/g'`;done
```
