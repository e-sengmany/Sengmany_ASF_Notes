# Web Programming - Day 11

## Bootstrap
- A CSS Framework
- Created to make front end and we more standardized


## Pros vs Cons
### Pros
- Easy to use
- Easy to customize
### Cons
- Not as fast as jQuery
- Not as powerful as Angular
- customization is limited

** Two ways of using it, installing files or using CDN

## How do we use it?
- At its core, all it is a giant CSS file.
- primarily utilized by classes


## Go To
- [Bootstrap](https://getbootstrap.com/)
- Go to Documents then pull the html code into your file.
- import to enusre that the link is in the head of your html file and the script is in the body.

### Bootstrap grid system
- internal columns are 12
- There are 6 different sizes, that are breakpoints
- which adjusts based on the screen size

## Consuming APIs
- Application Programming Interface
### Consuming APIs vs Serving/Building APIs
- Consuming APIs is when you are using an API to get data from a server.
  - Considerations
    - Does it have the data you need?
    - Cost
    - Authentication
  - Once we find an API:
    - What endpoints are available
      - ex: URL, URI
    - What methods do I use
      - ex: get, post, delete, update?
    - How is data sent?
      - ex: JSON, XML
    - How much data is sent?
    - What does the data look like?
- Serving/Building APIs is when you are creating an API to serve data to a client.

### HTTP
- There are many ways:
  - Request - backend
  - axios - only works in node/backend
  - needle 
  - AJAX
  - Fetch - works in browsser and is built into JS
    - Scaffolding 
      - fetch(endpoint)
      - .then(data)
      - .then(data)
      - .catch()errors