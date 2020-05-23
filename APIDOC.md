# *FILL IN NAME* API Documentation
*Fill in a short description here about the API's purpose.*

## *Fill in Endpoint 1 Title*
**Request Format:** /allimages

**Request Type:** GET

**Returned Data Format**: JSON

**Description:** Returns all photo JSON objects.


**Example Request:** /allimages

**Example Response:**

```json
[
  {
    "title": "DOUG01",
    "cap": "Douglas at the beach with a smol Addy behind him",
    "date": "03-09-2020",
    "src": "alki-doug-1.jpg",
    "type": "landscape",
    "shoot": "Alki Beach with Douglas"
  },
  {
    "title": "DOUG02",
    "cap": "Douglas at the beach",
    "date": "03-09-2020",
    "src": "alki-doug-2.jpg",
    "type": "landscape",
    "shoot": "Alki Beach with Douglas"
  },
  {
    "title": "STAN01",
    "cap": "An harbour at Stanley Park",
    "date": "11-10-2019",
    "src": "canada-1.jpg",
    "type": "landscape",
    "shoot": "canada-veterans-weekend"
  },
  ...
  {
    "title": "SF05",
    "cap": "Kimi No Nawa lookin' street",
    "date": "07-22-2019",
    "src": "sf-summer-2019-6.jpg",
    "type": "landscape",
    "shoot": "Summer in SF!"
  }
]
```

**Error Handling:**
Possible 500 error (Internal Server Error). If error occurs, returns an error with the message:
`Image retrieval failed. Please try again.`)

## *Fill in Endpoint 2 Title*
**Request Format:** /shoot/:shoot

**Request Type:** GET

**Returned Data Format**: JSON

**Description:** Returns all JSON objects that have the value of the given shoot for key `shoot`.

**Example Request:** /shoot/canada-veterans-weekend

**Example Response:**
*Fill in example response in the {}*

```json
[{"title":"STAN01","cap":"An harbour at Stanley Park","date":"11-10-2019","src":"canada-1.jpg","type":"landscape","shoot":"canada-veterans-weekend"},{"title":"STAN02","cap":"Simon and Tak slightly blurry in from of an harbour at Stanley Park","date":"11-10-2019","src":"canada-2.jpg","type":"portrait","shoot":"canada-veterans-weekend"},{"title":"SIM01","cap":"Simon on some random street in Vancouver wow pretty lights","date":"11-10-2019","src":"canada-3.jpg","type":"portrait","shoot":"canada-veterans-weekend"},{"title":"TAK01","cap":"Lonely Tak on some random street in Vancouver","date":"11-10-2019","src":"canada-4.jpg","type":"landscape","shoot":"canada-veterans-weekend"}]
```

**Error Handling:**
- Possible 500 error (Internal Server Error).
  - If error occurs, returns an error with the message: `Image retrieval failed. Please try again.`
- Possible 400 (invalid request) errors (all plain text):
  - If missing a parameter, returns an error with the message: `Missing POST parameter: shoot`
