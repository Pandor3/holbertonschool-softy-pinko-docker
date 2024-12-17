# Chercher une image de base
FROM ubuntu:latest

# Update and upgrade to its latest release
RUN apt-get update && apt-get upgrade -y

# Install python3 and python3-pip
RUN apt-get install -y python3 python3-pip

# Install flask via pip3, not apt-get
RUN pip3 install flask --break-system-packages

# Will define the work directory
WORKDIR /app

# Copy api.py into /app
COPY api.py /app

# Will start the container with these parameters
CMD ["python3", "api.py"]
