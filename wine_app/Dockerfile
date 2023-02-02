# Use latest Python runtime as a parent image
FROM python:3.9-slim-buster

# Meta-data
LABEL maintainer="Yoel Turner <yoelturner99@gmail.com>" \
    description="MLOps_Lab_09_deployment"

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install the required libraries
RUN pip install -r requirements.txt

# Make port 8888 available to the world outside this container
EXPOSE 9696

# Start the app
ENTRYPOINT ["gunicorn", "--bind=0.0.0.0:9696", "main:app"]