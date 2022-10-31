# Web Scraping
  - Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.
 
## web Scraping in python
  - We start by importing the following libraries.
  - 
          ``` python 
            import requests
          import urllib.request
          import time
          from bs4 import BeautifulSoup

  -   we set the url to the website and access the site with our requests library.
  -   ```
        url = 'http://web.mta.info/developers/turnstile.html'
        response = requests.get(url)
   
   - After that we parse it with BeautifulSoup:
   
     ``` 
       soup = BeautifulSoup(res.text, “html.parser”)
   
 ### Web Scraping best practices to follow to scrape without getting blocked 
   - Respect Robots.txt
   - Make the crawling slower, do not slam the server, treat websites nicely
   - Do not follow the same crawling pattern
   - Make requests through Proxies and rotate them as needed
   - Rotate User Agents and corresponding HTTP Request Headers between requests
   - Use a headless browser like Puppeteer, Selenium or Playwright
   - Beware of Honey Pot Traps
   - Check if Website is Changing Layouts
   - Avoid scraping data behind a login
   - Use Captcha Solving Services


