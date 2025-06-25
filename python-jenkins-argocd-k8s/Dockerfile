FROM python:3

# Install distutils first (required by Django)
RUN apt-get update && apt-get install -y python3-distutils

# Then install Django
RUN pip install django==3.2

# Copy your project files into container
COPY . .

# Run migrations
RUN python manage.py migrate

# Command to run your app (adjust as needed)
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
