FROM python:3

# Update and install distutils package (needed by Django)
RUN apt-get update && apt-get install -y python3-distutils

# Install Django
RUN pip install django==3.2

# Copy all project files to container
COPY . .

# Run database migrations
RUN python manage.py migrate

# Start the Django development server (adjust if needed)
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
