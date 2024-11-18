# AO3 Webscraper

This is an **unfinished** web scraper designed to extract data from [AO3](archiveofourown.org). This project uses Python and libraries such as `Selenium`, `BeautifulSoup`, and `pandas` to scrape fanfiction data from **Archive of Our Own (AO3)**. The script extracts details about works including titles, authors, summaries, tags, publication dates, and kudos.
This is in preparation for a personal project to create an AO3 recommender system.

---

## Features

- Automates webpage navigation using `Selenium`.
- Extracts structured data using `BeautifulSoup`.
- Outputs scraped data to a `pandas` DataFrame for further analysis or storage.

---

## Requirements

### Python Packages

Install the required Python libraries:

```bash
pip install selenium beautifulsoup4 pandas
  ```
---

## Browser and WebDriver

Ensure you have:

1. **Google Chrome** installed on your system.
2. The compatible **ChromeDriver** for Selenium. [Download ChromeDriver](https://sites.google.com/chromium.org/driver).
3. Add ChromeDriver to your system PATH or specify its location in the script.

---

## How It Works

1. **Initialize the WebDriver**: The script launches Chrome using Selenium.
2. **Navigate Pages**: The URL of the first search page is dynamically updated to iterate through multiple pages.
3. **Scrape Data**:
    - Extracts data for works listed on each page, including:
      - **Title**
      - **Author**
      - **Summary**
      - **Tags**
      - **Publication Date**
      - **Kudos**
4. **Save Data**: The extracted data is stored in a `pandas` DataFrame for further processing.

---

## Usage

1. Modify the `url` variable with your desired AO3 search query.
2. Adjust the range in the loop to scrape more or fewer pages.
3. Run the script:

   ```bash
   python ao3_scraper.py
     ```

---

## Example Output

The script generates a DataFrame with the following columns:

- **Title**: The title of the work.
- **Author**: The author's name (or `N/A` if unavailable).
- **Summary**: A brief summary of the work.
- **Tags**: Associated tags for the work.
- **Publication Date**: The date the work was published.
- **Kudos**: The number of kudos received (or `N/A` if unavailable).

---

## Notes

- **Respect AO3's Terms of Service**: Avoid excessive scraping to prevent overloading the server.
  - Use reasonable delays (`time.sleep`) between requests.
  - Limit the number of pages to scrape as needed.
- **Error Handling**: Add error handling to manage connection issues or changes to AO3's HTML structure.

---

## Customization

- **Change Fandom or Filters**: Update the search parameters in the URL to match your preferred fandom or filters.
- **Save to File**: Export the DataFrame to CSV or Excel using:

   ```python
   df.to_csv('ao3_data.csv', index=False)
    ```

---

Happy scraping! 🎉