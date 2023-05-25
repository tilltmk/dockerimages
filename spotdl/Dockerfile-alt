FROM debian:latest-slim

WORKDIR /app
RUN apt update -y && apt install git wget build-essential curl -y
RUN curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
RUN apt update -y
RUN apt install nodejs -y
RUN git clone https://github.com/spotDL/web-ui .
RUN npm i
RUN npm run dev
RUN npm build
RUN npm i -g serve
CMD ["serve ./dist"]
