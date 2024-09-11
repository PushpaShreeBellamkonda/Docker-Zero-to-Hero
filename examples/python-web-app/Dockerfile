# Use an official base image
FROM ubuntu:20.04

# Set working directory
WORKDIR /app

# Install Python and pip
RUN apt-get update && apt-get install -y python3 python3-pip

# Copy requirements.txt and install dependencies
COPY requirements.txt /app/
RUN pip install -r requirements.txt

# Copy the remaining app code
COPY . /app/

# Ensure the devops directory exists
RUN mkdir -p /app/devops

# Set the working directory to devops (or wherever needed)
WORKDIR /app/devops

# Optional: run your app
CMD ["python3", "app.py"]



