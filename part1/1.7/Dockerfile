FROM ubuntu
WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
COPY script.sh /script.sh
CMD ["sh", "-c", "/script.sh"]



