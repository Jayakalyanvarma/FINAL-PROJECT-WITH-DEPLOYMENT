FROM python:3

# Create a directory named "app" inside the container
RUN mkdir /app

# Set the working directory in the container
WORKDIR /app

# Copy the entire app directory into the container
COPY app.py /app/
COPY requirements.txt /app/
COPY models /app/models/
COPY templates /app/templates/
COPY static /app/static/

# Install Python dependencies
RUN pip install -r requirements.txt

# Set environment variables for Flask
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_RUN_PORT=8000

# Expose port 8000
EXPOSE 8000

# Command to run the Flask application
CMD ["python", "app.py"]