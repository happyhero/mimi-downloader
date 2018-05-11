# Mimi Downloader

A Bilibili video downloader based on Node.js and Electron.

[中文/Chinese](README.CN.md)

## Features
Download Video (.flv) and Danmaku files (.xml or .ass).

## To Use
To clone and run this repository you'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer. From your command line:
```bash
# Clone this repository
git clone https://github.com/stevenjoezhang/mimi-downloader
# Go into the repository
cd mimi-downloader
# Install dependencies
npm install
# Run the app
npm start
```
If everything's OK, you'll see a new window named "Mimi Downloader". Input the videourl, then follow the guide to download files.  
If playurl is required, you can get it like this:

![demo-video](help.png)

You can combine flv video parts using ffmpeg:
```bash
cid=11090110
# Replace 11090110 with your video's cid
for f in $cid-*.flv; do echo "file '$f'" > temp.txt; done
ffmpeg -f concat -i temp.txt -c copy $cid.flv
```
Note: If you're using Linux Bash for Windows, [see this guide](https://www.howtogeek.com/261575/how-to-run-graphical-linux-desktop-applications-from-windows-10s-bash-shell/) or use `node` from the command prompt.

## Credits
* [Mimi](http://zsq.im) Developer of this project.
* 田生 [XML to ASS Library](https://github.com/tiansh/us-danmaku) and bilibili ASS Danmaku Downloader, Mozilla Public License 2.0
* soimort [you-get](https://github.com/soimort/you-get) MIT license
* henrikingo [xml2json](https://github.com/henrikingo/xml2json) GNU LESSER GENERAL PUBLIC LICENSE Version 2.1
* [md5](http://pajhome.org.uk/crypt/md5) BSD License

## License
Released under the GNU General Public License v3  
http://www.gnu.org/licenses/gpl-3.0.html

## TODO List
Start/Pause Download.  
Resume broken downloads
