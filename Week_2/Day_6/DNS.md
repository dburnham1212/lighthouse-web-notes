[Table Of Contents](../../README.md)

# DNS

When you type a URL into a browser and press ↵, a website magically appears on your screen. How does that work? What are the steps that are performed in between the time the request is started and the time a response is delivered?

One fundamental step in this process involves a system called DNS, or Domain Name System, and it dates back to the beginning of the Internet itself!

A web URL is essentially an alias for an IP address (or many IP addresses) that requests can be routed to.

The Domain Name System is indisputably one of the most important and overlooked parts of the internet. Without DNS the internet as we know it today would collapse.

DNS is used to translate a domain name into a usable IP adress.

## How Does It Work?

First we should note that when we type in www.example.com we are actually browsing for the webpage www.example.com. with an added "." at the end. This extra "." represents the root of the internets namespace. 

When you first search for www.example.com. your browser and operating system will first determine if they know what the address is already. It could be configured on your computer or could be stored in memory. If neither the browser or the operating system know where www.example.com. is the operating system is configured to ask a resolving name server for IP adresses it does not know. The resolving name server is the workhorse of the DNS lookup, it is configured either manually or automatically within your operating system.

The only thing that all resolving name servers should know is where to find the root name servers. The root name servers will direct the resolving name server to the com name servers. The com name servers are also called the top level domain servers or TLD for short. The resolving name server then takes all this information from the root name servers puts it in its cache and then goes directly to the com TLD name servers.

When the resolving name server querys www.example.com the TLD name servers then redirect the resolving name server to the authoritative name servers. The resolving name server takes the response from the TLD name servers, stores it in cache, and then querys the example.com name servers. From there the autoritative name server will respond by providing the appropriate IP adress. The resolving name server then takes this information, puts it in cache, and gives the reply to the operating system. The operating system then gives this information to the browser and makes a connection to the IP address.

