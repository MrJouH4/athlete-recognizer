# Athlete Recognizer app
This project is a web application designed for athlete recognition using machine learning models and deployed using Flask framework. The application currently supports the identification of the following athletes:

![Website snapshot](/ui/images/ui_snapshot.png "website snapshot")

- Lionel Messi
- Maria Sharapova
- Roger Federer
- Serena Williams
- Virat Kohli

## Overview

The application implements logistic regression, support vector machine (SVM), and random forest classifiers. These models were trained using grid search cross-validation after data cleaning and wrangling processes. After evaluation, the logistic regression model was selected, achieving an accuracy of 0.909 for test data.

![91% Accuracy](/model/test_accuracy.png "test accuracy")
![Confusion Matrix](/model/confussion_matrix.png "confussion matrix")

## Installation

To run the project, follow these steps:

1. Install the required dependencies listed in `requirements.txt`:
   
   ```
   pip install -r requirements.txt
   ```
2. Run the server application:
   
   ```
   python server/server.py
   ```
3. Open `index.html` in UI folder in your web browser to access the user interface.

## Docker Installation (for Docker Users)

If you're using Docker, you can containerize the application:

1. Ensure Docker is installed on your system.

2. Build the Docker image:

   ```
   docker build -t athlete-recognizer .
   ```
3. Run the Docker container:

   ```
   docker run -p 5000:5000 athlete-recognizer
   ```
4. Access the application by opening `index.html` in your web browser.

## Next Steps

Future enhancements for the project include:

- Increasing the dataset size to improve model performance and the variety of athletes.
- Enhancing the machine learning models with advanced techniques including NeuralNetworks and pretrained models.
- Adding additional features to the web application for better user experience.
