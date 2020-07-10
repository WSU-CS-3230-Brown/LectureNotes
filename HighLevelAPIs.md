# High Level APIs #

* Instead of using ports and sockets you'll use URI's and URL's
* URI - Universal resource identifier
* URL - Locator
* URI vs URL

    * <https://www.w3.org/TR/uri-clarification/>
    * confusion between the two because they get used interchangeably a lot
    * URI is an identifier that might not provide enough information to access the resource it identifies
    * A URL is an identifier that includes information about how to access the resource
    * URI can be relative
    * URI can specify a relative path, URL has to be absolute

* convert between URI and URL

    * provide what method you want to use requires and it should work.
    * when using java.net Use a URI until you actually want to access the resource then convert to the URL

* Ascheme

    * part of the URI or URL that appears before the colon

        * `http://www.blah.com` the scheme is http
        * `ftp://`
        * `file://`
        * another way to define a url is that it's an HTTP URI

* don't worry too much about the terminology
* High-level vs low-level java api

* low level classes
    * Socket
    * ServerSocket
    * DatagramSocket

* High level classes

    * URI
    * URL
    * URLConnection
    * HttpURLConnection

* URI has nine components

    1.  scheme - you can write you own but it's ill advise due to name conflicts
    2.  scheme-specific part - identifier for the. resource you want to use
    3.  authority - host password username and port
    4.  user-info
    5.  host - can be ipv4/6 address or hostname
    6.  port
    7.  path - /path/to/resource on the host
    8.  query - separated by a ? can be any format but usually is kv pair
    9.  fragment - specifies a secondary resource or location

* uri doesn't have to be valid until you convert it to a url

## HttpUrlConnection ##

* When your browser asks for a web page it does a GET request
* the server that hosts the page will respond
* The response will include a status code

    * 200 means OK
    * 404 means not found
    * 500 a server-side error

* Providing data is done with a POST request