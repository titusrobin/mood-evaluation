# Sentiment Analyzer: Harnessing Hugging Face's AI
Overview
Welcome to Sentiment Analyzer, a dynamic Flask-based web application utilizing Hugging Face's cutting-edge AI technology for real-time sentiment analysis. This application leverages the power of transformer models to interpret and analyze user-inputted text, offering insights into the underlying emotions and sentiments.

# Features
Real-time Sentiment Analysis: Instantly determines the sentiment of user-entered text.
Powered by Hugging Face Transformers: Utilizes pre-trained models for accurate and efficient analysis.
User-Friendly Interface: Easy to navigate Flask web application for seamless user experience.
Getting Started
To get started with Sentiment Analyzer, follow these simple steps:

# Setup Environment: Ensure that Python and Flask are installed on your system.
Install Dependencies: Run pip install -r requirements.txt to install necessary libraries.
Launch Application: Start the Flask server and access the web application through your browser.
How It Works
Sentiment Analyzer uses a pre-trained model from Hugging Face's transformers library. The model, trained on extensive datasets, is adept at understanding various nuances in text and predicting sentiment with high accuracy.

# Model Integration
The Flask application (app.py) incorporates the Hugging Face model using its pipeline module.
User input is processed by the model to predict sentiment, displaying results in real-time.

![6](https://github.com/titusrobin/mood-evaluation/assets/143838819/9f257693-9501-433c-9376-f61a02a19a54)
![9](https://github.com/titusrobin/mood-evaluation/assets/143838819/d4e41e4e-d493-4ec8-b680-dc6115eba48b)


## Deploying Flask App to Docker Hub

#### Build the Docker image:
    - docker build -t my-flask-app .

#### Run the Docker container locally:
    - docker run -p 5000:5000 my-flask-app

### Deploying to Docker Hub
    - docker login
    - docker tag my-flask-app username/my-flask-app:latest
    - docker push username/my-flask-app:latest


## Prerequisites

      - [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli) 

## Steps


### 2. Configure Flask App

      - pip install flask transformers

### 3. Azure Login

      - az login

### 4. Deploy to Azure App Service

      - az webapp up --sku F1 --name <YOUR_APP_NAME> --location <YOUR_REGION>

Replace <YOUR_APP_NAME> with your app name and <YOUR_REGION> with your desired Azure region.

### 5. Access Your Web App

      - https://<YOUR_APP_NAME>.azurewebsites.net


## HTML Templates

The Flask web application uses HTML templates for the user interface. Two main templates are used:

### `index.html`

This HTML file serves as the main user interface for inputting text for sentiment analysis. It contains:

- Text area for user input.
- Form submission for analysis.
- Basic styling elements.

Modify `index.html` to adjust the layout, add more input fields, or enhance the user experience based on your application's requirements.

### `result.html`

The `result.html` template is used to display the sentiment analysis result. It includes:

- Display area for the analyzed text.
- Section to show the sentiment analysis result.

These HTML templates are used in conjunction with the Flask routes in `app.py` to render the user interface and display analysis results to the end-user.


### 6. CI/CD Automation files


.github/workflows - This directory in a Python project (or any GitHub repository) is used for creating and storing GitHub Actions workflows. GitHub Actions is a continuous integration and continuous delivery                           (CI/CD) platform provided by GitHub. The workflow is triggered on pushes to the main branch. It sets up :
   
       1. Python environment
       2. Installs project dependencies
       3. Install packages
       4. Runs tests
       5. Format
       6. Linting
       
