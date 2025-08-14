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
1. Create your accounts & install tools
A. Create your OpenWeather account & API key
```
https://openweathermap.org/api
```
Go to OpenWeather and register for a free account, then verify your email.

On your account page, find your API key (sometimes called APPID). Keep it handy.

<img width="905" height="401" alt="Image" src="https://github.com/user-attachments/assets/06233bae-2e4e-4f15-b1f5-5be27dfd7e6d" />


B. Create Access key for this IAM user and download the .csv with the Access Key ID and Secret Access Key.

You’ll only see the secret once—store it safely.
1. Clone the repository:
--bash
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git

3. Install dependencies:
   pip install -r requirements.txt

4. Configure environment variables (.env):
   OPENWEATHER_API_KEY=your_api_key
AWS_BUCKET_NAME=your_bucket_name

4.Configure AWS credentials:
aws configure

5. Run the application:
python src/weather_dashboard.py

## What I Learned

AWS S3 bucket creation and management
Environment variable management for secure API keys
Python best practices for API integration
Git workflow for project development
Error handling in distributed systems
Cloud resource management

## Future Enhancements

Add weather forecasting
Implement data visualization
Add more cities
Create automated testing
Set up CI/CD pipeline
     


