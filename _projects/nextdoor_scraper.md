---
layout: page
title: Nextdoor Scraper
description: A simple and plug-and-play scraper for Nextdoor
img: https://is5-ssl.mzstatic.com/image/thumb/Purple116/v4/f4/db/fe/f4dbfeaa-2566-c306-ef37-8e0bac2b3e91/AppIcon-1x_U007emarketing-0-7-0-85-220.png/1200x600wa.png/
importance: 4
category: Scraper
---

<img src = "/assets/img/image.png" style="width:100%;">


## TL;DR
Nextdoor Scraper is a scraper in development for the hyperlocal social media - Nextdoor.

## Major features
The collection of the following items can be automated:

- Reactions counts
- Expand comments (multilevel)
- Comments count and comment text
- Body texts
- Post and comment ID
- Formatted date
- Scrolling by date (with exceptions, see to-dos)
- Get post user_name and comment user_name
- Get neighbourhood data of posts' and comments' authors

## Selenium-based scraper
Unlike BeautifulSoup, Selenium is not originally built for web scraping. However, Selenium has an amazing infrastructure for us to interact with dynamic elements on a web page. 

Selenium offers a range of useful wrappers for us to run our scraper on a test browser (i.e., webdriver). 

```python
#install necessary dependencies
from selenium import webdriver 
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager #required by the latest version of selenium
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.common.exceptions import NoSuchElementException
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
```

Before running our scripts, we need to assign a driver and then access the webpage through the ```driver.get ``` function.

```python
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install())) #install webdriver

driver.get("https://nextdoor.nl/news_feed/") #open nextdoor on chrome driver
```

After setting up the driver, we can run our script (see [Github](https://github.com/jyeungtin/NextDoorScraping/tree/main/NDscraper)).

## Sample dataset
The data (.csv) that you get from the scraper will look the following table. Mind that posts with 0 comment will still be recorded, but those cells regarding comments will be null. 

| **ID**           | **Text**            | **Comment Count** | **Post Author**    | **Neighbourhood** | **Date**   | **Reaction Count** | **Comment**                                                    | **Comment Author** | **Comment Author Neighbourhood** | **Comment ID**         |
|------------------|---------------------|-------------------|--------------------|-------------------|------------|--------------------|----------------------------------------------------------------|--------------------|----------------------------------|------------------------|
| s_00000000000001 | Hello neighbours!   | 1                 | Carol Katie        | Millie Valley     | 15/02/2021 | 5                  | Welcome!                                                       | Oliver Anderson    | Millie Valley                    | comment_00000000000001 |
| s_00000000000002 | I have lost my cat. | 51                | Anne B. Richardson | Bridgerton Falls  | 15/02/2021 | 12                 | I think I have seen a black cat around the corner of the cafe! | B. Vazquez         | Millie Valley                    | comment_00000000000002 |
| ...              | ...                 | ...               | ...                | ...               | ...        | ...                | ...                                                            | ...                | ...                              | ...                    |
| s_99999999999999 | New restaurant!     | 0                 | Evan Allan         | Wallux Creek      | 09/01/2020 | 0                  |                                                                |                    |                                  |                        |
