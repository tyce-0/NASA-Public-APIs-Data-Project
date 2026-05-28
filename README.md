# NASA-Public-APIs-Data-Project
NASA Space Data Exploration Project

This project demonstrates how to work with NASA’s public APIs to retrieve, process, visualize, and export real-world space data using Python.

The project focuses on:

Accessing APIs with authentication keys
Fetching astronomy data from NASA servers
Displaying NASA’s Astronomy Picture of the Day (APOD)
Extracting asteroid data from the NeoWs API
Cleaning and transforming JSON data into a structured pandas DataFrame
Exporting processed data into CSV format for further analysis and sharing

📌 Project Objectives

The main objective of this project is to practice:
API consumption using Python
Working with JSON responses
Data preprocessing and cleaning
Data transformation using pandas
Exporting datasets into CSV files

This project simulates a real-world data engineering and data analysis workflow where data is collected from an external source, transformed into usable formats, and prepared for downstream analysis.


🛰️ APIs Used
1. Astronomy Picture of the Day (APOD)

The APOD API provides daily astronomy-related images along with descriptions written by professional astronomers.

Used for:

Fetching NASA’s daily astronomy image
Displaying image data inside a Jupyter Notebook

Official API Documentation:

NASA APOD API Documentation

2. Asteroids NeoWs API- NeoWs (Near Earth Object Web Service) provides asteroid-related information including:

Asteroid IDs
Estimated diameters
Relative velocity
Magnitude measurements

Used for:

Retrieving asteroid datasets
Performing data cleaning and preprocessing
Creating a structured pandas DataFrame

Official API Documentation:

NASA NeoWs API Documentation

🛠️ Technologies and Libraries used 

Python - The Main programming language
requests - For API communication
pandas - For Data manipulation
matplotlib - Image visualization
Pillow (PIL) - Image processing


🔑 API Authentication
NASA APIs require an API key for authentication and usage tracking.
An API key was generated through the NASA API portal:

NASA API Portal

The API key is stored securely inside a Python variable before making requests.

# Step 1 — Import Required Libraries

The necessary Python libraries were imported to handle:

API requests
Data processing
Image visualization
import requests
import pandas as pd
import matplotlib.pyplot as plt
from PIL import Image
from io import BytesIO

# Step 2 — Retrieve Astronomy Picture of the Day

A GET request was sent to NASA’s APOD endpoint using the requests library.

Tasks Performed
Connected to NASA API
Retrieved JSON response
Extracted image URL
Downloaded and displayed image inside notebook



The returned image URL was processed and visualized using matplotlib.

Tasks Performed
Downloaded image content
Opened image using Pillow
Rendered image inside notebook
☄️ Asteroid Data Processing

# Step 4 — Access NeoWs API

A request was sent to the NeoWs endpoint to retrieve asteroid information.


# Step 5 — Extract Relevant Asteroid Fields

The API response contained nested JSON structures.

The following fields were extracted:

Field	Description
Asteroid ID	Unique asteroid identifier
Asteroid Name	Official asteroid name
Minimal Estimated Diameter (km)	Minimum estimated size
Absolute Magnitude	Brightness measurement
Relative Velocity (km/h)	Speed relative to Earth

# Step 6 — Data Cleaning and Transformation

The raw JSON data was transformed into a structured list before converting into a pandas DataFrame.

 I  extracted Extracted nested values,Handled missing values and removed incomplete rows then Converted velocity column into numeric datatype during the preprocessing stage.

📊 Final DataFrame Structure
Asteroid ID	Asteroid Name	Minimal Estimated Diameter (km)	Absolute Magnitude	Relative Velocity (km/h)

The final dataset was clean, structured, and ready for analysis.

 # Exporting the clean Data

The cleaned dataset was exported into CSV format for sharing and future analysis.

📈 Key Skills Demonstrated

This project demonstrates practical skills in:

API integration
JSON parsing
Data preprocessing
Data transformation
Data visualization
Data export workflows
Real-world dataset handling
