# Python with Data Analysis

## Common Data Science Specializations

- image recognition
- voice recognition
- medical diagnosis 
- financial analysis/market prediction
- text analysis/chatbots

## Tools Set

- Atom (Python IDE)
- Power BI (Data Visualization)
- Amazon RDS (Database system)
- Datagrip (Database IDE)

## Community

Kaggle is an online community of data scientists and engineers. Kaggle provides public data sets for data science education study, or competitions to solve data science challenges.

## Popular Libraries

### Data Science

Popular libraries used in data science and engineering fields include:

NLTK is an open source Python library for natural language processing (NLP).

Requests is a Python HTTP library. Beautiful Soup is a Python library for parsing HTML and XML. Together they are used for data acquisition.

Pandas is an open source library for Python, built on top of NumPy library, used for data analysis and manipulation.

Pandas is often used with NumPy (for mathematical operations), Matplotlib (for plotting and visualization), SciPy (for statistical analysis), Scikit-learn (for machine learning).

Pandas provides two data structures for manipulating data: Series and DataFrame.

Series is a one-dimensional labelled array, while the axis label is called "index". Series resembles a column in an Excel sheet.

DataFrame is a two-dimensional table data structure with labeled axes (rows and columns). DataFrame resembles a table in an Excel sheet.

### Web Scraping

Requests: a Python library for retrieving information from websites.
BeautifulSoup: a Python library for parsing HTML and XML

Example:

import requests
from bs4 import BeautifulSoup as beautifulSoup

url = ["http://demo.site.com/data"]

for link in url:
    response = requests.get(link)
    if response.status_code != 200:
        print("Failed to link to website: ", link)
        continue
    
    page = response.text # get HTML page of website
    soup = beautifulSoup(page, "html.parser")
    
    for anchor in soup.find_all("a"):
        print(anchor.get("href", "/"))

### Natural Language Processing

NLTK: an open source Python library for natural language processing (NLP).

Practical usage scenario: Analyze volume of vocabulary based on a sample of writing paragraph.

### Machine Learning

Types of machine learning:

•	Supervised Learning
	deal with classification or regression problems (data has labels)
	boundary between right and wrong during prediction is clear
	common tools: support vector machine (SVM), random forests, navie Bayes

•	Unsupervised Learning
	deal with clustering or assocation problems (data has no label)
	common tools: k-means clustering, hidden markov models

•	Reinforcement Learning
	common tools: monte carlo, evolutionary algorithms

Deep learning:

A type of machine learning which mocks how brain organizes and works, based on artificial neural network (ANN).
