
# Note

Maturity model based on which we can determine how well given web service adheres to [[REST API]] principles.

## levels

#### level 0

System does not classify as RESTful. E.g.:

```
/booking
```

#### level 1

Introduces separate endpoints, each for different resource.

```
/bookingDestinations
/bookingRooms
```

#### level 2

Introduces HTTP verbs for separating operations.

```
/destinations  -- GET 
/reservations  -- GET
/reservations  -- PUT
```

#### level 3

Introduces hypermedia controls ([[HATEOAS]]) - elements embedded in response indicating relationship between resources.

Request:

```
GET /room/?customerId=1&date=10-11-2020&hotelCode=ASTORIA
```

Response:

```
 {
    "customerId": "1",
    "reservations": [{"room": "102", "checkin": "10-11-2020", "checkout": "11-14-2020", "price": "100", "href": "https://localhost:8080/room/102"}]
 }
```

# Active recalls

## 1'st 

03-03-2026 20:53 - 2 hours after creation of that note.

RRM tells us how much Web API adheres to REST constraints. In this model we have 3 levels:

**Level 0**: API is not RESTful

**Level 1**: API has different endpoints to distinguish resources. E.g.

```
/bookingFlights
/bookingRooms
```

**Level 2**: API introduces HTTP proverbs to distinguish operations. E.g.:

```
/flights      GET
/flights      POST
/reservations POST
```

**Level 3**: Response from API shows relationships of given resource with other resources

##### What is missing

REST, RESTful - explain in my own terms

HATEOAS