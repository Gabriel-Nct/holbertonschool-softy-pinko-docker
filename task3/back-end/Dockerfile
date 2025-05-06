# Start your image with an ubuntu base image
FROM ubuntu:latest

# The /app directory should act as the main application directory
WORKDIR /app

# Update packages and install necessary dependencies
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip \
    && rm /usr/lib/python*/EXTERNALLY-MANAGED \
    && pip3 install Flask flask-cors

# Copy the Python file to the container
COPY ./api.py /app/api.py

# Expose the port Flask will run on
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]