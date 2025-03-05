# Use Python 3.12 slim as the base image for a lightweight container
FROM python:3.12-slim 

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt . 

# Install Python dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . . 

# Command to run the application using Uvicorn server
# Host on 0.0.0.0 to allow external connections
# Run on port 8000
CMD ["unvicorn" , "main:app"  , "--host", "0.0.0.0", "--port", "8000"]
