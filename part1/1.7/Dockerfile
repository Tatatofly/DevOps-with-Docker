FROM ubuntu:16.04
COPY . .
RUN chmod +x scr.sh
RUN apt-get update && apt-get install -y curl
CMD ["./scr.sh"]
