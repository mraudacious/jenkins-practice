# Use the official Python base image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Copy the dependency file first, to leverage Docker cache
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application files
COPY . .

# Expose the port if your app uses a web framework (like Flask or FastAPI)
EXPOSE 5000

# Run the app
CMD ["python", "app.py"]
