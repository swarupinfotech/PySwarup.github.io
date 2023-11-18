# Dockerfile

# Author       : Swarup Mahato
# Github       : https://github.com/swarupinfotech?tab=repositories
# Messenger    : https://www.facebook.com/profile.php?id=100069856215966
# Email        : swarupinfotech1@gmail.com
# Date         : 18-11-2023
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/KasRoudra/PyPhisher"

# Working directory
WORKDIR /PyPhisher/
# Add files 
ADD . /PyPhisher

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install python3-pip php openssh-client -y
RUN pip3 install -r files/requirements.txt --break-system-packages
RUN apt-get clean

# Main command
CMD ["python3", "pyphisher.py", "--noupdate"]

## Wanna run it own? Try following commnads:

## "sudo docker build . -t kasroudra/pyphisher:latest", "sudo docker run --rm -it kasroudra/pyphisher:latest"

## "sudo docker pull kasroudra/pyphisher", "sudo docker run --rm -it kasroudra/pyphisher"
