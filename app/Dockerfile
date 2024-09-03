# Dockerfile for book_catalog microservice
# Use the official Python image from the Docker Hub- slim for smaller memory image
FROM python:3.8-slim
# specifies the working directory 
WORKDIR /app    
# copies requirements.txt file into the docker container.      
COPY requirements.txt requirements.txt  
#Install the required dependencies
RUN pip install --no-cache-dir -r requirements.txt    
# copies all the current folders file to the docker container
COPY . . 
 # Expose the port the app runs on
EXPOSE 8000
# Command to run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]