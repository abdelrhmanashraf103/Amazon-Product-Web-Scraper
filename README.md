🛒 Amazon Product Web Scraper
🚀 Project Overview

This project is a web scraping script built with Python, BeautifulSoup, and Requests to extract detailed product information from Amazon product pages. The goal is to automate product data collection (title, price, ratings, reviews, description, and features) and save it into a CSV file for further analysis.

This scraper can be used by shoppers, data analysts, or businesses to:

Track price changes over time 📉📈

Compare competing products 🔍

Collect structured data for market research 📊

🔧 Tech Stack & Libraries

Python 🐍

Requests → Sending HTTP requests

BeautifulSoup (bs4) → HTML parsing & data extraction

Time → Request delays to avoid blocking

CSV → Storing structured product data

📥 Data Extraction Workflow

Send Request to Amazon

A User-Agent header is added to mimic a browser and avoid being blocked.

The script checks the HTTP status code and handles cases like 403 (Blocked) or 503 (Server unavailable) gracefully.

Parse HTML with BeautifulSoup

Extracts multiple product details such as:
✅ Product Title (id="productTitle")
✅ Product Price (class="a-price-whole")
✅ Product Rating (id="acrPopover")
✅ About this Product (a-unordered-list a-vertical a-spacing-mini)
✅ Product Description (id="productDescription")
✅ Customer Reviews (id="cm-cr-dp-review-list")

Data Validation

If an element is not found, the script prints a warning with debugging tips (e.g., “Inspect the HTML manually”).

Save Results in CSV

Extracted product details are written into a CSV file (amazon_airpod_pro_max.csv) for structured storage.

Columns include:

product_title

product_price

product_rate

product_info

product_description

product_review

📊 Example Use Case

For the Apple AirPods Pro Max product page, the script extracts:

Title → Apple AirPods Pro Max with Active Noise Cancellation 🎧

Price → ₹59,900

Rating → 4.5 out of 5 stars ⭐

Features → “Active Noise Cancellation, Transparency Mode, Personalized Spatial Audio…”

Description → Long product description from Amazon

Reviews → Recent customer feedback

📌 Key Learnings

✔️ How to send safe requests with headers & delays
✔️ How to parse structured & unstructured data from HTML
✔️ Best practices for handling missing elements in scraping
✔️ Writing clean datasets into CSV format for further analysis

⚠️ Important Notes

Amazon actively blocks scraping. Always respect robots.txt and Terms of Service.

For production usage, consider Selenium, Proxies, or Rotating User-Agents to handle dynamic content and prevent blocking.

🌟 Why This Project Matters

This project demonstrates real-world data collection & automation skills that can be applied in:

E-commerce Analytics

Price Monitoring Systems

Competitor Benchmarking

Customer Sentiment Analysis

It’s a solid foundation for data-driven decision-making in retail and marketing.
