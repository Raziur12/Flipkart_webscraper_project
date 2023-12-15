# Flipkart_webscraper_project
# Web Scraper using Beautiful Soup, Selenium and requests for RPA(Automation) form Flipkart 

![image](https://github.com/Raziur12/Flipkart_webscraper_project/assets/153851061/3b4dd50f-f152-4a34-921a-83c7d1efc71e)


Let's see overall, open a Flipkart website and search a any things, like that mobile phone,gaming products etc.
Now Inspact the page of that product and check the specific thing , for example:- MRP, Title etc.
After inspact the page then see where is the MRP content, if MRP inside the span tag then,
<span class="a-offscreen"> Rs 9,499.00 </span>, here span is the Tag, a-offscreen is the attribute and Rs9,499.00 is the content of the HTML/CSS.
# Requriments
i) Python (3.5 or higher version)
ii) Jupyter Notebook
Open the jupyter notebook and create a new file as a Flipkart_webscraper.ipynb
# First install requriments libraries 
i) pip install requests
ii) pip install beautifulsoup or pip install bs4
iii) pip install pandas
iv) pip install numpy
Explain :- 
BeautifulSoup is a library that you can use to pass the HTML code and find the elements inside it.
Install requests becouse you will be sending requests from local PC to Flipkart website.
Third thing we need to install is pandas becouse when you scrape the Data from online we need to convert ot into the CAC(Customer Aquistion Cost) format and we will using pandas to convert those text Data into proper data form and then Store it into CSV.
# Note:-
Define is HTTP header so whenever we visite any website on the internet, you send HTTP request to it,HTTP request contains a lot of different things and one of them is header inside the header you will find a lot of different things and one of the most important thing in that is user agent, user agent tells that you are trying to access this website and you are a genuine user by identifying your browser information and show me of the other information requried to access the website.
# Let's start, Import all libraries inside the project file
from bs4 import BeautifulSoup as bs
import requests as r
import pandas as pd
# Create a variable name as URL to store the all information of Flipkart website

URL = "https://www.flipkart.com/search?q=gaming&otracker=search&otracker1=search&marketplace=FLIPKART&as-show=on&as=off"
# Create a variable name as HEADERS for get the HTTP response
HEADERS = {
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36',
    'Accept-Language': 'en-US, en;q=0.5',
}
# Now crate a variable name as webpage to send to request using get method and fatch the all information of the URL and also get the 200 response 
# Let's see
webpage = r.get(URL, headers=HEADERS)
run the webpage and check you get the response 200 or not, if you get 200 response that means your code running successfully.
webpage
![Uploading image.png…]()
