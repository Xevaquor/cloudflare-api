# Welcome

This is Mavenized fork of https://github.com/LoadLow/CloudflareApiLibrary project by LoadLow.


CloudflareApiLibrary
====================

Use Cloudflare API in Java
- Documentation of API : http://www.cloudflare.com/docs/client-api.html
- Documentation of my Lib : http://loadlow.github.io/CloudflareApiLibrary/

`````
  This lib allows you to use easier and faster the CloudflareAPI.
  (Used libs like ApacheHTTP, JSON... are in the "lib" folder)
`````

<h4>Exemple using requests :</h4>
(All CloudflareRequests are in the "com.cloudflare.api.requests" package)
`````java
CloudflareAccess access = new CloudflareAccess(
                "CF_MAIL",
                "CF_APIKEY");
        
CloudflareRequest request = new CloudflareRequest(access, ...);
try {
            boolean result = request.execute();
            System.out.println("Operation executed : " + result);
} catch (CloudflareError e) {
            e.printStackTrace();
}
`````

<h4>Informations :</h4>
- This lib returns API errors with Exceptions (CloudflareException)
- The package constants contains ALL constants of the CloudflareAPI (even if some unused)
- This API is available for all Cloudflare accounts (and free accounts!)

<h4>Required :</h4>
- A Cloudflare Account
- An APIKey generated on the Cloudflare Account Settings panel
- The mail of your account
- A specific domain using Cloudflare and linked with your Cloudflare Account

<h4>Available :</h4>
- Create/Edit DNS Records (CNAME, MX, AA, AAAA, SPF, NS, TXT, LOC)
- Edit Cache Level (Aggressive, basic)
- Trust/Block/Unlist IP Address
- Modify Minify Level (JS, HTML, CSS)
- Change RocketLoader Status(Off, Automatic, Manual)
- Edit Security Level(UnderAttack, Hight, Medium, Low, Essentialy off)
- Purge cache and purge a specified file from cache
- Toggle Always Online status
- Toggle Development mode 
- Toogle IPV6 Support
- Update zone challenge stats

<h4>TODO :</h4>
- Parsing Statistics Responses
- Create SRV Record
