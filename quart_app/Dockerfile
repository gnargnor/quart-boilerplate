FROM python:3.7-alpine

# Create a user
RUN adduser -D quart
# Set working directory for the purpose of this Dockerfile
WORKDIR /home/quart

# Copy requirements to the app root
COPY quart_app/requirements.txt ./
# Create a virtual environment and install the dependecies
RUN python3 -m venv venv && \
  venv/bin/pip install --no-cache-dir -r requirements.txt --upgrade && \
  chown -R quart:quart ./

# Copy the app into our user root
COPY quart_app/ /home/quart/
# Make our entrypoint executable
RUN chmod +x boot.sh

# Set the user
USER quart
# Set the entrypoint
ENTRYPOINT ["sh", "./boot.sh"]