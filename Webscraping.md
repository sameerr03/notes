A method to get information by running a webscraper that gets information of a website and parses it

# financials
```
import requests
from bs4 import BeautifulSoup

income_statement={}

url="https://finance.yahoo.com/quote/MSFT/financials?p=MSFT"
headers={"User-Agent":"Chrome/114.0.5735.134"}
webpage_MSFT=requests.get(url, headers=headers)
page_content=webpage_MSFT.content

soup=BeautifulSoup(page_content,"html.parser")
tabl=soup.find_all("div",{"class":"M(0) Whs(n) BdEnd Bdc($seperatorColor) D(itb)"})
for t in tabl:
    rows=t.find_all("div",{"class":"D(tbr) fi-row Bgc($hoverBgColor):h"})
    for row in rows:
        income_statement[row.get_text(separator="|").split("|")[0]]=row.get_text(separator="|").split("|")[1]
        

```

This gets the information from yahoo finance about microsoft income statement. 

headers is used to bypass yahoo finance from blocking web scrapers
the code in class is based on patterns that occur in the website in order to store the information. the occurrences of these strings in the code is iterated through and thus text and thereby relevant information that is stored on the website can be extracted. 

The following code scrapes the cash flow, balance sheet and the income statement data for multiple stocks and stores each type of financial metric in a dataframe

```
import requests
from bs4 import BeautifulSoup
import pandas as pd

stocks=["AAPL","MSFT","HDFCBANK.NS"]
incomest_dict={}
bs_dict={}
cf_dict={}

for ticker in stocks:
    # income statement webscraper
    incomest={}
    hrow={}
    url="https://finance.yahoo.com/quote/{}/financials?p={}".format(ticker, ticker)
    headers={"User-Agent":"Chrome/114.0.5735.134"}
    webpage=requests.get(url, headers=headers)
    soup=BeautifulSoup(webpage.content,"html.parser")
    tabl=soup.find_all("div",{"class":"M(0) Whs(n) BdEnd Bdc($seperatorColor) D(itb)"})
    for t in tabl:
        heading = t.find_all("div",{"class":"D(tbr) C($primaryColor)"})
        for trow in heading:
            hrow[trow.get_text(separator="|").split("|")[0]]=trow.get_text(separator="|").split("|")[1:]
        rows=t.find_all("div",{"class":"D(tbr) fi-row Bgc($hoverBgColor):h"})
        for row in rows:
            incomest[row.get_text(separator="|").split("|")[0]]=row.get_text(separator="|").split("|")[1:]
    temp=pd.DataFrame(incomest).T
    temp.columns=hrow["Breakdown"]
    incomest_dict[ticker]=temp
    
for ticker in stocks:
    # balance sheet webscraper
    bs={}
    hrow={}
    url="https://finance.yahoo.com/quote/{}/balance-sheet?p={}".format(ticker, ticker)
    headers={"User-Agent":"Chrome/114.0.5735.134"}
    webpage=requests.get(url, headers=headers)
    soup=BeautifulSoup(webpage.content,"html.parser")
    tabl=soup.find_all("div",{"class":"M(0) Whs(n) BdEnd Bdc($seperatorColor) D(itb)"})
    for t in tabl:
        heading = t.find_all("div",{"class":"D(tbr) C($primaryColor)"})
        for trow in heading:
            hrow[trow.get_text(separator="|").split("|")[0]]=trow.get_text(separator="|").split("|")[1:]
        rows=t.find_all("div",{"class":"D(tbr) fi-row Bgc($hoverBgColor):h"})
        for row in rows:
            bs[row.get_text(separator="|").split("|")[0]]=row.get_text(separator="|").split("|")[1:]
    temp=pd.DataFrame(bs).T
    temp.columns=hrow["Breakdown"]
    bs_dict[ticker]=temp
    
for ticker in stocks:
    #cash flow web scraper
    cf={}
    hrow={}
    url="https://finance.yahoo.com/quote/{}/cash-flow?p={}".format(ticker, ticker)
    headers={"User-Agent":"Chrome/114.0.5735.134"}
    webpage=requests.get(url, headers=headers)
    soup=BeautifulSoup(webpage.content,"html.parser")
    tabl=soup.find_all("div",{"class":"M(0) Whs(n) BdEnd Bdc($seperatorColor) D(itb)"})
    for t in tabl:
        heading = t.find_all("div",{"class":"D(tbr) C($primaryColor)"})
        for trow in heading:
            hrow[trow.get_text(separator="|").split("|")[0]]=trow.get_text(separator="|").split("|")[1:]
        rows=t.find_all("div",{"class":"D(tbr) fi-row Bgc($hoverBgColor):h"})
        for row in rows:
            cf[row.get_text(separator="|").split("|")[0]]=row.get_text(separator="|").split("|")[1:]
    temp=pd.DataFrame(cf).T
    temp.columns=hrow["Breakdown"]
    cf_dict[ticker]=temp
    
#Conversion of values in the dataframe to numeric type from objects
for ticker in stocks:
    for col in incomest_dict[ticker].columns:
        incomest_dict[ticker][col]=incomest_dict[ticker][col].str.replace('-','')
        incomest_dict[ticker][col]=incomest_dict[ticker][col].str.replace(',','')
        incomest_dict[ticker][col]=pd.to_numeric(incomest_dict[ticker][col],errors="coerce")

for ticker in stocks:
    for col in bs_dict[ticker].columns:
        bs_dict[ticker][col]=bs_dict[ticker][col].str.replace('-','')
        bs_dict[ticker][col]=bs_dict[ticker][col].str.replace(',','')
        bs_dict[ticker][col]=pd.to_numeric(bs_dict[ticker][col],errors="coerce")
        
for ticker in stocks:
    for col in cf_dict[ticker].columns:
        cf_dict[ticker][col]=cf_dict[ticker][col].str.replace('-','')
        cf_dict[ticker][col]=cf_dict[ticker][col].str.replace(',','')
        cf_dict[ticker][col]=pd.to_numeric(cf_dict[ticker][col],errors="coerce")
```

The final part of the code converts the data that is extracted from object type to numeric type so that it can be easily manipulated.

# statistics
```
import requests
from bs4 import BeautifulSoup

stats_dict={}
ticker="AAPL"
stocks=["AAPL","MSFT","HDFCBANK.NS"]
for ticker in stocks:
    # income statement webscraper
    stats={}
    hrow={}
    url="https://finance.yahoo.com/quote/{}/key-statistics?p={}".format(ticker, ticker)
    headers={"User-Agent":"Chrome/114.0.5735.134"}
    webpage=requests.get(url, headers=headers)
    soup=BeautifulSoup(webpage.content,"html.parser")
    tabl=soup.find_all("table",{"class":"W(100%) Bdcl(c)"})
    for t in tabl:
        rows=t.find_all("tr")
        for row in rows:
            stats[row.get_text(separator="|").split("|")[0]]=row.get_text(separator="|").split("|")[-1]
    stats_dict[ticker]=stats
```

-1 is put in the term to adapt to the code of the website 