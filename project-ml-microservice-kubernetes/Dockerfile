FROM python:3.7.3-stretch

LABEL maintainer="Damjan Dvoršek"

## Step 1:
# Create a working directory
WORKDIR /udacity

## Step 2:
# Copy source code to working directory
COPY app.py requirements.txt ./
COPY model_data ./model_data

## Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install -r requirements.txt

## Step 4:
# Expose port 80
EXPOSE 80
## Step 5:
# Run app.py at container launch
ENTRYPOINT [ "python", "app.py" ]

