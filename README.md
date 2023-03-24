# yt-dlp Configs
My yt-dlp setup for downloading YouTube playlists an music. Note that some files are not config files, but plain commands.

##Crops the thumbnail to be quatratic and embeds it into the mp3 file
```
yt-dlp LINK -f bestaudio -x --audio-format mp3 --add-metadata --embed-thumbnail --audio-quality 0 --ppa "EmbedThumbnail+ffmpeg_o:-c:v mjpeg -vf crop=\"'if(gt(ih,iw),iw,ih)':'if(gt(iw,ih),ih,iw)'\""
```
