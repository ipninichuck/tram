#Tram Application Docker Container

FROM python:3.7-buster
LABEL maintainer="Ivan Ninichuck <ipninichuck@gmail.com>"
LABEL description="Dockerfile base for Tram Application"

#Copy packages needed
COPY requirements.txt /app/
WORKDIR /app

#use pip to install required modules
RUN pip3 install -r requirements.txt

#Copy Source Files to Container
COPY . /app

#Manually add the NLTK punkt module
RUN python3 -m nltk.downloader punkt

#Entrypoint for Container
ENTRYPOINT ["python"]

#Argument for command
CMD ["tram.py"]
