# Real-Time-Data-Processing-System-for-Weather_Monitoring-with_Rollups_Aggregates
## Overview
- This project implements a Python-based system that tracks real-time weather conditions across multiple cities using the OpenWeatherMap API. It provides features like weather data visualization, daily summaries, trend analysis, and configurable alert notifications for temperature thresholds.

## Key Features
- Live Weather Data: Retrieve up-to-date weather information for multiple cities.
- Daily Summaries: Aggregate temperature data for daily highs, lows, and averages.
- Weather Condition Insights: Highlight the dominant weather patterns across cities.
- Historical Data Visualization: Plot and analyze historical trends.
- Custom Alerts: Get notified when temperature thresholds are exceeded, with optional email alerts.
- Console Alerts: Immediate warnings in the console with the option for email notifications.
- Design Approach
- Modular System:

## The application is structured into modules (e.g., data retrieval, aggregation, alerting, visualization) to ensure scalability and ease of maintenance.
## Concurrent API Requests:
- The project leverages Python’s asyncio and aiohttp libraries to asynchronously fetch data for multiple cities in parallel, improving efficiency.
## Memory and Database Storage:
- Recent weather data is processed in-memory for quick access, while historical data is saved in a SQLite database for long-term analysis.
## Customizable Configuration:
- A configuration file allows users to easily adjust settings such as cities, update intervals, and alert parameters.
## Visualization:
- Matplotlib is used to generate graphs for weather summaries and historical trends, offering clear and meaningful data visualizations.
## Flexible Alerts:
- The system includes a configurable alerting mechanism that can be extended to different notification systems, such as email or SMS.
# Prerequisites
- Python 3.7 or newer
- pip (for package installation)
- Setup Instructions
-Clone the Repository

- Create and Activate a Virtual Environment 
```
python -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
```
- Install Required Packages
```
pip install -r requirements.txt
```
## Configure the System
- Open src/config/config.py and update the following settings:
-  Replace "your_api_key_here" with your OpenWeatherMap API key.
-  Adjust the CITIES list to include the cities you want to track.
-  Modify UPDATE_INTERVAL (in seconds) and ALERT_THRESHOLDS to suit your needs.
## Run the Application
```
python run.py
```
## Configuration Options
- `API_KEY`: Your OpenWeatherMap API key.
- `CITIES`: A list of city names to monitor.
- `UPDATE_INTERVAL`: Time in seconds between weather updates.
- `ALERT_THRESHOLDS`: Temperature values that trigger alerts when exceeded.
## Running Tests
- To execute the test suite:
```
python -m unittest discover tests
```
- Extending the System
- Add More Cities: Update the CITIES list in src/config/config.py.
- Change Alert Settings: Modify ALERT_THRESHOLDS in the same file.
- Enhance Visualizations: Extend the DataVisualizer class located in src/visualization/data_visualizer.py to add new charts or graphs.
## Troubleshooting
- Double-check that your OpenWeatherMap API key is correctly entered in the config file.
- If data isn't being retrieved, ensure your internet connection is stable.
- If you're facing visualization issues, confirm that Matplotlib is correctly installed and functioning.
