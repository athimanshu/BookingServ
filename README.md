# BookingService

## Solution
 ---
 
### API's

```
Get All booking
Url: http://localhost:8080/v1/bfs/booking/
Method: GET
Response: [{
	"id": 1,
	"first_name": "Himanshku",
	"last_name": "Sicsngh",
	"date_of_birth": "20-07-1994",
	"checked_in": "20-07-1994",
	"checked_out": "20-07-1994",
	"total_price": 900.0,
	"deposit": 700.0,
	"address": {
		"line1": "line1",
		"line2": "line2",
		"city": "",
		"state": "Karnataka",
		"country": "india",
		"zipcode": "560037"
	}
}]
```

```
Create New Booking
Url:http://localhost:8080/v1/bfs/booking
Method: PUT
Request: {
	"first_name": "Himanshku",
	"last_name": "Sicsngh",
	"date_of_birth": "20-19-1993",
	"total_price": 900.00,
	"deposit": 700.00,
	"checked_in": "20-19-1993",
	"checked_out": "20-19-1993",
	"address": {
		"line1": "line1",
		"line2": "line2",
		"state": "Karnataka",
		"city": "",
		"country": "india",
		"zipcode": "560037"
	}
}

```

### Idempotency
This logic is applied on basis of first and last name. If both are same then we get exception saying booking exist for that user.
