# Searcha  base image
FROM ubuntu:latest

# Update and upgrade to its latest release
RUN apt-get update && apt-get upgrade -y

# Install python3 and python3-pip
RUN apt-get install -y python3 python3-pip

# This will prevent an error when installing python packages
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install flask via pip3, not apt-get
RUN pip3 install flask --break-system-packages

# Install flask-cors via pip3
RUN pip3 install flask-cors --break-system-packages

# Will define the work directory
WORKDIR /app

# Copy api.py into /app
COPY ./api.py /app/api.py

# Will start the container with these parameters
CMD ["python3", "api.py"]
