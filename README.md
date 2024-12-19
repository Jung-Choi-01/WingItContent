# WingItContent
content hub for the VRChat game WingIt
---
each directory represents an image pack
- image packs have n files {0-n}.jpg where n is defined in size.txt

# how were these directories created this seems really stupid and hard??
requires
	- a bunch of images that have consistent resolutions
	- imagemagick 
	- chatgpt helps a lot you can ask it lots of things
essentially, i followed this procedure:
we have a bunch of yucky unprocessed files to start (funny.jpg, cat.png, graph.webp)
1. convert all files to be raw .jpg, i.e. funny.jpg, cat.jpg, graph.jpg (imagemagick can do this, ask gpt)
2. rename all files to be sequential titles, i.e. 1.jpg, 2.jpg, 3.jpg (bash can do this, ask gpt)
3. arrange files in a consistent grid such that they're below 2048x2048 (must be below in BOTH dimensions)
	- i.e. image 2049x1 will not work
	- magick montage is a great way to do this
4. put them in that grid
5. make a data.json with the total number of output files and grid dimensions (as seen in the live repo) and upload