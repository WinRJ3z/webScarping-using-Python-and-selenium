# webScarping-using-Python-and-selenium
# Web Scraping with Selenium

This Python program demonstrates web scraping using Selenium to extract data from the ** endoflife.date ** website. In this example, we are scraping end-of-life information for various applications based on the URLs provided in the code. This program is capable of running multiple scrapes concurrently using asyncio and storing the data in a SQLite database.

## Prerequisites

Before running the script, make sure you have the following:

- Python installed (3.7 or higher)
- Selenium library (`pip install selenium`)
- Chrome WebDriver (download from [Chrome WebDriver](https://sites.google.com/chromium.org/driver/))
- SQLite3 (usually comes with Python)
- asyncio libbrary

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/WinRJ3z/webScarping-using-Python-and-selenium
### Navigate to the project directory:

    cd webScarping-using-Python-and-selenium/learning/
### Modify the urls list in the script to include the URLs of the particular application in endoflife.date website you want to scrape:

    urls = [
        ("https://endoflife.date/ruby", "ruby_versions"),
        ("https://endoflife.date/python", "python_versions"),
        # Add more URLs here
    ]
### Run the script:
    Webscraping.py
The script will scrape data from the specified URLs concurrently using asyncio and store it in a SQLite database named Allen.db.

### Database Schema
The SQLite database stores the scraped data in a table with the following schema:

-version (TEXT): Application version
-release_date (TEXT): Release date of the application version
-end_of_life_date (TEXT): End-of-life date of the application version
-latest (TEXT): Latest information
