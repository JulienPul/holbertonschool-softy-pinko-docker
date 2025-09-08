FROM ubuntu:latest
# maj paquets
RUN apt-get update && apt-get upgrade -y
# maj logiciels
RUN apt-get install -y python3 python3-pip
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install --no-cache-dir flask
COPY ./api.py /app/api.py
EXPOSE 5252
CMD ["python3", "api.py"]
