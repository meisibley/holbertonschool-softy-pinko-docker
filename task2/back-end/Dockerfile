# base on lastest ubuntu
FROM ubuntu:latest

# update apt and install python3, python3-pip, and flask
RUN apt-get update -y
RUN apt-get install -y python3 python3-pip
RUN pip3 install Flask 

# upgrade currently installed software
RUN apt-get upgrade -y

# create working directory to /app
WORKDIR /app

# copy the python script to the working directory
COPY ./api.py /app/api.py

# expose port 5252
EXPOSE 5252

# run the Flask app
CMD ["python3", "api.py"]
