# Proxy-List-Scrapper 
#### [demo live example using javascript](https://narkhedesam.github.io/Proxy-List-Scrapper)
<p align="center">
    <img width="460" height="300" src="https://raw.githubusercontent.com/narkhedesam/Proxy-List-Scrapper/master/_Proxy-List-Scrapper%20logo.jpg">
</p>
<p align="center">
    <a href="https://paypal.me/sameernarkhede/250">
        <img src="https://img.shields.io/badge/Donate-PayPal-green.svg" alt="paypal" />
    </a>
    <img src="https://img.shields.io/github/license/narkhedesam/Proxy-List-Scrapper" alt="Proxy-List-Scrapper licence" />
    <img src="https://img.shields.io/github/forks/narkhedesam/Proxy-List-Scrapper" alt="Proxy-List-Scrapper forks" />
    <img src="https://img.shields.io/github/stars/narkhedesam/Proxy-List-Scrapper" alt="Proxy-List-Scrapper stars" />
    <img src="https://img.shields.io/github/issues/narkhedesam/Proxy-List-Scrapper" alt="Proxy-List-Scrapper issues" />
    <img src="https://img.shields.io/github/issues-pr/narkhedesam/Proxy-List-Scrapper" alt="Proxy-List-Scrapper pull-requests" />
</p>
<br/><br/>
Proxy List Scrapper from various websites. 
They gives the free proxies for temporary use.

### What is a proxy
A proxy is server that acts like a gateway or intermediary between any device and the rest of the internet. A proxy accepts and forwards connection requests, then returns data for those requests. This is the basic definition, which is quite limited, because there are dozens of unique proxy types with their own distinct configurations.

### What are the most popular types of proxies:
Residential proxies, Datacenter proxies, Anonymous proxies, Transparent proxies

### People use proxies to:
Avoid Geo-restrictions, Protect Privacy and Increase Security, Avoid Firewalls and Bans, Automate Online Processes, Use Multiple Accounts and Gather Data

#### Chrome Extension in here
you can download the chrome extension "Free Proxy List Scrapper Chrome Extension" folder and load in the extension.<br/>
##### Goto Chrome Extension <a href="https://chrome.google.com/webstore/detail/free-proxy-list-scrapper/jpnflejagpflcemgfnhckkdckpkkfbcc?hl=en-US">click here</a>.

## Web_Scrapper Module <a href="https://github.com/narkhedesam/Proxy-List-Scrapper/blob/master/Web_Scrapper/README.md">here</a>
Web Scrapper is proxy web scraper using proxy rotating api https://scrape.do <br/>
 you can check official documentation from <a href="https://docs.scrape.do/">here</a>
 
<h5>You can send request to any webpages with proxy gateway & web api provided by scrape.do</h5>
<br/><br/>
## How to use Proxy List Scrapper
You can clone this project from github. or use<br/>

    pip install Proxy-List-Scrapper
 
Make sure you have installed the requests and urllib3 in python<br/>

in import add<br/>
    
    from Proxy_List_Scrapper import Scrapper, Proxy, ScrapperException

After that simply create an object of Scrapper class as "scrapper"<br/>

    scrapper = Scrapper(category=Category, print_err_trace=False)

Here Your need to specify category defined as below:<br/>

    SSL = 'https://www.sslproxies.org/',
    GOOGLE = 'https://www.google-proxy.net/',
    ANANY = 'https://free-proxy-list.net/anonymous-proxy.html',
    UK = 'https://free-proxy-list.net/uk-proxy.html',
    US = 'https://www.us-proxy.org/',
    NEW = 'https://free-proxy-list.net/',
    SPYS_ME = 'http://spys.me/proxy.txt',
    PROXYSCRAPE = 'https://api.proxyscrape.com/?request=getproxies&proxytype=all&country=all&ssl=all&anonymity=all',
    PROXYNOVA = 'https://www.proxynova.com/proxy-server-list/'
    PROXYLIST_DOWNLOAD_HTTP = 'https://www.proxy-list.download/HTTP'
    PROXYLIST_DOWNLOAD_HTTPS = 'https://www.proxy-list.download/HTTPS'
    PROXYLIST_DOWNLOAD_SOCKS4 = 'https://www.proxy-list.download/SOCKS4'
    PROXYLIST_DOWNLOAD_SOCKS5 = 'https://www.proxy-list.download/SOCKS5'
    ALL = 'ALL'

These are all categories.<br/>
After you have to call a function named "getProxies"<br/>

    # Get ALL Proxies According to your Choice
    data = scrapper.getProxies()

the data will be returned by the above function the data is having the response data of function.<br/>
in data having proxies,len,category
 - @proxies is the list of Proxy Class which has actual proxy.<br/>
 - @len is the count of total proxies in @proxies.<br/>
 - @category is the category of proxies defined above. <br/> 
<br/>


## You can handle the response data as below


    # Print These Scrapped Proxies
    print("Scrapped Proxies:")
    for item in data.proxies:
        print('{}:{}'.format(item.ip, item.port))

    # Print the size of proxies scrapped
    print("Total Proxies")
    print(data.len)

    # Print the Category of proxy from which you scrapped
    print("Category of the Proxy")
    print(data.category)
  
## Author 
<b>Sameer Narkhede</b> <br/>
<p align="left">
  <a href="https://github.com/narkhedesam" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg" alt="https://github.com/narkhedesam" height="20" width="20" />
  </a>
  <a href="https://narkhedesam.com/" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/googlechrome.svg" alt="https://narkhedesam.com/" height="20" width="20" />
  </a>
  <a href="https://www.linkedin.com/in/sameer-narkhede/" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="https://www.linkedin.com/in/sameer-narkhede/" height="20" width="20" />
  </a>
  <a href="https://www.facebook.com/narkhedesam" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/facebook.svg" alt="https://www.facebook.com/narkhedesam" height="20" width="20" />
  </a>
  <a href="https://www.instagram.com/sam_narkhede/" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" alt="https://www.instagram.com/sam_narkhede/" height="20" width="20" />
  </a>
  <a href="https://t.me/narkhedesam" target="blank">
    <img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/telegram.svg" alt="https://t.me/narkhedesam" height="20" width="20" />
  </a>

</p>

### Thanks for giving free proxies
 - https://www.sslproxies.org/
 - https://www.google-proxy.net/
 - https://free-proxy-list.net/anonymous-proxy.html
 - https://free-proxy-list.net/uk-proxy.html
 - https://www.us-proxy.org/
 - https://free-proxy-list.net/
 - http://spys.me/proxy.txt
 - https://proxyscrape.com/
 - https://www.proxynova.com/proxy-server-list/
 - https://www.proxy-list.download/
<br/><br/>


## Take a look here


![Screenshot](https://raw.githubusercontent.com/narkhedesam/Proxy-List-Scrapper/master/Screenshot.png)


<!-- ## Donation -->

<!-- If this project help you reduce time to develop, you can give me a cup of coffee :relaxed:  -->
<!-- <br/> -->

<!-- [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/sameernarkhede/250) -->

 
