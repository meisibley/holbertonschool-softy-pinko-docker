# base image for container
FROM ubuntu:latest

# Update APT and install python3, python3-pip, and flask
RUN apt-get update -y
RUN apt-get install -y python3 python3-pip
RUN pip3 install Flask 

# Upgrade currently installed software
RUN apt-get upgrade -y

# Set working directory to /app
WORKDIR /app

# Copy the python script to the working directory
COPY ./api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]
