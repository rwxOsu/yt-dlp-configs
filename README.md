# yt-dlp Configs
My yt-dlp setup for downloading YouTube playlists and music

## Shell Commands
The following commands plain shell commands
### Crops the thumbnail to be quatratic and embeds it into the mp3 file
```
yt-dlp LINK -f bestaudio -x --audio-format mp3 --convert-thumbnail png --add-metadata --embed-thumbnail --ignore-config --audio-quality 0 --ppa "ffmpeg: -c:v mjpeg -vf crop=\"'if(gt(ih,iw),iw,ih)':'if(gt(iw,ih),ih,iw)'\""
```
### Find out the IDs of non available YouTube Videos
This Command appends the IDs of not available YouTube-Videos to nichtverfuegbar.txt. Run this command after downloading your playlist with `--download-archive`
If you want to seperate the individual runs, run first:
```
echo ********************* >> nichtverfuegbar.txt
```
Then run the following command:
```
yt-dlp --get-id --download-archive archiv.txt --flat-playlist --ignore-config --cookies-from-browser chrome LINK >> nichtverfuegbar.txt
```
