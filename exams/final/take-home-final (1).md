# Data 200: Data Systems for Data Analytics


# Name: fathima mohammadi

# Take Home Final Exam
<font color='red'>**Due Date:** Dec 20, 5p (T-F 1:30p section) </font> <br>
<font color='red' style="margin-left: 1.85cm; display: inline-block;">Dec 21, 11:59a (T-F 3p section)</font>

---

### **Task**: Scrape data from Goodreads.com 📚

---

### **Objective**
For this exam, you will scrape and analyze data from Goodreads.com. The work is split into two parts, each focusing on different aspects of the data
1. **"Best Books" Analysis**: Explore Goodreads' "Best Books" lists for a specific year.
2. **Author-Level Analysis**: Study the trends and patterns in the works of a specific author.

---

### **Instructions**

#### **Task 1: Best Books**
You are tasked with analyzing Goodreads' "Best Books" lists for a specific year based on the **first letter of your first name**. For example, if your first name starts with **A–E**, you are assigned to the year **2023**; if it starts with **F–J**, you are assigned to **2022**, and so on:

| Initials | Assigned Year | URL                                              |
|----------|---------------|---------------------------------------------------------|
| A–E      | 2023          | [Best Books of 2023](https://www.goodreads.com/list/best_of_year/2023) |
| F–J      | 2022          | [Best Books of 2022](https://www.goodreads.com/list/best_of_year/2022) |
| K–O      | 2021          | [Best Books of 2021](https://www.goodreads.com/list/best_of_year/2021) |
| P–T      | 2020          | [Best Books of 2020](https://www.goodreads.com/list/best_of_year/2020) |
| U–Z      | 2019          | [Best Books of 2019](https://www.goodreads.com/list/best_of_year/2019) |



**Your Tasks**:
1. Scrape data from the Goodreads "Best Books of [Year]" list:
   - **URL**: https://www.goodreads.com/list/best_of_year/2023 (replace the year with your assigned year). You can also use the table above.
2. Collect the following data for each book:
   - Title
   - Publication date (first published)
   - Author
   - Genre (if available, and feel free to pick the first genre listed)
   - Average rating
   - Number of ratings
   - Number of pages
   - Rank
   - Language (if available)
   - Number of people who are currently reading (if available)
   - Number of people who want to read (if available)
3. Perform the following analyses:
   - **Genre ratings**:
       - Compare average ratings across genres. Which 2-3 genres tends to have the highest ratings? Create a table showing average rating score, and average rank by genre.
   - **Popularity and ratings**:
       - Examine whether books with more ratings tend to have higher or lower average scores. Create a scatterplot showing the relationship between the number of ratings and average rating. On the x-axis, you should have **number of ratings**; on the y-axis, you should have **average rating**.

---

#### **Task 2: Author-Level Analysis**
You are now tasked with analyzing books by a specific author based on the **first letter of your first name**:

| Your first name initial | Author              | Author Goodreads link                               | Birthday       |
|----------|---------------------|--------------------------------------------------------------------|----------------|
| A–E      | Stephen King        | [Stephen King](https://www.goodreads.com/author/list/3389)         | Sep 21, 1947   |
| F–J      | George R.R. Martin  | [George R.R. Martin](https://www.goodreads.com/author/list/346732) | Sep 20, 1948   |
| K–O      | Ernest Hemingway    | [Ernest Hemingway](https://www.goodreads.com/author/list/1455)     | Jul 21, 1899   |
| P–T      | Neil Gaiman         | [Neil Gaiman](https://www.goodreads.com/author/list/1221698)       | Nov 10, 1960   |
| U–Z      | Nora Roberts        | [Nora Roberts](https://www.goodreads.com/author/list/625)          | Oct 10, 1950   |


**Your Tasks**:
1. Scrape all books by your assigned author:
   - Use the link provided for your author.
2. Collect the following data for each book:
   - Title
   - Publication date (first published)
   - Author
   - Genre (if available, and feel free to pick the first genre listed)
   - Average rating
   - Number of ratings
   - Number of pages
   - Rank (from the books written by the author)
   - Language (if available)
   - Number of people who are currently reading (if available)
   - Number of people who want to read (if available)
3. Perform the following analyses:
   - **Language Distribution**:
     - How many books has the author published in English? In other languages? Create a table showing the count of books by language.
   - **Author's Age and Page Count**:
     - Do authors tend to write longer books as they age? Use the author's birthday to calculate their age at the time of each book's publication. Create a line plot with **author's age** on the x-axis and **page count** on the y-axis.
   - **Author's Age and Rating**:
     - For English-only books, create a line plot with **author's age** on the x-axis and **average rating** on the y-axis.
     - Repeat the analysis including books in languages other than English. Does your interpretation change?
   - **Pages vs. Ratings**:
     - Is there a relationship between the number of pages and a book's average rating? Create a scatterplot with **page count** on the x-axis and **average rating** on the y-axis.
   - **Interest on a book**:
     - Is there a relationship between the number of people who are currently reading the book and the number of people who left a rating? Create a scatterplot with **number of people who are currently reading** on the x-axis and **number of ratings** on the y-axis. Create a second scatterplot with **average rating** on the y-axis. Do books with more interest tend to receive higher ratings?

---

### **Submission Requirements**
Submit your work as a single `.ipynb` file, along with a copy of it as a `.md` file. The notebook should include:
1. **Code**:
   - Well-documented python code using Selenium for web scraping.
   - Proper error handling and strategies for dynamic content.
2. **Cleaned Data**:
   - Include the cleaned datasets from both tasks as .csv files. You can upload them in your github repo.
3. **Analysis and Report**:
   - Present your findings using markdown cells, tables, and visualizations you make in python.
   - Address all questions posed for your assigned tasks.
4. **Visualizations**:
   - Include relevant charts (e.g., bar charts, line plots, scatterplots) to support your conclusions.

---

### **Rubric**

| Item                        | Weight |
|-----------------------------|--------|
| Code accuracy               | 25%    |
| Code clarity and annotation | 25%    |
| Exploratory data analysis   | 25%    |
| Discussion of findings      | 25%    |

---

### **Tips**
- Make sure to insert time.sleep() right after you request driver to go to a link (before requesting elements). Make sure to wait at least 0.7 second, or even slightly higher if you run into issues.
- Try-except blocks will be your friend because xpath positions on a page may differ depending on the book and content availability.

---

### **Resources**
- Course notes on Github
- Selenium documentation: https://www.selenium.dev/documentation/
- Pandas documentation: https://pandas.pydata.org/docs/
- Matplotlib documentation: https://matplotlib.org/stable/contents.html

Good luck! 🏁



```python
import requests 

url = 'https://www.goodreads.com/list/best_of_year/2022'
headers = {'User-Agent': 'Mozilla/5.0'}

response = requests.get(url,headers=headers)
print(response.status_code)
```

    200



```python
pip install selenium
```

    Requirement already satisfied: selenium in /opt/anaconda3/lib/python3.12/site-packages (4.27.1)
    Requirement already satisfied: urllib3<3,>=1.26 in /opt/anaconda3/lib/python3.12/site-packages (from urllib3[socks]<3,>=1.26->selenium) (2.2.2)
    Requirement already satisfied: trio~=0.17 in /opt/anaconda3/lib/python3.12/site-packages (from selenium) (0.27.0)
    Requirement already satisfied: trio-websocket~=0.9 in /opt/anaconda3/lib/python3.12/site-packages (from selenium) (0.11.1)
    Requirement already satisfied: certifi>=2021.10.8 in /opt/anaconda3/lib/python3.12/site-packages (from selenium) (2024.8.30)
    Requirement already satisfied: typing_extensions~=4.9 in /opt/anaconda3/lib/python3.12/site-packages (from selenium) (4.11.0)
    Requirement already satisfied: websocket-client~=1.8 in /opt/anaconda3/lib/python3.12/site-packages (from selenium) (1.8.0)
    Requirement already satisfied: attrs>=23.2.0 in /opt/anaconda3/lib/python3.12/site-packages (from trio~=0.17->selenium) (24.3.0)
    Requirement already satisfied: sortedcontainers in /opt/anaconda3/lib/python3.12/site-packages (from trio~=0.17->selenium) (2.4.0)
    Requirement already satisfied: idna in /opt/anaconda3/lib/python3.12/site-packages (from trio~=0.17->selenium) (3.7)
    Requirement already satisfied: outcome in /opt/anaconda3/lib/python3.12/site-packages (from trio~=0.17->selenium) (1.3.0.post0)
    Requirement already satisfied: sniffio>=1.3.0 in /opt/anaconda3/lib/python3.12/site-packages (from trio~=0.17->selenium) (1.3.0)
    Requirement already satisfied: wsproto>=0.14 in /opt/anaconda3/lib/python3.12/site-packages (from trio-websocket~=0.9->selenium) (1.2.0)
    Requirement already satisfied: pysocks!=1.5.7,<2.0,>=1.5.6 in /opt/anaconda3/lib/python3.12/site-packages (from urllib3[socks]<3,>=1.26->selenium) (1.7.1)
    Requirement already satisfied: h11<1,>=0.9.0 in /opt/anaconda3/lib/python3.12/site-packages (from wsproto>=0.14->trio-websocket~=0.9->selenium) (0.14.0)
    Note: you may need to restart the kernel to use updated packages.



```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import pandas as pd

# Set up the Chrome driver service)  # Update with the correct path to your chromedriver
driver = webdriver.Chrome()

url = 'https://www.goodreads.com/list/best_of_year/2022'
driver.get(url)

titles = []
authors = []
ratings = []

for book in book_rows:
    try:
        book_rows = driver.find_elements('xpath', "//*[@id='bodycontainer']/div[3]/div[1]/div[2]/div[2]/table/tbody/tr[1]/td[2]/a/span")
    except:
        title = 'N/A'
    titles.append(title)
```


    ---------------------------------------------------------------------------

    WebDriverException                        Traceback (most recent call last)

    Cell In[1], line 12
          9 driver = webdriver.Chrome()
         11 url = 'https://www.goodreads.com/list/best_of_year/2022'
    ---> 12 driver.get(url)
         14 titles = []
         15 authors = []


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/webdriver.py:393, in WebDriver.get(self, url)
        391 def get(self, url: str) -> None:
        392     """Loads a web page in the current browser session."""
    --> 393     self.execute(Command.GET, {"url": url})


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/webdriver.py:384, in WebDriver.execute(self, driver_command, params)
        382 response = self.command_executor.execute(driver_command, params)
        383 if response:
    --> 384     self.error_handler.check_response(response)
        385     response["value"] = self._unwrap_value(response.get("value", None))
        386     return response


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/errorhandler.py:232, in ErrorHandler.check_response(self, response)
        230         alert_text = value["alert"].get("text")
        231     raise exception_class(message, screen, stacktrace, alert_text)  # type: ignore[call-arg]  # mypy is not smart enough here
    --> 232 raise exception_class(message, screen, stacktrace)


    WebDriverException: Message: disconnected: Unable to receive message from renderer
      (failed to check if window was closed: disconnected: not connected to DevTools)
      (Session info: chrome=131.0.6778.205)
    Stacktrace:
    0   chromedriver                        0x000000010154f184 cxxbridge1$str$ptr + 3626716
    1   chromedriver                        0x00000001015479d4 cxxbridge1$str$ptr + 3596076
    2   chromedriver                        0x0000000100fb4968 cxxbridge1$string$len + 89228
    3   chromedriver                        0x0000000100f9fc90 cxxbridge1$string$len + 4020
    4   chromedriver                        0x0000000100f9fa00 cxxbridge1$string$len + 3364
    5   chromedriver                        0x0000000100f9ea9c core::str::slice_error_fail::ha0e52dbcb60e6bae + 64284
    6   chromedriver                        0x0000000100fbf7c4 cxxbridge1$string$len + 133864
    7   chromedriver                        0x0000000101032780 cxxbridge1$string$len + 604836
    8   chromedriver                        0x0000000100fed568 cxxbridge1$string$len + 321676
    9   chromedriver                        0x0000000100fee1b8 cxxbridge1$string$len + 324828
    10  chromedriver                        0x000000010151a9ac cxxbridge1$str$ptr + 3411716
    11  chromedriver                        0x000000010151dccc cxxbridge1$str$ptr + 3424804
    12  chromedriver                        0x000000010150186c cxxbridge1$str$ptr + 3308996
    13  chromedriver                        0x000000010151e58c cxxbridge1$str$ptr + 3427044
    14  chromedriver                        0x00000001014f309c cxxbridge1$str$ptr + 3249652
    15  chromedriver                        0x00000001015384b8 cxxbridge1$str$ptr + 3533328
    16  chromedriver                        0x0000000101538634 cxxbridge1$str$ptr + 3533708
    17  chromedriver                        0x0000000101547648 cxxbridge1$str$ptr + 3595168
    18  libsystem_pthread.dylib             0x000000019ea2c2e4 _pthread_start + 136
    19  libsystem_pthread.dylib             0x000000019ea270fc thread_start + 8




```python
from selenium import webdriver
import time

driver = webdriver.Chrome()

url = 'https://www.goodreads.com/list/best_of_year/2022'
driver.get(url)
time.sleep(5) # give more time for the data to be able to load

html_source = driver.page_source
print(html_source[:2000])

driver.quit()

```

    <html class="desktop withSiteHeaderTopFullImage
     picture es5array es5date es5function es5object strictmode es5string json es5syntax es5undefined es5 no-touchevents cssanimations flexbox flexwrap csstransforms localstorage" style=""><head>
      <title>Best Books of 2022 (1515 books)</title>
    
    <meta content="1,515 books based on 1829 votes: Book Lovers by Emily Henry, Lessons in Chemistry by Bonnie Garmus, I'm Glad My Mom Died by Jennette McCurdy, Reminders o..." name="description">
    <meta content="telephone=no" name="format-detection">
    <link href="https://www.goodreads.com/list/best_of_year/2022?id=171064.Best_Books_of_2022" rel="canonical">
    
    
    
      
      <!-- * Copied from https://info.analytics.a2z.com/#/docs/data_collection/csa/onboard */ -->
    <script src="https://rules.quantcount.com/rules-p-0dUe_kJAjvkoY.js" async=""></script><script async="" src="https://sb.scorecardresearch.com/beacon.js"></script><script src="https://secure.quantserve.com/aquant.js?a=p-0dUe_kJAjvkoY" async="" type="text/javascript"></script><script async="" src="//c.amazon-adsystem.com/aax2/apstag.js"></script><script async="" type="text/javascript" src="https://securepubads.g.doubleclick.net/tag/js/gpt.js"></script><script id="twitter-wjs" src="https://platform.twitter.com/widgets.js"></script><script>
      //<![CDATA[
        !function(){function n(n,t){var r=i(n);return t&&(r=r("instance",t)),r}var r=[],c=0,i=function(t){return function(){var n=c++;return r.push([t,[].slice.call(arguments,0),n,{time:Date.now()}]),i(n)}};n._s=r,this.csa=n}();
        
        if (window.csa) {
          window.csa("Config", {
            "Application": "GoodreadsMonolith",
            "Events.SushiEndpoint": "https://unagi.amazon.com/1/events/com.amazon.csm.csa.prod",
            "Events.Namespace": "csa",
            "CacheDetection.RequestID": "W1QT0KHW1XFBBSHZDKVB",
            "ObfuscatedMarketplaceId": "A1PQBFHBHS6YH1"
          });
        
          window.csa("Events")("setEntity", {
            session: { id: "005-5308660-9801391" },
            page: {requestId: "W1Q



```python
from selenium import webdriver
import time

driver = webdriver.Chrome()

url = 'https://www.goodreads.com/list/best_of_year/2022'
driver.get(url)

time.sleep(5)

html_body = driver.find_element('tag name', 'body').text
print(html_body[:3000])

driver.quit()

```

    HomeMy Books
    Browse ▾
    Community ▾
    Sign InJoin
    
    Listopia
    
    Best Books of 2022
    The best books published during 2022.
    
    For 2022
    2022 books most frequently added to shelves
    2022 lists
    2022 shelf
    Graphic Novels of 2022
    Picture Books of 2021
    YA Novels of 2022
    
    By year:
    1889
    1890, 1891, 1892, 1893, 1894, 1895, 1896, 1897, 1898, 1899
    1900
    1910
    1920
    1930
    1940
    1950
    
    , , , , , , , , ,
    , , , , , , , , , ,
    , , , , , , , , ,
    , , , , , , , , ,
    , , , , , , , , ,
    , , , ,
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    FEATURED NEWS & INTERVIEWS
    
    
    
    Discover & read more
    Sign up to get better recommendations with a free account.
    Continue with Amazon
    Sign up with email
    Already a member? Sign in
    By clicking “Sign up” I agree to the Goodreads Terms of Service and confirm that I am at least 13 years old. Read our Privacy Policy



```python
from selenium import webdriver 
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()

url = "https://www.goodreads.com/list/best_of_year/2022"
driver.get(url)
time.sleep(3)

for _ in range(10):
    driver.find_element(By.TAG_NAME,'body').send_keys(Keys.PAGE_DOWN)
    time.sleep(2)

html_body = driver.find_element(By.TAG_NAME,'body').text
print(html_body[:3000]) 

driver.quit()
```

    HomeMy Books
    Browse ▾
    Community ▾
    Sign InJoin
    
    Listopia
    
    Best Books of 2022
    The best books published during 2022.
    
    For 2022
    2022 books most frequently added to shelves
    2022 lists
    2022 shelf
    Graphic Novels of 2022
    Picture Books of 2021
    YA Novels of 2022
    
    By year:
    1889
    1890, 1891, 1892, 1893, 1894, 1895, 1896, 1897, 1898, 1899
    1900
    1910
    1920
    1930
    1940
    1950
    
    , , , , , , , , ,
    , , , , , , , , , ,
    , , , , , , , , ,
    , , , , , , , , ,
    , , , , , , , , ,
    , , , ,
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    FEATURED NEWS & INTERVIEWS
    
    
    
    Discover & read more
    Sign up to get better recommendations with a free account.
    Continue with Amazon
    Sign up with email
    Already a member? Sign in
    By clicking “Sign up” I agree to the Goodreads Terms of Service and confirm that I am at least 13 years old. Read our Privacy Policy



```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import pandas as pd
import time

driver = webdriver.Chrome()

url = 'https://www.goodreads.com/list/best_of_year/2022'
driver.get(url)
time.sleep(3)

for _ in range(10):
    driver.find_element(By.TAG_NAME,'body').send_keys(Keys.PAGE_DOWN)
    time.sleep(2)

print('Checking page source...')
print(driver.page_source[:2000])

titles = []
authors = []
ratings = []

try:
    
    book_rows = driver.find_elements(By.XPATH, "//tr[contains(@class, 'bookalike')]")
    print(f"Number of books found: {len(book_rows)}")

    for book in book_rows:
        try:
            title = book.find_element(By.XPATH, ".//a[contains(@class, 'bookTitle')]").text.strip()
        except:
            title = "N/A"
        titles.append(title)

        try:
            author = book.find_element(By.XPATH, ".//a[contains(@class, 'authorName')]").text.strip()
        except:
            author = "N/A"
        authors.append(author)

        try:
            rating = book.find_element(By.XPATH, ".//span[contains(@class, 'minirating')]").text.split("—")[0].strip()
        except:
            rating = "N/A"
        ratings.append(rating)

except Exception as e:
    print('There Was An Error During Extraction:', e)

df = pd.DataFrame({
    'Title': titles,
    'Author': authors,
    'Average Rating': ratings
})

df.to_csv('goodreads_fixed_books.csv', index=False)
print("The Data Is Saved Successfully To 'goodreads_fixed_books.csv'.")

driver.quit()
```

    Checking page source...
    <html class="desktop withSiteHeaderTopFullImage
     picture es5array es5date es5function es5object strictmode es5string json es5syntax es5undefined es5 no-touchevents cssanimations flexbox flexwrap csstransforms localstorage" style=""><head>
      <title>Best Books of 2022 (1515 books)</title>
    
    <meta content="1,515 books based on 1829 votes: Book Lovers by Emily Henry, Lessons in Chemistry by Bonnie Garmus, I'm Glad My Mom Died by Jennette McCurdy, Reminders o..." name="description">
    <meta content="telephone=no" name="format-detection">
    <link href="https://www.goodreads.com/list/best_of_year/2022?id=171064.Best_Books_of_2022" rel="canonical">
    
    
    
      
      <!-- * Copied from https://info.analytics.a2z.com/#/docs/data_collection/csa/onboard */ -->
    <script src="https://rules.quantcount.com/rules-p-0dUe_kJAjvkoY.js" async=""></script><script async="" src="https://sb.scorecardresearch.com/beacon.js"></script><script src="https://secure.quantserve.com/aquant.js?a=p-0dUe_kJAjvkoY" async="" type="text/javascript"></script><script async="" src="//c.amazon-adsystem.com/aax2/apstag.js"></script><script async="" type="text/javascript" src="https://securepubads.g.doubleclick.net/tag/js/gpt.js"></script><script id="twitter-wjs" src="https://platform.twitter.com/widgets.js"></script><script>
      //<![CDATA[
        !function(){function n(n,t){var r=i(n);return t&&(r=r("instance",t)),r}var r=[],c=0,i=function(t){return function(){var n=c++;return r.push([t,[].slice.call(arguments,0),n,{time:Date.now()}]),i(n)}};n._s=r,this.csa=n}();
        
        if (window.csa) {
          window.csa("Config", {
            "Application": "GoodreadsMonolith",
            "Events.SushiEndpoint": "https://unagi.amazon.com/1/events/com.amazon.csm.csa.prod",
            "Events.Namespace": "csa",
            "CacheDetection.RequestID": "NG08P0X03KNGG8TTADG0",
            "ObfuscatedMarketplaceId": "A1PQBFHBHS6YH1"
          });
        
          window.csa("Events")("setEntity", {
            session: { id: "174-2969711-1988014" },
            page: {requestId: "NG0
    Number of books found: 0
    The Data Is Saved Successfully To 'goodreads_fixed_books.csv'.



```python
from selenium import webdriver 
from selenium.webdriver.common.by import By
import pandas as pd
import time

driver = webdriver.Chrome()

url = "https://www.goodreads.com/list/best_of_year/2022"

driver.get(url)
time.sleep(2)

titles = []
authors = []
ratings = []

book_rows = driver.find_elements(By.CSS_SELECTOR, "table.tableList tr")

for row in book_rows:
    try:
        # Title
        title = row.find_element(By.CSS_SELECTOR, "a.bookTitle span").text.strip()
        titles.append(title)
    except:
        titles.append("N/A")

    try:
        # Author
        author = row.find_element(By.CSS_SELECTOR, "span[itemprop='author']").text.strip()
        authors.append(author)
    except:
        authors.append("N/A")

    try:
        # Ratings
        rating = row.find_element(By.CSS_SELECTOR, "span.minirating").text.split()[0]
        ratings.append(float(rating))
    except:
        ratings.append(0.0)

driver.quit()

df = pd.DataFrame({
    'Title': titles,
    'Author': authors,
    'Average Rating': ratings
})

df.to_csv('goodreads_best_books_2022.csv',index = False)
print("The Data Is Saved Successfully To 'goodreads_best_books_2022.csv'")
```

    The Data Is Saved Successfully To 'goodreads_best_books_2022.csv'



```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd
import time

# Initialize WebDriver
driver = webdriver.Chrome()

# URL of Goodreads Best Books of 2020
url = "https://www.goodreads.com/list/best_of_year/2022"

# Load the webpage
driver.get(url)
time.sleep(3)  # Allow time for the page to fully load

# Lists to store the scraped data
titles = []
authors = []
ratings = []

# Locate book rows
book_rows = driver.find_elements(By.CSS_SELECTOR, "table.tableList tr")

# Extract data for each book
for row in book_rows:
    try:
        # Title
        title = row.find_element(By.CSS_SELECTOR, "a.bookTitle span").text.strip()
        if not title:
            continue  # Skip rows with missing titles
        titles.append(title)
    except:
        continue  # Skip problematic rows

    try:
        # Author
        author = row.find_element(By.CSS_SELECTOR, "a.authorName span").text.strip()
        authors.append(author)
    except:
        authors.append("N/A")  # If author is missing

    try:
        # Average Rating
        rating_text = row.find_element(By.CSS_SELECTOR, "span.minirating").text.strip()
        rating = float(rating_text.split()[0])  # Extract the numerical part
        ratings.append(rating)
    except:
        ratings.append(0.0)  # Default to 0 if rating is missing

# Close the browser
driver.quit()

# Create a DataFrame
df = pd.DataFrame({
    "Title": titles,
    "Author": authors,
    "Average Rating": ratings
})

# Remove rows with empty or invalid data
df = df[df['Title'] != ""]

# Save to CSV
df.to_csv("goodreads_best_books_2022_cleaned.csv", index=False)
print("Data saved successfully to 'goodreads_best_books_2022_cleaned.csv'.")
```

    Data saved successfully to 'goodreads_best_books_2022_cleaned.csv'.



```python
import time
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By

# Initialize Selenium WebDriver
driver = webdriver.Chrome()  # Make sure you have ChromeDriver installed
base_url = "https://www.goodreads.com"

# Example list of book URLs (replace with your own list of extracted URLs)
book_urls = [
    "/book/show/44778083-the-house-in-the-cerulean-sea",
    "/book/show/44778083-house-of-earth-and-blood"
]

# List to store data
books_data = []

# Loop through each book page
for url in book_urls:
    driver.get(base_url + url)
    time.sleep(2)  # Wait for the page to load
    
    try:
        # Extract the first genre listed on the page
        genre = driver.find_element(By.CLASS_NAME, "bookPageGenreLink").text
    except:
        genre = "Not Found"  # Handle missing genres
    
    books_data.append({"URL": url, "Genre": genre})
    print(f"Extracted genre: {genre} for URL: {url}")

# Close the driver
driver.quit()

# Convert to a DataFrame
df = pd.DataFrame(books_data)
df.to_csv("book_genres.csv", index=False)
print("Genres saved to 'book_genres.csv'")
```

    Extracted genre: Not Found for URL: /book/show/44778083-the-house-in-the-cerulean-sea
    Extracted genre: Not Found for URL: /book/show/44778083-house-of-earth-and-blood
    Genres saved to 'book_genres.csv'



```python
import time
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By

# Initialize Selenium WebDriver
driver = webdriver.Chrome()  # Make sure you have ChromeDriver installed
base_url = "https://www.goodreads.com"

# Example list of book URLs
book_urls = [
    "/book/show/44778083-the-house-in-the-cerulean-sea",
    "/book/show/44778083-house-of-earth-and-blood"
]

# List to store extracted data
books_data = []

# Loop through each book page
for url in book_urls:
    driver.get(base_url + url)
    time.sleep(3)  # Allow the page to fully load
    
    try:
        # Locate genre links using the updated class
        genre_elements = driver.find_elements(By.CSS_SELECTOR, "a.Button.Button--tag.Button--medium span.Button__labelItem")
        genres = [element.text for element in genre_elements if element.text.strip()]
        
        # Extract the first genre or assign 'Not Found'
        first_genre = genres[0] if genres else "Not Found"
    except Exception as e:
        print(f"Error: {e}")
        first_genre = "Not Found"
    
    books_data.append({"URL": url, "Genre": first_genre})
    print(f"Extracted genre: {first_genre} for URL: {url}")

# Close the driver
driver.quit()

#save the results
df = pd.DataFrame(books_data)
df.to_csv("book_genres.csv", index=False)
print("Genres saved to 'book_genres.csv'")
```

    Extracted genre: Romance for URL: /book/show/44778083-the-house-in-the-cerulean-sea
    Error: Message: no such window: target window already closed
    from unknown error: web view not found
      (Session info: chrome=131.0.6778.205)
    Stacktrace:
    0   chromedriver                        0x0000000102bf3184 cxxbridge1$str$ptr + 3626716
    1   chromedriver                        0x0000000102beb9d4 cxxbridge1$str$ptr + 3596076
    2   chromedriver                        0x0000000102658968 cxxbridge1$string$len + 89228
    3   chromedriver                        0x0000000102633e44 core::str::slice_error_fail::ha0e52dbcb60e6bae + 3780
    4   chromedriver                        0x00000001026c2d48 cxxbridge1$string$len + 524396
    5   chromedriver                        0x00000001026d5c24 cxxbridge1$string$len + 601928
    6   chromedriver                        0x0000000102691568 cxxbridge1$string$len + 321676
    7   chromedriver                        0x00000001026921b8 cxxbridge1$string$len + 324828
    8   chromedriver                        0x0000000102bbe9ac cxxbridge1$str$ptr + 3411716
    9   chromedriver                        0x0000000102bc1ccc cxxbridge1$str$ptr + 3424804
    10  chromedriver                        0x0000000102ba586c cxxbridge1$str$ptr + 3308996
    11  chromedriver                        0x0000000102bc258c cxxbridge1$str$ptr + 3427044
    12  chromedriver                        0x0000000102b9709c cxxbridge1$str$ptr + 3249652
    13  chromedriver                        0x0000000102bdc4b8 cxxbridge1$str$ptr + 3533328
    14  chromedriver                        0x0000000102bdc634 cxxbridge1$str$ptr + 3533708
    15  chromedriver                        0x0000000102beb648 cxxbridge1$str$ptr + 3595168
    16  libsystem_pthread.dylib             0x000000019ea2c2e4 _pthread_start + 136
    17  libsystem_pthread.dylib             0x000000019ea270fc thread_start + 8
    
    Extracted genre: Not Found for URL: /book/show/44778083-house-of-earth-and-blood
    Genres saved to 'book_genres.csv'



```python
import time
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

# Initialize Selenium WebDriver
driver = webdriver.Chrome()  
base_url = "https://www.goodreads.com/search?q="

# Load the CSV with titles and authors
input_file = "goodreads_best_books_2022_cleaned.csv"  # Replace with your CSV file name
output_file = "book_urls.csv"

# Read the book titles and authors
books_df = pd.read_csv(input_file)
book_urls = []

try:
    print("Searching for book URLs...")
    for index, row in books_df.iterrows():
        title = row['Title']  # Make sure 'Title' matches the column name in your CSV
        search_url = base_url + title.replace(" ", "+")
        
        driver.get(search_url)  # Visit Goodreads search page
        time.sleep(2)  # Wait for the page to load

        try:
            # Wait for search results to load
            first_result = WebDriverWait(driver, 10).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "a.bookTitle"))
            )

            # Get the URL of the first search result
            book_url = first_result.get_attribute("href")
            print(f"Found URL for '{title}': {book_url}")
        except:
            book_url = "Not Found"
            print(f"URL not found for '{title}'")

        # Append the result to the list
        book_urls.append({'Title': title,'URL': book_url})

finally:
    driver.quit()

#save the results
output_df = pd.DataFrame(book_urls)
output_df.to_csv(output_file, index=False)
print(f"Saved book URLs to '{output_file}'.")
```

    Searching for book URLs...
    Saved book URLs to 'book_urls.csv'.



```python
import time
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import os

# Initialize Selenium WebDriver
driver = webdriver.Chrome()  
base_url = "https://www.goodreads.com/search?q="

# Load input and output files
input_file = "goodreads_best_books_2022_cleaned.csv"  # Replace with your CSV file name
output_file = "book_urls.csv"

# Load the book list
books_df = pd.read_csv(input_file)

# Try to load existing URLs into a dictionary
if os.path.exists(output_file):
    existing_urls = pd.read_csv(output_file).set_index('Title')['URL'].to_dict()
else:
    existing_urls = {}

book_urls = []

try:
    print("Searching for book URLs...")
    for index, row in books_df.iterrows():
        title = row['Title']
        
        # Check if the URL already exists in the dictionary
        if title in existing_urls:
            print(f"Using cached URL for '{title}'")
            book_url = existing_urls[title]
        else:
            search_url = base_url + title.replace(" ", "+")
            driver.get(search_url)
            time.sleep(2)  # Allow page to load

            try:
                # Wait for search results to load
                first_result = WebDriverWait(driver, 10).until(
                    EC.presence_of_element_located((By.CSS_SELECTOR, "a.bookTitle"))
                )
                book_url = first_result.get_attribute("href")
                print(f"Found URL for '{title}': {book_url}")
            except Exception as e:
                book_url = "Not Found"
                print(f"URL not found for '{title}': {e}")

            # Update the dictionary with the new URL
            existing_urls[title] = book_url

        # Append the result to the list
        book_urls.append({'Title': title, 'URL': book_url})

finally:
    driver.quit()

# Save the results to the output CSV file
output_df = pd.DataFrame(book_urls)
output_df.to_csv(output_file, index=False)
print(f"Saved book URLs to '{output_file}'.")
```


    ---------------------------------------------------------------------------

    KeyboardInterrupt                         Traceback (most recent call last)

    Cell In[16], line 10
          7 import os
          9 # Initialize Selenium WebDriver
    ---> 10 driver = webdriver.Chrome()  
         11 base_url = "https://www.goodreads.com/search?q="
         13 # Load input and output files


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/chrome/webdriver.py:45, in WebDriver.__init__(self, options, service, keep_alive)
         42 service = service if service else Service()
         43 options = options if options else Options()
    ---> 45 super().__init__(
         46     browser_name=DesiredCapabilities.CHROME["browserName"],
         47     vendor_prefix="goog",
         48     options=options,
         49     service=service,
         50     keep_alive=keep_alive,
         51 )


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/chromium/webdriver.py:66, in ChromiumDriver.__init__(self, browser_name, vendor_prefix, options, service, keep_alive)
         57 executor = ChromiumRemoteConnection(
         58     remote_server_addr=self.service.service_url,
         59     browser_name=browser_name,
       (...)
         62     ignore_proxy=options._ignore_local_proxy,
         63 )
         65 try:
    ---> 66     super().__init__(command_executor=executor, options=options)
         67 except Exception:
         68     self.quit()


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/webdriver.py:241, in WebDriver.__init__(self, command_executor, keep_alive, file_detector, options, locator_converter, web_element_cls, client_config)
        239 self._authenticator_id = None
        240 self.start_client()
    --> 241 self.start_session(capabilities)
        242 self._fedcm = FedCM(self)
        244 self._websocket_connection = None


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/webdriver.py:329, in WebDriver.start_session(self, capabilities)
        322 """Creates a new session with the desired capabilities.
        323 
        324 :Args:
        325  - capabilities - a capabilities dict to start the session with.
        326 """
        328 caps = _create_caps(capabilities)
    --> 329 response = self.execute(Command.NEW_SESSION, caps)["value"]
        330 self.session_id = response.get("sessionId")
        331 self.caps = response.get("capabilities")


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/webdriver.py:382, in WebDriver.execute(self, driver_command, params)
        379     elif "sessionId" not in params:
        380         params["sessionId"] = self.session_id
    --> 382 response = self.command_executor.execute(driver_command, params)
        383 if response:
        384     self.error_handler.check_response(response)


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/remote_connection.py:404, in RemoteConnection.execute(self, command, params)
        402 trimmed = self._trim_large_entries(params)
        403 LOGGER.debug("%s %s %s", command_info[0], url, str(trimmed))
    --> 404 return self._request(command_info[0], url, body=data)


    File /opt/anaconda3/lib/python3.12/site-packages/selenium/webdriver/remote/remote_connection.py:428, in RemoteConnection._request(self, method, url, body)
        425     body = None
        427 if self._client_config.keep_alive:
    --> 428     response = self._conn.request(method, url, body=body, headers=headers, timeout=self._client_config.timeout)
        429     statuscode = response.status
        430 else:


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/_request_methods.py:144, in RequestMethods.request(self, method, url, body, fields, headers, json, **urlopen_kw)
        136     return self.request_encode_url(
        137         method,
        138         url,
       (...)
        141         **urlopen_kw,
        142     )
        143 else:
    --> 144     return self.request_encode_body(
        145         method, url, fields=fields, headers=headers, **urlopen_kw
        146     )


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/_request_methods.py:279, in RequestMethods.request_encode_body(self, method, url, fields, headers, encode_multipart, multipart_boundary, **urlopen_kw)
        275     extra_kw["headers"].setdefault("Content-Type", content_type)
        277 extra_kw.update(urlopen_kw)
    --> 279 return self.urlopen(method, url, **extra_kw)


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/poolmanager.py:443, in PoolManager.urlopen(self, method, url, redirect, **kw)
        441     response = conn.urlopen(method, url, **kw)
        442 else:
    --> 443     response = conn.urlopen(method, u.request_uri, **kw)
        445 redirect_location = redirect and response.get_redirect_location()
        446 if not redirect_location:


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/connectionpool.py:789, in HTTPConnectionPool.urlopen(self, method, url, body, headers, retries, redirect, assert_same_host, timeout, pool_timeout, release_conn, chunked, body_pos, preload_content, decode_content, **response_kw)
        786 response_conn = conn if not release_conn else None
        788 # Make the request on the HTTPConnection object
    --> 789 response = self._make_request(
        790     conn,
        791     method,
        792     url,
        793     timeout=timeout_obj,
        794     body=body,
        795     headers=headers,
        796     chunked=chunked,
        797     retries=retries,
        798     response_conn=response_conn,
        799     preload_content=preload_content,
        800     decode_content=decode_content,
        801     **response_kw,
        802 )
        804 # Everything went great!
        805 clean_exit = True


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/connectionpool.py:536, in HTTPConnectionPool._make_request(self, conn, method, url, body, headers, retries, timeout, chunked, response_conn, preload_content, decode_content, enforce_content_length)
        534 # Receive the response from the server
        535 try:
    --> 536     response = conn.getresponse()
        537 except (BaseSSLError, OSError) as e:
        538     self._raise_timeout(err=e, url=url, timeout_value=read_timeout)


    File /opt/anaconda3/lib/python3.12/site-packages/urllib3/connection.py:464, in HTTPConnection.getresponse(self)
        461 from .response import HTTPResponse
        463 # Get the response from http.client.HTTPConnection
    --> 464 httplib_response = super().getresponse()
        466 try:
        467     assert_header_parsing(httplib_response.msg)


    File /opt/anaconda3/lib/python3.12/http/client.py:1428, in HTTPConnection.getresponse(self)
       1426 try:
       1427     try:
    -> 1428         response.begin()
       1429     except ConnectionError:
       1430         self.close()


    File /opt/anaconda3/lib/python3.12/http/client.py:331, in HTTPResponse.begin(self)
        329 # read until we get a non-100 response
        330 while True:
    --> 331     version, status, reason = self._read_status()
        332     if status != CONTINUE:
        333         break


    File /opt/anaconda3/lib/python3.12/http/client.py:292, in HTTPResponse._read_status(self)
        291 def _read_status(self):
    --> 292     line = str(self.fp.readline(_MAXLINE + 1), "iso-8859-1")
        293     if len(line) > _MAXLINE:
        294         raise LineTooLong("status line")


    File /opt/anaconda3/lib/python3.12/socket.py:708, in SocketIO.readinto(self, b)
        706 while True:
        707     try:
    --> 708         return self._sock.recv_into(b)
        709     except timeout:
        710         self._timeout_occurred = True


    KeyboardInterrupt: 



```python
import time
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

# Load URLs from the saved file
input_file = "book_urls.csv"
output_file = "goodreads_book_data.csv"

book_data = []

driver = webdriver.Chrome()

try:
    urls_df = pd.read_csv(input_file)

    for index, row in urls_df.iterrows():
        book_title = row['Title']
        book_url = row['URL']
        print(f"Extracting data from {book_url}")

        driver.get(book_url)
        time.sleep(2)  # Allow page to load

        try:
            # Extract Title
            title = WebDriverWait(driver, 10).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "h1[data-testid='bookTitle']"))
            ).text
        except:
            title = "Not Found"

        try:
            # Extract Author
            author = driver.find_element(By.CSS_SELECTOR, "span[data-testid='authorName']").text
        except:
            author = "Not Found"

        try:
            # Extract Average Rating
            avg_rating = driver.find_element(By.CSS_SELECTOR, "div[data-testid='averageRating']").text
        except:
            avg_rating = "Not Found"

        book_data.append({
            "Title": title,
            "Author": author,
            "Average Rating": avg_rating,
            "URL": book_url
        })
        print(f"Extracted: {title}, {author}, {avg_rating}")

finally:
    driver.quit()

# Save to a new CSV file
output_df = pd.DataFrame(book_data)
output_df.to_csv(output_file, index=False)
print(f"Saved book data to '{output_file}'.")


```


```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException

# Initialize Selenium WebDriver
driver = webdriver.Chrome()
url = "https://www.goodreads.com/book/show/45047384-the-house-in-the-cerulean-sea?from_search=true&from_srp=true&qid=fb2xFor0tp&rank=1"

try:
    print("Extracting data from:", url)
    driver.get(url)

    # Wait for the title to load
    try:
        title = WebDriverWait(driver, 15).until(
            EC.presence_of_element_located((By.CSS_SELECTOR, "h1[data-testid='bookTitle']"))
        ).text
    except TimeoutException:
        title = "Not Found"
    # Extract the author
    try:
        author = WebDriverWait(driver, 15).until(
            EC.presence_of_element_located((By.CSS_SELECTOR, "span.ContributorLink__name"))
        ).text
    except TimeoutException:
        author = "Not Found"

    # Extract average rating
    try:
        avg_rating = WebDriverWait(driver, 15).until(
            EC.presence_of_element_located((By.CSS_SELECTOR, "div.RatingStatistics__rating"))
        ).text
    except TimeoutException:
        avg_rating = "Not Found"

    # Print the results
    print("Title:", title)
    print("Author:", author)
    print("Average Rating:", avg_rating)

finally:
    driver.quit()
```


```python
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException

# Input and Output File Names
input_file = "book_urls.csv"  # Your CSV with book URLs
output_file = "goodreads_book_data.csv"

# Initialize Selenium WebDriver
driver = webdriver.Chrome()

# Read the CSV File with URLs
books_df = pd.read_csv(input_file)

# Prepare a List to Store the Results
extracted_data = []

try:
    print("Extracting data for all book URLs...")
    for index, row in books_df.iterrows():
        url = row['URL']
        print(f"Extracting data from: {url}")
        
        driver.get(url)
        
        # Extract Title
        try:
            title = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "h1[data-testid='bookTitle']"))
            ).text
        except TimeoutException:
            title = "Not Found"
        
        # Extract Author
        try:
            author = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "span.ContributorLink__name"))
            ).text
        except TimeoutException:
            author = "Not Found"
        
        # Extract Average Rating
        try:
            avg_rating = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "div.RatingStatistics__rating"))
            ).text
        except TimeoutException:
            avg_rating = "Not Found"
        
        # Store the Extracted Data
        extracted_data.append({
            "URL": url,
            "Title": title,
            "Author": author,
            "Average Rating": avg_rating
        })

        print(f"Extracted: {title}, {author}, {avg_rating}")

finally:
    driver.quit()

# Save the Data to a CSV File
output_df = pd.DataFrame(extracted_data)
output_df.to_csv(output_file, index=False)
print(f"Saved extracted data to '{output_file}'.")

```


```python
import pandas as pd
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException

# Input and Output File Names
input_file = "book_urls.csv"  # Your CSV with book URLs
output_file = "goodreads_enriched_data.csv"

# Initialize Selenium WebDriver
driver = webdriver.Chrome()

# Read the CSV File with URLs
books_df = pd.read_csv(input_file)

# Prepare a List to Store the Results
extracted_data = []

try:
    print("Extracting enhanced data for all book URLs...")
    for index, row in books_df.iterrows():
        url = row['URL']
        print(f"Extracting data from: {url}")
        
        driver.get(url)
        
        # Extract Title
        try:
            title = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "h1[data-testid='bookTitle']"))
            ).text
        except TimeoutException:
            title = "Not Found"
        
        # Extract Author
        try:
            author = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "span.ContributorLink__name"))
            ).text
        except TimeoutException:
            author = "Not Found"
        
        # Extract Average Rating
        try:
            avg_rating = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "div.RatingStatistics__rating"))
            ).text
        except TimeoutException:
            avg_rating = "Not Found"
        
        # Extract Publication Date
        try:
            pub_date = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "p[data-testid='publicationInfo']"))
            ).text
        except TimeoutException:
            pub_date = "Not Found"
        try:
            genre = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "a.Button--tag-inline"))
            ).text
        except TimeoutException:
            genre = "Not Found"
        # Extract Genre
        try:
            genre = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "a.Button--tag-inline"))
            ).text
        except TimeoutException:
    genre = "Not Found"

        # Extract Number of Ratings
        try:
            num_ratings = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "div.RatingStatistics__meta > span"))
            ).text
        except TimeoutException:
            num_ratings = "Not Found"
        
        # Extract Number of Pages
        try:
            pages = WebDriverWait(driver, 15).until(
                EC.presence_of_element_located((By.CSS_SELECTOR, "p[data-testid='pagesFormat']"))
            ).text
        except TimeoutException:
            pages = "Not Found"

        # Store the Extracted Data
        extracted_data.append({
            "URL": url,
            "Title": title,
            "Author": author,
            "Average Rating": avg_rating,
            "Publication Date": pub_date,
            "Genre": genre,
            "Number of Ratings": num_ratings,
            "Pages": pages
        })

        print(f"Extracted: {title}, {author}, {avg_rating}, {pub_date}, {genre}, {num_ratings}, {pages}")

finally:
    driver.quit()

# Save the Data to a CSV File
output_df = pd.DataFrame(extracted_data)
output_df.to_csv(output_file, index=False)
print(f"Saved enhanced book data to '{output_file}'.")
```


```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException
import time

# Initialize WebDriver
driver = webdriver.Chrome()  # Ensure chromedriver is set up correctly
book_url = "https://www.goodreads.com/book/show/45047384-the-house-in-the-cerulean-sea"

try:
    print("Loading book page...")
    driver.get(book_url)
    time.sleep(3)  # Allow time for the page to load fully

    # Extract the first genre
    try:
        print("Extracting the first genre...")
        first_genre = WebDriverWait(driver, 10).until(
            EC.presence_of_element_located((By.CSS_SELECTOR, "a[href*='/genres/']"))
        ).text
        print(f"First Genre: {first_genre}")
    except TimeoutException:
        print("Genre not found within the specified timeout.")
except Exception as e:
    print(f"An error occurred: {e}")
finally:
    driver.quit()
    print("WebDriver closed.")
```


```python
import os
import inspect

def get_notebook_path():
    frame = inspect.currentframe()
    try:
        # Get the frame where this function is called
        frame_info = inspect.getframeinfo(frame)
        # Get the absolute path to the current working directory
        abs_dir = os.path.abspath('.')
        # Combine it with the notebook's filename
        notebook_path = os.path.join(abs_dir, frame_info.filename)
        return notebook_path
    finally:
        del frame

print(get_notebook_path())
```


```python

```
