# FROM ubuntu

# WORKDIR /app

# COPY requirements.txt /app
# COPY devops /app

# RUN apt-get update && \
#     apt-get install -y python3 python3-pip && \
#     pip install -r requirements.txt && \
#     cd devops

# ENTRYPOINT ["python3"]
# CMD ["manage.py", "runserver", "0.0.0.0:8000"]



FROM ubuntu:20.04  # Specific version of Ubuntu for stability

WORKDIR /app  # Setting the working directory

COPY requirements.txt /app  # Copying the requirements file
COPY devops /app  # Copying the source code folder

# Update the package index, install Python and PIP
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install --no-cache-dir -r requirements.txt  # Using pip3 to install dependencies

# Set the entrypoint to use Python
ENTRYPOINT ["python3"]

# Default command to run Django server
CMD ["manage.py", "runserver", "0.0.0.0:8000"]

