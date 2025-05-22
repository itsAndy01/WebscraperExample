import re ##replace white space 
import requests  ###scrape libray 
from bs4 import BeautifulSoup     ##libray - parsing or cleaning  
url = "https://edition.cnn.com/travel/article/scenic-airport-landings-2020/index.html"
response = requests.get(url)
####print(response.text)
if response.status_code == 200:
    #Example of finding all the h1 tags
    soup = BeautifulSoup(response.text, "html.parser")
    # get title
    title = soup.find("h1").get_text()
    print(title)
    main = soup.find("article").get_text()
    new = re.sub(r'\n{2,}', '\n\n', main)
    print(new)
else: "connection not created"
