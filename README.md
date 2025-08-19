# DATA CRAPER: A Web Scraping Tool

"DATA CRAPER" is a Python-based web scraping tool designed to extract tabular data from websites and save it into CSV files. This project was developed by Rizul Sharma. The primary goal is to automate the process of data collection from web pages for data analysis and other purposes.

## Features

* **Web Scraping:** Extracts data from any given URL.
* **Table Detection:** Automatically identifies and extracts all tables on a webpage.
* **CSV Conversion:** Converts the extracted HTML tables into structured CSV files.
* **Ease of Use:** Simple to use with a command-line interface.

## Technologies Used

* **Python 3.8**
* **Libraries:**
    * **BeautifulSoup**: For parsing HTML.
    * **Pandas**: For creating and managing CSV files.
    * **Requests**: For making HTTP requests.

## Getting Started

### Prerequisites

Make sure you have Python 3 installed on your system. You can download it from [python.org](https://www.python.org/).

### Installation

1.  Clone the repository to your local machine:
    ```sh
    git clone https://github.com/anij715/DataCraper.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd DataCraper
    ```
3.  Install the required Python libraries:
    ```sh
    pip install -r requirements.txt
    ```
    *(Note: You will need to create a `requirements.txt` file containing the necessary libraries: `requests`, `pandas`, and `beautifulsoup4`)*

## Usage

You can use the script from the command line by providing a URL.

```sh
python data_craper.py <URL>
```
Replace `<URL>` with the URL of the webpage you want to scrape. The script will then find all the tables on that page and save them as `table-1.csv`, `table-2.csv`, and so on, in the same directory.

### How It Works
The script sends an `HTTP GET` request to the specified URL to retrieve the HTML content. It then uses the BeautifulSoup library to parse the HTML and find all `<table>` tags. For each table found, it extracts the headers (from `<th>` tags) and the rows (from `<tr>` and `<td>` tags). Finally, it uses the Pandas library to organize the data and save it as a `CSV` file.

## Acknowledgments
This project was submitted as part of the Bachelor's Degree in Computer Science & Engineering at KIIT Deemed to be University under thr guidance of Prof. Sujoy Datta.
[Full Report](https://www.researchgate.net/publication/341949318_DATA_CRAPER)
