FROM python:3

# Install system dependencies
RUN apt-get update && apt-get install -y python3-distutils

# Install Django
RUN pip install django==3.2

# Copy your project files into the image
COPY . .

# Run migrations
RUN python manage.py migrate

# Set default command
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
