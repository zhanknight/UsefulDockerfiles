# A slim container with Python 3 and yt-dlp
# Usage 1: docker build -t yt-dlp . 
# Usage 2: docker run --rm -it -v {host directory}:/downloads yt-dlp <URL> <Options>
# Will just print ytdlp help if nothing is specified. 

FROM python:3-alpine

RUN pip install --upgrade yt-dlp

WORKDIR /downloads

CMD [ "yt-dlp", "--help" ]
