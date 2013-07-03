# Production env
* SSL supplier: *https://www.cheapssls.com/*

# Development env
* Pow (http://pow.cx/): Rack Server for OS X (generates .dev domains and allows multiple server runnign side-by-side)
* PowSSL (https://gist.github.com/paulnicholson/2050941): generates SSL certificates to be used with Pow. **Note:** it doesn't work well with Rails as the latter won't recognize the request as through SSL. Use NGIX as a proxy instead.
* XipIO (http://xip.io): Pow compatible DNS which redirects requests to a local network's IP address. Useful as Pow requires a subdomain with the name of the app to be accessed to (e.g. myapp.dev). If we want to try that server on another device from the same network we couldn't. For instance, supose your local IP is 10.0.0.1, you might try myapp.10.0.0.1 from another computer but that won't work as IPs are not domains. Xip.io fixes this as it will redirect all requests to its subdomains to a local IP. So, you would try for the example above to access myapp.10.0.0.1.xip.io and you're good to go, no installation required.
