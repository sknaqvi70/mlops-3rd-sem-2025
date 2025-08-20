# Step 1: Use an official Python runtime as a parent image
FROM python:3.13-slim

# Step 2: Set the working directory to /app
WORKDIR /app

# Step 3: Copy the requirements file and install the dependencies
# We do this first to take advantage of Docker's layer caching
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Step 4: Copy the rest of the application's source code
COPY . .

# Step 5: Expose the port the app runs on
EXPOSE 5000

# Step 6: Define the command to run the application
CMD ["python", "app.py"]