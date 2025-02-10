# Docker Basics 🐳

## Overview  
This project serves as an introduction to **Docker**, starting with a simple "Hello, World!" script using **Python** inside a Docker container.

## 📚 Documentation & Prerequisites  
Ensure you have the following installed:  
- [Docker](https://www.docker.com/)  
- [Docker Desktop](https://www.docker.com/products/docker-desktop)  
- [Python](https://www.python.org/)  

## 📌 Installation & Setup  

### **1️⃣ Create the Python Script (`app.py`)**  
Start by creating a file named `app.py` and add the following code:  
```python
print("Hello, World! from Docker")
```

### **2️⃣ Create the Dockerfile**  
Now, create a `Dockerfile` to containerize the Python script:  
```dockerfile
# Use the official Python image
FROM python:3.9

# Copy the application code into the container
COPY app.py /app.py

# Set the working directory
WORKDIR /

# Command to run the script
CMD ["python", "app.py"]
```

## 🚀 Deployment  

### **1️⃣ Verify Docker & Python Installation**  
Check if Docker and Python are installed:  
```sh
docker --version  
python --version  
```

### **2️⃣ Build the Docker Image**  
Run the following command to build the Docker image:  
```sh
docker build -t my-python-app .
```

### **3️⃣ Verify Image Creation**  
Check if the image was successfully built:  
```sh
docker images
```

### **4️⃣ Run the Docker Container**  
Execute the following command to run the container and print "Hello, World!" in the console:  
```sh
docker run my-python-app
```

## 🏆 Conclusion  
You have successfully run your first **Python application inside a Docker container!** 🎉  
This basic setup serves as a foundation for containerized applications.

---
