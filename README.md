# 510lab2final
# Event Weather Information Script

## Overview
This Python script is designed for extracting event information from a specified website and augmenting this data with weather forecasts based on the event's location and date. It achieves this by scraping event data, determining geographical coordinates, and fetching weather information from the National Weather Service API.

## Requirements
- Python 3.x
- Libraries: `requests`, `bs4` (BeautifulSoup), `pandas`, `geopy`
- An internet connection for API access and web scraping

## Installation
To install the necessary libraries, run the following commands in your terminal:

```bash
pip install -r requirements.txt
pip install geopy
Features
Scrapes event URLs from "https://visitseattle.org/events".
Fetches geographical coordinates for event locations.
Retrieves weather forecasts for the event's date and location.
Saves the enhanced event data with weather information into a CSV file.
Usage
Run the script to start data extraction and processing. The script will generate an output file named updated_csv_file3.csv containing the event data along with the associated weather forecasts.

## Functions

get_weather(latitude, longitude): Fetches the temperature for given coordinates.
get_coordinates(location): Converts a location into geographical coordinates.
format_date(date_str): Formats date strings into a standardized format.
get_weather(lat, lon, date): Retrieves a detailed weather forecast for the specified date and coordinates.
## Data Flow
The script iterates over multiple pages of the event website to collect event URLs.
It then determines the geographical coordinates of each event location.
For each event, the script fetches the weather forecast for the event's date.
Finally, the script compiles all the data into a CSV file.
## Output
updated_csv_file3.csv: A CSV file containing event details along with weather forecasts.
## Note
The script includes a sleep function (commented out) to avoid overwhelming the server during web scraping.
Error handling is in place for HTTP requests and date formatting.
The script is structured to fetch the weather forecast closest to each event's date, considering if it's daytime.
Contribution
Suggestions and improvements are welcome. Feel free to fork this project and submit your contributions via pull requests.
