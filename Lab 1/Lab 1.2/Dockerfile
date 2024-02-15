# Enable Dockerfile to read Python
FROM python:3.10-slim

# Allow messages to show in Knative logs
ENV PYTHONUNBUFFERED True

# Set environment to container
ENV APP_HOME /app

# Set directory to flask container
WORKDIR $APP_HOME

# Copy the directory contents into flask container
COPY . ./

# Install needed packages
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Run web service
# In this case there is 1 worker with 8 different threads
CMD exec gunicorn --bind :$PORT --workers 1 --threads 8 --timeout 0 main:app
