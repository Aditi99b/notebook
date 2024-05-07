---
toc: True
comments: False
layout: post
title: Data Structures Writeup 
description: My writeup!  
type: hacks
courses: {'compsci': {'week': 12}}
---

### Collections

- From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.
<img width="802" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/ff18f441-05f4-42d4-a26b-fb465a18802e">

- This is a database with all of the attention values in the sqlite data. The existence of a structured storage system, likely in the form of an SQLite database file. This database houses information pertaining to attention values, which could encompass metrics like user engagement, website visits, or social media interactions. Utilizing SQLite allows for efficient management and querying of this data, enabling analysis and insights into patterns of attention and user behavior. 

- From VSCode model, show your unique code that was created to initialize table and create test data.
<img width="611" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/043a926d-2987-4fe0-9af7-2d45475e4789">

- It sets up a database table structure and populate it with test data for initial testing or development purposes. It includes SQL statements to create the table schema, defining its columns and data types, followed by additional commands to insert sample data into the table. This initialization process allows developers to simulate real-world scenarios and ensure the functionality of their code within the database environment.

### Lists and Dictionaries

- In VSCode using Debugger, show a list as extracted from database as Python objects.
<img width="467" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/5d8f81c3-5d87-4a8c-9702-c79f161a2f04">

- This code extracts a list of Python objects from a database, likely using SQLite, representing structured data entries. Each object likely corresponds to a row or record in the database, containing attributes or fields mapped to Python variables. This enables easy manipulation and utilization of the database content within Python programs.

- In VSCode use Debugger and list, show two distinct example examples of dictionaries, show Keys/Values using debugger.
<img width="464" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/e80388b2-4fde-4231-88f6-12581bb56de8">
<img width="451" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/3aa5dce5-dbff-4715-9b01-59b835375c1e">

- Using a debugger, you can inspect these dictionaries' keys and values during runtime. For instance, in Python, you can use breakpoints and step through the code to examine the contents of these dictionaries at different points in your program execution. This helps in understanding how data is structured and accessed within dictionaries, aiding in debugging and development.

### APIs and JSON

- In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods. Discuss algorithmic condition used to direct request to appropriate Python method based on request method.
- In VSCode, show algorithmic conditions used to validate data on a POST condition.
<img width="689" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/5d0f40a6-b0fa-419b-8656-a221a5c02037">
<img width="517" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/3ab8ae09-3e6c-4b75-8157-90154f028043">
<img width="378" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/95e00b7d-cbf8-4a71-a3ef-7efa4c7d6d00">
<img width="698" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/a6e82806-12ca-43e7-8c84-1aa229d9f503">

- The provided Python API code defines request and response handling for GET, POST, and UPDATE methods. Algorithmic conditions within the code determine which Python method to execute based on the incoming request method, enabling proper routing of requests. In VSCode, the algorithmic conditions for validating data on a POST request likely involve checking the data payload against predefined criteria, such as required fields or data formats, to ensure data integrity before processing.

- In Postman, show URL request and Body requirements for GET, POST, and UPDATE methods.
- In Postman, show the JSON response data for 200 success conditions on GET, POST, and UPDATE methods.
![image](https://github.com/Aditi99b/notebook/assets/139928265/73987c23-99f7-4df2-a8f5-366b3d145770)
![image](https://github.com/Aditi99b/notebook/assets/139928265/f8a9dec9-2c8f-44ba-bbed-c8af78a85645)

- This request involves writing code that sends HTTP requests to URLs, specifying the body requirements for GET, POST, and UPDATE methods. In Postman, you can showcase the JSON response data received when these requests return a success status code of 200 for each method, indicating that the requests were processed correctly and the server responded as expected. This demonstration helps ensure the functionality and integrity of the API endpoints under various operations.

- In Postman, show the JSON response for error for 400 when missing body on a POST request.
- In Postman, show the JSON response for error for 404 when providing an unknown user ID to a UPDATE request.
![image](https://github.com/Aditi99b/notebook/assets/139928265/fd96f49a-1c4b-4e2d-81e6-8ae52311f531)

- To create a JSON response for a 400 error when a POST request is missing a body, you would typically craft a JSON object containing an error message or code indicating the bad request due to the absence of required data. In Postman, to simulate a 404 error for an unknown user ID in an UPDATE request, you'd send the request with an invalid user ID, triggering a response containing a JSON object conveying an error message indicating that the requested resource (user) was not found.

### Frontend

- In Chrome inspect, show response of JSON objects from fetch of GET, POST, and UPDATE methods.
<img width="552" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/9afc8d48-c705-45e5-8553-be5774de6539">

- The provided code likely handles JSON responses returned from HTTP requests made using the GET, POST, and UPDATE methods. These methods are commonly used for retrieving, creating, and updating data on a server, respectively. By parsing the JSON objects received from these requests, the code can effectively handle the data exchanged between the client and the server.

- In the Chrome browser, show a demo (GET) of obtaining an Array of JSON objects that are formatted into the browsers screen.
<img width="959" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/0e42afdf-0742-49eb-a01f-2a257a00e79f">

- This code snippet likely refers to a backend endpoint using the HTTP GET method to retrieve data, possibly from a server. The data returned is likely an array of JSON objects formatted for consumption by a web browser. When accessed through a browser, this data would typically be displayed on the screen, potentially as a list or table of information.

- In JavaScript code, describe fetch and method that obtained the Array of JSON objects.
This JavaScript code utilizes the `fetch()` function to send a request to a specified URL (`https://api.example.com/data`). Upon receiving a response, it checks if the response was successful using the `ok` property. If the response is successful, it parses the response body as JSON using the `.json()` method. The parsed JSON data, which is an array of objects, is then accessible in the second `.then()` block. Finally, you can manipulate or utilize this array of JSON objects as needed within your application.

- In JavaScript code, show code that performs iteration and formatting of data into HTML.
![image](https://github.com/Aditi99b/notebook/assets/139928265/caa5a40d-6d32-439b-b26c-3f9b26c3d61e)

- This code iterates through a dataset, likely structured as a collection or array, and formats each piece of data into HTML elements. It likely employs loops or iterators to traverse the data, extracting relevant information and incorporating it into HTML tags such as <div>, <p>, or <table> for display on a web page. This process streamlines the creation of dynamic web content by automating the conversion of raw data into visually appealing HTML structures.

- In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show update. Repeat this demo showing both success and failure.
- In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen.
<img width="604" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/ba9f5090-e151-47de-b96e-825a33ba2a67">

- When the JavaScript code executes successfully in the Chrome Browser, it triggers an alert dialog box to appear on the screen. This dialog box displays a message indicating the probability of getting a score above 9.0, rounded to two decimal places. This immediate pop-up notification provides clear feedback to the user about the successful completion of the operation.

- In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen.
<img width="343" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/9cadf6d4-3547-42b3-8257-c013c58446f5">

- When an error occurs during the execution of the JavaScript code in the Chrome Browser, the .catch() method is triggered. This method logs the error message to the console using console.error().

### Optional/Extra, Algorithm Analysis

- Show algorithms and preparation of data for analysis. This includes cleaning, encoding, and one-hot encoding.

- Cleaning: 
<img width="595" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/9ec20448-f20c-4985-9587-01d45b9e6b54">

- Encoding:
<img width="302" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/97fbcd7d-d276-411c-9dc1-ed3f3c773eb4">

- Show algorithms and preparation for predictions.

- Algorithms 
<img width="238" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/818545e3-46bc-4b61-922b-4944f5c10b43">
Linear regression is chosen as the modeling algorithm for predicting the relationship between features and target due to its simplicity and effectiveness for regression tasks.

- Preparation for Predictions

<img width="308" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/228599b8-3ed9-492a-9a0e-bc332633f575">
Data preprocessing, such as one-hot encoding, is applied to ensure the input data is in a suitable format for the model.

<img width="386" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/da4d8992-a6f7-4b68-84d8-dff82b2dcbf9">
A pipeline is created to streamline the preprocessing and modeling steps, ensuring seamless integration.

<img width="247" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/1159f355-43b2-44ba-8aa6-4a2377f9a4e4">
The pipeline is trained on the training data, enabling both preprocessing and model learning to occur simultaneously.

<img width="341" alt="image" src="https://github.com/Aditi99b/notebook/assets/139928265/6e6d6397-9163-488e-9821-8cf33e1b1fd4">
Predictions are made on new data using the trained pipeline, which automatically applies the necessary preprocessing steps before making predictions.


**Discuss concepts and understanding of Linear Regression algorithms.**
In machine learning, linear regression serves as a foundational algorithm for modeling the relationship between independent variables and a continuous target variable. By fitting a linear equation to the observed data, it enables prediction of outcomes based on input features, making it applicable in diverse domains such as finance, healthcare, and marketing. Linear regression's simplicity, interpretability of coefficients, and ability to capture linear relationships make it a valuable tool for both predictive modeling and understanding the underlying patterns in data.

**Discuss concepts and understanding of Decision Tree analysis algorithms.**
Decision Tree analysis involves recursively partitioning the feature space to construct a tree-like structure where decisions are made at each node based on feature values, leading to interpretable rules for prediction. Its simplicity, interpretability, and ability to handle both numerical and categorical data make it widely applicable across domains such as healthcare, finance, and marketing. Extensions like Random Forests and Gradient Boosting enhance predictive performance by aggregating multiple trees while mitigating overfitting, further expanding its utility in machine learning tasks.


