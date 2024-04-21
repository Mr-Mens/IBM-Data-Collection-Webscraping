# SpaceX Falcon 9 First Stage Landing Prediction: Web Scraping Lab

## Overview

This repository is designed to assist in the collection of Falcon 9 and Falcon Heavy launch records via web scraping from a dedicated Wikipedia page. The purpose is to predict the landing success of SpaceX's Falcon 9 first stage, a critical aspect given the cost implications of rocket reusability.

## Repository Contents

- `README.md` - Provides detailed instructions for executing the lab tasks.
- `scrape_data.py` - Python script for web scraping launch data.
- `requirements.txt` - List of required Python libraries.

## Prerequisites

Ensure Python (version 3.8 or newer is recommended) is installed along with the necessary packages:

```bash
pip install -r requirements.txt
```

## Lab Objective

The aim of this lab is to perform web scraping to extract historical launch records of Falcon 9 and Falcon Heavy rockets from Wikipedia, process the data, and prepare it for predictive modeling on landing outcomes.

### Estimated Time to Complete: 40 minutes

## Instructions

### Step 1: Environment Setup

Clone the repository and install the required Python libraries:

```bash
git clone https://github.com/your-username/spacex-web-scraping-lab.git
cd spacex-web-scraping-lab
pip install -r requirements.txt
```

### Step 2: Perform Web Scraping

Execute the `scrape_data.py` script to start the web scraping process:

```bash
python scrape_data.py
```

This script will:
- Fetch the HTML content of the Wikipedia page containing Falcon 9 and Falcon Heavy launch records.
- Parse the HTML to extract data about each launch.
- Convert the data into a structured format and store it in a CSV file.

### Step 3: Data Exploration

After collecting the data, explore the structured dataset:

```python
import pandas as pd
data = pd.read_csv('spacex_web_scraped.csv')
print(data.head())
```

## Tasks Overview

1. **Web Scraping**: Automate data collection from the Wikipedia page using `BeautifulSoup`.
2. **Data Parsing**: Extract relevant information and convert it into a structured Pandas DataFrame.
3. **Data Cleaning**: Handle inconsistencies and prepare the dataset for analysis.

## Expected Outputs

The script should output a CSV file named `spacex_web_scraped.csv`, containing the following information for each launch:

- Flight Number
- Date
- Time
- Booster Version
- Launch Site
- Payload
- Payload Mass
- Orbit
- Customer
- Launch Outcome
- Booster Landing

## Data Fields

Each field in the dataset provides insights into the launch specifics:

- **Flight Number**: Identifier for the launch attempt.
- **Date and Time**: Scheduled date and time of the launch.
- **Booster Version**: Specific version of the Falcon booster used.
- **Launch Site**: Geographical launch location.
- **Payload**: Name and type of the payload.
- **Payload Mass**: Mass of the payload in kilograms.
- **Orbit**: Targeted orbital destination.
- **Customer**: Client for whom the launch is conducted.
- **Launch Outcome**: Result of the launch (e.g., success, failure).
- **Booster Landing**: Outcome of the booster landing attempt.

## Authors

- [Yan Luo](https://www.linkedin.com/in/yan-luo-96288783/) - Data Scientist at IBM, specializing in data extraction and analysis.
- [Nayef Abou Tayoun](https://www.linkedin.com/in/nayefaboutayoun/) - Data Analyst at IBM, focusing on predictive modeling and data analytics.

## Change Log

| Date (YYYY-MM-DD) | Version | Changed By       | Change Description                |
|-------------------|---------|------------------|-----------------------------------|
| 2021-06-09        | 1.0     | Yan Luo          | Updated tasks and review materials|
| 2020-11-10        | 1.0     | Nayef Abou Tayoun| Created initial lab instructions  |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details. 

Forks, contributions, and feedback are welcome to improve the lab and its related materials.
