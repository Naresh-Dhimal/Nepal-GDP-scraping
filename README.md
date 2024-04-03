# Web Scraping Nepal GDP
import requests module to sent http request 
```python
import requests
```
sending http requests with url = "https://www.worldometers.info/gdp/nepal-gdp/"
```python
requests.get('url').content
```
BeautifulSoup package is used to pasing the html document
```python
from bs4 import BeautifulSoup
BeautifulSoup(response_data, 'html.parser')
```
finding the table class
```python
soup_data.find(class_ = '<class_table_name>')
```
finding the table head<br>
![image](https://github.com/Naresh-Dhimal/Nepal-GDP-scraping/assets/122601911/395ce972-851f-4da5-a751-a42e074864b5)

to store table header list comprehension is used
```python
table_title = [title.text for title in table_headers]
```
pandas library is used to create DataFrame of table data<br>
![image](https://github.com/Naresh-Dhimal/Nepal-GDP-scraping/assets/122601911/9d71fa1d-dedd-474d-9645-061bdc9a5a9b)

similarly, table row data retrives and store in table_tr<br>
![image](https://github.com/Naresh-Dhimal/Nepal-GDP-scraping/assets/122601911/2d5d142e-8ea4-4c23-ad92-d8408ea70884)

after that table_tr data are store in df dataframe<br>
![image](https://github.com/Naresh-Dhimal/Nepal-GDP-scraping/assets/122601911/65903ca4-40e0-4708-a42a-0029fb3fb49c)

finally, all retrives data are converted in to .csv file
```python
df.to_csv("Nepal GDP.csv", index = False)
```
additionally, .csv file are also store in database file name Nepal Gdb.db
