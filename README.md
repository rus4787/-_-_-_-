# Web Scraping Project: Declaration Data Extraction
## Overview
This project is a web scraping script designed to extract data from the "declaration.rostrud.gov.ru" website. The script uses Selenium and Pandas to navigate through multiple pages of the website, extract data, and save it into CSV files. The data is saved in parts, with each part corresponding to a specific range of pages.

## Requirements
To run this project, you need to have the following Python packages installed:
- selenium
- webdriver-manager
- pandas

You can install these packages using pip: pip install selenium webdriver-manager pandas

## Project Structure
The project consists of a single Jupyter Notebook file (parser.ipynb) that contains the code for web scraping and data extraction.

## How It Works
1. Initialization: The script initializes the Selenium WebDriver and sets up the necessary configurations.
2. Page Navigation: The script iterates through a range of pages, starting from page 3762 up to page 4834. For each page, it loads the URL and extracts the required data.
3. Data Extraction: The script extracts data from each page and appends it to a Pandas DataFrame.
4. Data Saving: After processing a certain number of pages (e.g., every 100 pages), the script saves the collected data into a CSV file. The CSV files are named sequentially (e.g., reestr_data_part_43.csv, reestr_data_part_44.csv, etc.).

## Example Output
The script outputs log messages to the console, indicating the progress of the scraping process. For example:

"""
Загружаем страницу 3762: https://declaration.rostrud.gov.ru/declaration/index?page=3762&per-page=50
Загружаем страницу 3763: https://declaration.rostrud.gov.ru/declaration/index?page=3763&per-page=50
...
Сохраняем данные после страницы 3800...
Данные сохранены в reestr_data_part_43.csv
"""

## Usage
- Clone the Repository: Clone this repository to your local machine.
- Install Dependencies: Ensure you have the required Python packages installed.
- Run the Script: Open the parser.ipynb file in Jupyter Notebook and run the cells to start the scraping process.

## Notes
- The script is designed to handle large volumes of data by saving it in parts. This helps in managing memory usage and allows for resuming the process if interrupted.
- The script assumes that the structure of the website remains consistent across the pages it scrapes. Any changes in the website's structure may require updates to the script.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue if you have any suggestions or improvements.
