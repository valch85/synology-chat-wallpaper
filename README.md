# synology-chat-wallpaper
some infor about change backgroud wallpaper of the Synology Chat

SSH to the NAS and under sudo search for the location of the files (before that, I checked what is the file name via developers tools in firefox loaded for the wallpaper). For me, it was wallpaper_dark_01.jpg.

find / -name wallpaper_dark_01.jp

I've got such a response:

/volume1/@appstore/Chat/ui/images/theme/2x/wallpaper_dark_01.jpg

/volume1/@appstore/Chat/ui/images/theme/1x/wallpaper_dark_01.jpg

Have tried to add new wallpapers but it is not worked for me so I decided to change exist.

I copied, with replace, new files for the wallpaper_dark_01.jpg & thumbnail_dark_01.jpg on both directories.

Change owner and permissions to a proper one

chmod -R 755 /volume1/@appstore/Chat/ui/images/theme/1x

chmod -R 755 /volume1/@appstore/Chat/ui/images/theme/2x

chown -R Chat:Chat /volume1/@appstore/Chat/ui/images/theme/1x

chown -R Chat:Chat /volume1/@appstore/Chat/ui/images/theme/2x

Restarted desktop application. For a browser, I needed to clean a cache that it started to show new wallpaper.
