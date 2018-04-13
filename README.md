# ImageMagick-Snippets
My set of imagemagick commands

## Crop to a square centred in file
- Overwrites original
- Wildcard PNG selection

~~~~
convert *.png -set filename:original %t -gravity center -background black -extent 1440x1440 -quality 100 %[filename:original].png
~~~~


## Resize and then expand canvas
- Overwrites original
- Wildcard PNG selection
- Fill with background colour (black)

~~~~
convert *.png -set filename:original %t -resize "1080x1080" -gravity center -background black -extent 1080x2280 -quality 100 %[filename:original].png
~~~~

~~~~
convert *.png -set filename:original %t -resize "1440x1440" -gravity center -background black -extent 1440x2960 -quality 100 %[filename:original].png
~~~~


## Convert PNG frames to GIF

~~~~
convert -loop 1 -delay 10 *.png Animation_10.gif
~~~~
