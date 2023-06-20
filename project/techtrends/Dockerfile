# Use an official Python 3.8 runtime as a parent image
FROM python:3.8

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Run init_db.py to initialize the database
RUN python init_db.py

# Make port 3111 available to the world outside this container
EXPOSE 3111

# Run the application when the container launches
CMD ["python", "app.py"]
