# PSSC Knowledge Archives Scraper

This project is a web scraper designed to extract data from the Philippine Social Science Council (PSSC) Knowledge Archives. The scraper focuses on different sections like the Aghamtao, Philippine Review of Economics, and Philippine Political Science Journal, extracting information such as filenames, file links, and publication years.

## Features

- Scrapes filenames, file links, and publication years from specified sections.
- Automatically corrects and cleans file links.
- Saves the extracted data into CSV files.

## Requirements

- Python 3.x
- BeautifulSoup4
- Requests
- Pandas

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/pssc-scraper.git
    cd pssc-scraper
    ```

2. Create a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

Run the scraper script for different sections by executing:

```bash
python scraper.py
