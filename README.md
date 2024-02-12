# Web Scraping Nepal GDP
import requests module to sent http request 
```python
import requests
```
sending http requests with url = "https://www.worldometers.info/gdp/nepal-gdp/"
```python
requessts.get('url').content
```
BeautifulSoup package is used to pasing the html document
```python
from bs4 import BeautifulSoup
BeautifulSoup(response_data, 'html.parser')
```
finding the table class
```python
soup_data.find(class_ = '<class_table_name>'
```
finding the table head
```python
table_data.find_all('th')
```

