1. High-Rated Books Scraper

This Python script is a web scraper designed to extract the titles of books with 4 or 5-star ratings from the website books.toscrape.com. It uses the requests library to fetch the HTML content of each page and BeautifulSoup (bs4) to parse and navigate the HTML structure, effectively acting as a data extractor. This project serves as an excellent, real-world example of how to combine these two powerful libraries for web scraping.

Key Features

- Multi-Page Scraping: The script iterates through the first 50 pages of the website to ensure comprehensive data collection. This demonstrates how to handle pagination, a common challenge in web scraping.

- Targeted Data Extraction: It specifically looks for books with a high rating by checking for CSS classes like .star-rating.Four or .star-rating.Five. This highlights the precision of CSS selectors for finding specific elements.

- Structured Data Storage: The titles of the highly-rated books are stored in a Python list (titulos_rating_alto), which can then be easily processed, saved to a file, or used for further analysis.

- Simple & Effective: The code is straightforward, making it an ideal project for beginners to understand the core concepts of web scraping: fetching a page, parsing its content, and extracting specific information.

How to Run the Script

- Dependencies: You need to have Python installed, along with the requests and beautifulsoup4 libraries. If you don't have them, you can install them via pip:

      Bash
      
      pip install requests beautifulsoup4
  
- Save the Code: Save the code as a Python file (e.g., scraper.py).

- Execute: Run the script from your terminal.

      Bash
      
      python scraper.py
  
  The script will print the title of each 4 or 5-star book directly to your console.

Important Notes

- Website's Terms of Service: Always check a website's robots.txt file and terms of service before scraping. This project uses a dummy website specifically designed for scraping practice, but for real-world applications, it's crucial to be mindful of legal and ethical considerations.

- Dynamic Websites: This script works well for static websites like books.toscrape.com. For websites that load content dynamically with JavaScript, you might need more advanced tools like Selenium to simulate a browser.


2. Website Image Downloader

This Python script is a simple web scraper that downloads the image of the first course listed on the website escueladirecta.com. It's a clear and concise demonstration of how to use requests to fetch web content and BeautifulSoup (bs4) to parse HTML, locate a specific element, and then download the image file linked in that element. This is a practical example of web scraping for a specific, non-textual piece of data.

How It Works

- Fetch HTML: The requests.get() function retrieves the entire HTML content of the specified URL.

- Parse with BeautifulSoup: bs4.BeautifulSoup() parses the raw HTML text, turning it into a structured object (sopa) that's easy to navigate.

- Locate the Image URL: The script uses a CSS selector '.course-box-image' to find the HTML element that contains the course image. It then accesses the src attribute of the first element found ([0]['src']) to get the direct URL of the image.

- Download and Save: A second requests.get() call is made to download the image file itself using its URL. The content of this response is then written to a new file named mi_imagen.jpg in binary write mode ('wb'), which ensures the image is saved correctly.

Instructions for Use

- Dependencies: You need to have Python 3, requests, and beautifulsoup4 installed. If you don't have them, run the following commands:

      Bash
      
      pip install requests beautifulsoup4
  
- Save the Script: Save the code as a Python file (e.g., download_image.py).

- Run: Execute the script from your terminal:

      Bash
      
      python download_image.py
  
    Once the script finishes, you will find a new file named mi_imagen.jpg in the same directory, which is the downloaded image from the website.
