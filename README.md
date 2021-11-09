# eBay-Scraper

This repository was made to complete [Hw_03](https://github.com/mikeizbicki/cmc-csci040/tree/2021fall/hw_03).

## Summary

The python file `ebay-dl.py` contains code that will scrape eBay for the first ten pages of results for a user-input `search_term` and provide a dictionary with each itemized result and its `name`, `price`, `status`, `shipping` cost, and if it has `free_returns`.  

`ebay-dl.py`does this by generating an eBay search url that includes the specified `search_term`, then scrapes through the pages html looking for css selectors that correspond with the data we're looking for (`name`, `price`, `status`, `shipping` cost, and if it has `free_returns`). As the code is scraping this data, itemized results are being added to a dictionary that will be downloaded as a `.json` file once the code has finished running.



## Instructions

**1. Download python file `ebay-dl.py`**

**2. Enter in the command line:**
 ```  
 $ python3 ebay-dl.py 'search_term' 
 ```
`'search_term'` will need to be replaces with the item you'd like to scrape data for.
The search term must be contained in 'quotes' in order for the code to work with multiple word search terms.


**3. Determine Number of Pages Scraped **

This code is set to automatically attempt scraping the first ten pages of results from the code in line 60 `parser.add_argument('--num_pages', default=10)`, however you can change the number of pages you'd like scraped with the command line below: 
 ```  
 $ python3 ebay-dl.py 'search_term' --num_pages=5
 ```
The above example searches five pages, replace the 5 with the amount of pages you'd like. 

*important note:* eBay might limit the number of pages they'll allow you to scrape after sensing that youre using this program to do your scraping. 

**4. Enjoy your new JSON file!**

