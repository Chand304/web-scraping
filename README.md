# Web Scraping Practice with Python

## 📌 Project Overview
This project demonstrates basic web scraping using Python. I practiced extracting book information from [Books to Scrape](https://books.toscrape.com/), a website designed for web scraping practice.

The main goal was to understand how to fetch website data, parse HTML, and extract specific information using BeautifulSoup.

## 🛠️ Technologies Used
- Python
- Requests
- BeautifulSoup
- HTML Parsing
- Jupyter Notebook

## 📚 Concepts Learned
- Sending HTTP requests using `requests`
- Fetching website HTML content
- Parsing HTML using BeautifulSoup
- Understanding HTML tags and CSS classes
- Using `find()` and `find_all()`
- Extracting text and HTML attributes
- Using loops to extract multiple records
- Working with lists in Python

## 💻 Code Example

```python
import requests
from bs4 import BeautifulSoup

url = "https://books.toscrape.com/"

response = requests.get(url)

webpage = response.text

soup = BeautifulSoup(webpage, "html.parser")

book = soup.find_all('article', class_='product_pod')

name = []

for i in book:
    title = i.find('h3').find('a')['title']
    name.append(title)

print(name)
```

## 🎯 Project Objectives
- Extract book titles from a website.
- Understand HTML structure.
- Practice web scraping fundamentals.
- Improve Python programming skills.

## 🚀 Future Improvements
- Extract book prices.
- Extract book ratings.
- Extract availability status.
- Scrape multiple pages.
- Save extracted data into CSV files using Pandas.

## 📖 Practice Website
[Books to Scrape](https://books.toscrape.com/)

## 👨‍💻 Author
Python and Machine Learning Learner

---

**Note:** This project is created for educational and web scraping practice purposes.
