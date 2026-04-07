# Advaned Web Programming - 1 APR

### Dog Image Generator in React
1) Click the button
    - on click event
    - http request => utilize an endpoint
2) Image will change

- Utilize useState() and fetch() to make calls
    - fetch() => utilize endpoint
    - .then() => we will get a response, if good return parse then return, else return error
    - .then() => do something with parsed data
    - -.catch() => error handling

### Axios version
- axios()
- .then() => combines both thens from fetch
- .catch()

**one less promise because axios automatically parses the data**

## Consuming API considerations
1) Endpoints, what are available
2) Verbs, ex: GET,POST
3) What kind of data? JSON or XML
4) What does data look like? object or JSON
5) How much data are we getting back?