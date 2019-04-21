for a in ~/proj/emoji/svg/*.svg; do ./inkscape --verb=FitCanvasToDrawing --verb=FileSave --verb=FileQuit ; done
convert -background none -bordercolor none -density 4800 -border 540 1f577.svg 1f577.png
