# CORS Proxy

## Installation

1. Install a local version
    - Clone this repository
    - Install the server dependencies
    
        ```
        npm install
        ```
    
    - Start the server
         
         ```
         node server
         ```

## Usage

When making an API call using JavaScript (using XMLHTTPRequest, $.ajax, etc):

1. Substitute the actual service URL with the Proxy URL 

1. Set the request method, query parameters, and body as usual

1. Set the actual service URL in a header named 'Target-Endpoint'

1. Send the request as usual


## CORS Headers

The proxy allows **all** origins, methods, and headers. You probably want to lock this down in a production 
environment.


## Other Headers

The proxy currently passes the "Authorization" header to the target endpoint. You can modify the proxy to pass
 additional headers (or all of them).