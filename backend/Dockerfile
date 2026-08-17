# Use a minimal base image with Python 3.9 installed
FROM python:3.9-slim

# Set the working directory inside the container to /app
WORKDIR /app

# Copy all files from the current directory on the host to the container's /app directory
COPY . .

# Install Python dependencies listed in requirements.txt
RUN pip install -r requirements.txt

# Expose the port that the Flask app will run on
EXPOSE 7860

# Command to run the Gunicorn server
CMD ["gunicorn", "--bind", "0.0.0.0:7860", "app:superkart_api"]
