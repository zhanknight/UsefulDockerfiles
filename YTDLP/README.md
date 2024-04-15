# YTDLP
A slim container with Python 3 and yt-dlp preinstalled
# Usage
1. `docker build -t yt-dlp . `
2. `docker run --rm -it -v {host directory}:/downloads yt-dlp <URL> <Options>`

Will just print ytdlp help if nothing is specified. 
