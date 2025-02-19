# Bani-service [2022]
(srcvirus: The following documentation is from the original github repo. It needs to be updated with the new changes. FOllow with a grain (or bag) of salt.)
_Scrape posts from any group or user into a .csv file without needing to register for any API access_

____

### How to use it?

Firstly, make sure you have selenium >= 3.141.0, GeckoDriver and FireFox installed. Install aws cli and configure with proper access credentials.

Export your email and password for Facebook login in EMAIL and PASSWORD environment variables.

Use `main.py` to collect the data. 
```
usage: fb-scraper/main.py [-h] [--pages PAGES [PAGES ...]] [--groups GROUPS [GROUPS ...]][-d DEPTH]
Data Collection
arguments:
  -h, --help            show this help message and exit
  -p, --pages PAGES [PAGES ...]
                        List the pages/profile you want to scrape
                        for recent posts
  
  -g, --groups GROUPS [GROUPS ...]
                        List the groups you want to scrape
                        for recent posts
  
  -d DEPTH, --depth DEPTH
                        How many recent posts you want to gather in
                        multiples of (roughly) 8.
```
Example: ```python scraper.py --pages feelzesty -d 20```
____
The output is `posts.json` inside the script folder.

Output is in two columns: index, text
