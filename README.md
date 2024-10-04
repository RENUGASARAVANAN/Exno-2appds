# Exno-2appds
**AIM:**

To Perform Data Collection through web scraping using python.

**ALGORITHM:**

Step 1: Include the Necessary python libraries.
 
Step 2: Use the requests library to send HTTP requests to a web page.
 
Step 3: Retrieve the HTML content and use BeautifulSoup to parse it.
 
Step 4: Navigate and extract the necessary data.
 
Step 5: Handle the Java script content and retrieve the data using the html tags.
 
Step 6: Check with the website permission and scrap the content.

**PROGRAM:**
#### DEVELOPED BY: RENUGA S
#### REG NO: 212222230118

```
import requests
from bs4 import BeautifulSoup
import pandas as pd

url = 'https://www.w3schools.com/html/html_table_sizes.asp'
response = requests.get(url)
response

soup = BeautifulSoup(response.content, 'html.parser')
headings = soup.find_all('h2')
headlist=[x.text for x in headings]
for heading in headlist:
   print(heading)

df=pd.DataFrame(headlist,columns=['Headings'])
df.to_csv('newdata.csv', index=False)
df
```

**OUTPUT:**

![Screenshot 2024-10-04 083643](https://github.com/user-attachments/assets/7e3268b7-bc5d-4219-8e3a-3fa1afbd2a23)

![Screenshot 2024-10-04 083649](https://github.com/user-attachments/assets/84c1669b-785f-43ab-b81f-aad5f5989f01)

![Screenshot 2024-10-04 083707](https://github.com/user-attachments/assets/47ba3e66-052b-4925-802c-3c89705f1b4a)

**RESULT:**

 Thus , data Collection through web scraping using python is successfully performed.
 
