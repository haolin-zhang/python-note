# Python with Data Analysis

## Common Data Science Specializations

- image recognition
- voice recognition
- medical diagnosis 
- financial analysis/market prediction
- text analysis/chatbots

## Tools Set

- **Atom** (Python IDE)
- **Power BI** (Data Visualization)
- **Amazon RDS** (Database system)
- **Datagrip** (Database IDE)

## Community

**Kaggle** is an online community of data scientists and engineers. Kaggle provides public data sets for data science education study, or competitions to solve data science challenges.

## Popular Libraries

### Data Science

Popular libraries used in Data Science include:

- **NumPy**  
  an open source library for mathematical operations

- **Matplotlib**  
  an open source library for plotting and visualization

- **SciPy**  
  an open source library for statistical analysis

- **Pandas**  
  an open source library for Python, built on top of NumPy library, used for data analysis and manipulation

### Web Scraping

Popular libraries used in Web Scraping include:

- **Requests**  
  a Python HTTP library

- **Beautiful Soup**  
  a Python library for parsing HTML and XML. Together with Requests, are used for data acquisition

Example:

```python
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
```

### Natural Language Processing

Popular libraries used in Natural Language Processing (NLP) include:

- **NLTK**  
  an open source Python library for natural language processing (NLP)

Practical usage scenario: Analyze volume of vocabulary based on a sample of writing paragraph.

### Machine Learning

Libraries used in Machine Learning (ML) include:

- **Scikit-Learn**  
  an open source library for machine learning

Types of machine learning:

- **Supervised Learning**  
  deal with classification or regression problems (data has labels)  
  boundary between right and wrong during prediction is clear  
  common tools: support vector machine (SVM), random forests, navie Bayes

- **Unsupervised Learning**  
  deal with clustering or assocation problems (data has no label)  
  common tools: k-means clustering, hidden markov models

- **Reinforcement Learning**  
  common tools: monte carlo, evolutionary algorithms

- **Deep Learning**  
  a type of machine learning which mocks how brain organizes and works, based on Artificial Neural Network (ANN)


