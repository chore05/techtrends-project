# Use an official Python 3.8 runtime as a parent image
FROM python:3.8

# Set the working directory to /usr/src/app
WORKDIR /usr/src/app

# Copy the requirements.txt file into the Docker container
COPY ./project/techtrends/requirements.txt ./

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the remaining directory contents into the container at /usr/src/app
COPY ./project/techtrends .

# Run init_db.py to initialize the database
RUN python init_db.py

# Make port 3111 available to the world outside this container
EXPOSE 3111

# Run the application when the container launches
CMD ["python", "app.py"]
