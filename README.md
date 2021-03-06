## search for a website with a different proxy each time
This script automates the process of searching for a website via keywords
and the Bing search engine.... page after page.
<br><br>
Pass a complete URL and at least 1 keyword as command line arguments:
<br>
python3 https://www.roboshout.com texts
<br><br>
Or with multiple search terms:
<br>
python3 https://site.com keyword1 keyword2 keyword2 ....
<br><br>
It first scrapes a list of proxies from the web
using <a href="https://www.sslproxies.org">SSL Proxies</a>.
<br><br>
When the object is initialized in the constructor, the following method is called:
<br><br>
self.__scrape_socket()
<br><br>
This saves each ip/port for each proxy server into a list after scraping the table
of proxy servers from sslproxies.org.
<br><br>
Then using a new socket from the list for each iteration, a random keyword is
searched for via https://www.bing.com until the desired website is found.
<br><br>
The website is then visited, and one link is randomly clicked within the website.
<br><br>
Due to the slow performance of most (but not all) proxy servers, it's important to
<i>slow</i> the bot down using the built in time module.
<br><br><b>
proxy_crawler_CONSOLE.py is the same exact script but uses pyvirtualdisplay to restrict
output to the console (NO GUI). The package "xvfb" may need to be installed along with
pyvirtualdisplay.
</b><br><br>
This was developed on Ubuntu 16.04.4 LTS with selenium/geckodriver and firefox 60.0
<br><br>
I use this version of geckodriver on Ubuntu:
<br><br>
<b>wget https://github.com/mozilla/geckodriver/releases/download/v0.23.0/geckodriver-v0.23.0-linux64.tar.gz</b>
<br><br>
Geckodriver should be saved somewhere in your PATH... ie: /usr/local/bin
<hr>
<b>Author: James Loye Colley  22MAY2018</b>
