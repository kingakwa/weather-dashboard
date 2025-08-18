# Weather Data Collection System

## Project Overview
This project is a Weather Data Collection System that demonstrates core DevOps principles by combining:

- External API Integration (OpenWeather API)
- External API Integration (OpenWeather API)
- Cloud Storage (AWS S3)
- Infrastructure as Code
- Version Control (Git)
- Python Development
- Error Handling
- Environment Management

## Features
- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in AWS S3
- Supports multiple cities tracking
- Timestamps all data for historical tracking

## Technical Architecture
- Language: Python 3.x
- Cloud Provider: AWS (S3)
- External API: OpenWeather API
- VScode for coding
- Dependencies:
   - boto3 (AWS SDK)
   - python-dotenv
   - requests

 <img width="438" height="205" alt="Image" src="https://github.com/user-attachments/assets/556eb1c4-75e4-4376-b241-367292fb62db" />

 ## Project Structure
weather-dashboard/
  src/
    __init__.py
    weather_dashboard.py
  tests/
  data/
  .env
  .gitignore
  requirements.txt
  

<img width="934" height="347" alt="Image" src="https://github.com/user-attachments/assets/f9e966b4-878e-4f99-8de9-fac3667e8b6b" />

  
## Setup Instructions
**1. Create your accounts & install tools**
A. Create your OpenWeather account & API key
```
https://openweathermap.org/api
```
- Go to OpenWeather and register for a free account, then verify your email.
- On your account page, find your API key (sometimes called APPID). Keep it handy.

<img width="905" height="401" alt="Image" src="https://github.com/user-attachments/assets/06233bae-2e4e-4f15-b1f5-5be27dfd7e6d" />


B. Create Access key for this IAM user and download the .csv with the Access Key ID and Secret Access Key.
   **You’ll only see the secret once—store it safely.**
   
**2. Clone the repository:**
```
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git
``` 
**3. Install dependencies:**
   ```
   pip install -r requirements.txt
   ```
   This will install:   
    -boto3 (AWS SDK for Python),
     -requests (HTTP),
      -python-dotenv (loads secrets from .env). PyPI
   
**4. Configure environment variables (.env):**
   ```
   echo "OPENWEATHER_API_KEY=your_api_key"
   echo "AWS_BUCKET_NAME=your_bucket_name"
   ```
   - The starter app includes defaults. If you want to change them, open src/weather_dashboard.py and look for a CITIES list—edit/add city names like "London", "Douala", "New York". Save the file.
   - make sure your bucket name is unique.
   -  Test your OpenWeather key (sanity check)
Run a quick request in your terminal (replace the key and city):
  ```
 curl "https://api.openweathermap.org/data/2.5/weather?q=Douala&appid=YOUR_OPENWEATHER_KEY_HERE&units=metric"
  ```
-You should see JSON output with weather fields (name, main.temp, weather[0].description, etc.).

-If you get an error like {"cod":401, "message":"Invalid API key"}, double-check the key and that your email is verified.

<img width="744" height="71" alt="Image" src="https://github.com/user-attachments/assets/711e2943-b253-44d5-b420-32e03bab5680" />


**5.Configure AWS credentials:**
aws configure

**6.Run the application:**
```  
python src/weather_dashboard.py
```

## Expected behavior:

- The script prints statuses (fetching each city).
- It writes timestamped JSON files into a local data/ folder.
- It uploads those JSON files into your S3 bucket.

  <img width="572" height="265" alt="Image" src="https://github.com/user-attachments/assets/1fc87916-045b-4b0b-b41f-05b4302788aa" />

7. Verify your S3 uploads
- In the AWS Console
- Open S3 → your bucket → you should see objects under a folder path like weather/YYYY/MM/DD/… (structure may vary).

8. push content of on your local mechine (VScode) to your git repo
   
   <img width="678" height="154" alt="Image" src="https://github.com/user-attachments/assets/e9199d76-082f-4379-b345-0b40466f875c" />
  
## What I Learned

- AWS S3 bucket creation and management
- Environment variable management for secure API keys
- Python best practices for API integration
- Git workflow for project development
- Error handling in distributed systems
- Cloud resource management

## Future Enhancements

Add weather forecasting
Implement data visualization
Add more cities
Create automated testing
Set up CI/CD pipeline
     






