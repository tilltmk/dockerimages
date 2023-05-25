FROM debian:bullseye-slim

WORKDIR /app
RUN mkdir /data
RUN apt update -y && apt install git wget build-essential curl ffmpeg python3 python3-pip -y
RUN pip install spotdl streamlit
RUN git clone https://github.com/timothydillan/spotdl-streamlit-wrapper .
CMD streamlit run spotify.py
