FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y \
 && apt-get install -y python3 python3-pip \
 && apt-get clean && rm -rf /var/lib/apt/lists/*

# PEP 668 guard off
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED /usr/lib/python*/dist-packages/EXTERNALLY-MANAGED

# Installe Flask + CORS
RUN pip3 install --no-cache-dir flask flask-cors

WORKDIR /app
COPY ./api.py /app/api.py

EXPOSE 5252
CMD ["python3", "api.py"]
