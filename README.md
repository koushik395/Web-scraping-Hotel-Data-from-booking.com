# Web-scraping-Hotel-Data-from-booking.com

The hotel industry is continuously growing for the last 15 years since the last recession. With growth, competition has also increased in the industry.Every other day market welcomes new vendors and with that profit margins get narrow for the old vendors. So, it has become quite challenging for the OTAs to keep up with the booking revenue.<br>
But OTAs can overcome this problem by tracking their competitor’s pricing. But the question is how can you track them? Well, here not only web scraping can help you track your competitors but will also improve your revenue.<br>
Now we are going to scrape booking.com with python. By the end,we will be able to scrape prices and other details of any hotel from booking.com

These are the following data points that we are going to scrape from the target website.

* Address
* Name
* Pricing
* Rating
* Room Type
* Facilities
* Room sqft

Obviously, hotel data scraping goes beyond this and this was just an example of how python can be used for scraping Booking.com for price comparison purposes. You can use Python for scraping other websites like Expedia, Hotels.com, etc.<br>
But scraping at scale would not be possible with this process. After some time booking.com will block your IP and your data pipeline will be blocked permanently. For seamless scraping use Web Scraping API which will rotate IPs on every new request and will use headless chrome to reduce any chance of blockage.

## Why use Python to Scrape booking.com
Python is the most versatile language and is used extensively with web scraping. Moreover, it has dedicated libraries for scraping the web.
With a large community, you might get your issues solved whenever you are in trouble.

## Requirements for scraping booking.com
We need Python 3.x for this tutorial and I am assuming that you have already installed that on your computer. Along with that, you need to install two more libraries which will be used further in this tutorial for web scraping.

1. **Requests** will help us to make an HTTP connection with Bing.
1. **BeautifulSoup** will help us to create an HTML tree for smooth data extraction.

## How to scrape the data points
Since we have already decided which data points we are going to scrape let’s find their HTML location by inspecting chrome.

For this tutorial, we will be using the find() and find_all() methods of BeautifulSoup to find target elements. DOM structure will decide which method will be better for each element.

First we will be taking the input of journey Date and Destination and other relevant details. Next we will iterate throughout the web page and extract all the "<a>" tag which are the Links. After that we will iterate through each and every linked Pages and extract all the links.

After our Job is done by extracting we will create a soup object to parse the html page and we will use the required functions to extract the Data from the Web Pages.

### Extracting hotel name and address
hotel name can be found under h2 tag with class pp-header__title.
hotel address can be found under span tag with data-node_tt_id as attribute.

**Here BS4 will use an HTML parser to convert a complex HTML document into a complex tree of python objects.**

**In a similar manner, we will extract the address,Rating,Facilities,Room_type.**

After we have Web scraped the Booking.com website and gathere relevant information we have converted that data into a Pandas Dataframe. The sample output is attached below.

![Output](https://github.com/koushik395/Web-scraping-Hotel-Data-from-booking.com/blob/main/output.JPG?raw=true)

**The Full resultant CSV file is attached in the Repository**
