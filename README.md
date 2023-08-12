# TextVision Image Text Extractor

![demo](https://github.com/ahsann455/TextVision-Image-Text-Extractor/assets/97152316/c5b7a9b8-c1bb-4352-9668-486de41a3984)

This Flask application utilizes Azure Computer Vision to extract text from images. It provides a user-friendly interface to submit an image URL and retrieve the extracted text content.

# Prerequisites

Before you begin, make sure you have the following:

-- Azure subscription: You'll need an Azure subscription to access Computer Vision services. If you don't have one, you can create a free account.

-- Azure Computer Vision API Key and Endpoint: To access the Computer Vision service, you'll need an API key and endpoint. Follow the steps to create a Computer Vision resource and obtain the necessary credentials.

-- Install requirements.txt
```pip install -r requirements.txt```

# Using the Application

-- Open your web browser and go to http://127.0.0.1:5000/.

-- You will see a simple interface with a text input field and a "Submit" button.

-- Enter the URL of the image from which you want to extract text and click "Submit".

-- The application will send the image to the Azure Computer Vision service, which will extract the text content from the image.

-- The extracted text will be displayed below the image input field.

To extract text from images in files on your local computer, visit https://postimg.cc/, upload your image there, and then copy and paste the "Direct Link" of the uploaded image to the ImageURL above.

# How the Application Works

The Flask application uses the azure-cognitiveservices-vision-computervision library to interact with the Azure Computer Vision service.

When you submit an image URL, the application calls the extractTextFromImage function, which performs the following steps:

Sends a request to the Computer Vision service to read text from the provided image URL.
Retrieves the operation location and waits for the results.
Once the operation is completed, the extracted text is collected from the response.
The extracted text is then displayed on the web page.

The user interface is built using Flask's render_template function and HTML templates located in the templates directory.
