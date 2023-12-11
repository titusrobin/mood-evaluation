# Auto Scaling Flask App Using Azure App Services

[![Sentiment_Analysis CI/CD](https://github.com/titusrobin/mood-evaluation/actions/workflows/cicd.yml/badge.svg)](https://github.com/titusrobin/mood-evaluation/actions/workflows/cicd.yml)

## Hugging Face Model Integration

The Flask web application (`app.py`) integrates a sentiment analysis model provided by Hugging Face's Transformers library. This model is used to analyze the sentiment of text input by users.

### Model Description

The sentiment analysis model employed in this application is based on Hugging Face's pre-trained transformer models, which are designed for natural language processing tasks. The model uses transfer learning on a large corpus to predict the sentiment of text data.

### Integration Details

The model is loaded using Hugging Face's `pipeline` module within the Flask application (`app.py`). When a user inputs text into the application, the model processes the text and predicts the sentiment, returning the result to the user.

The relevant code snippets in `app.py` demonstrate how the model is loaded and used for sentiment analysis.

### Model Customization

This application uses a pre-trained sentiment analysis model, but Hugging Face offers various pre-trained models for different natural language processing tasks. Users can explore and choose different models based on their specific requirements by modifying the model loading code in `app.py`.

### Working of the app

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
       
