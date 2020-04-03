# SDC_CRUD_v2
v2 for SDC project

### POST

`/api/houses/{ houseId }/images`

**Purpose**: Adding a new image of the house

______________________________________________________
### GET

`/api/houses/{ houseId }`

**Purpose**: Get all the information on a house

**Response**: JSON object containing a house's information
```json
{
  "id": int,
  "neighborhood": string,
  "home_cost": int,
  "bedrooms": int,
  "bathrooms": int,
  "home_address": string,
  "sf": int,
  "home_image": url string,
  "heart_filled": boolean
}
```

`/api/houses/{ houseId }/neighborhood`

**Purpose**: Retrieving nearby restaurants

**Data Params**

`{ name: <neightborhood name> }`

**Response**: JSON object containing an array of homes in the neighborhood.
```json
[
  "id": int,
  "neighborhood": string,
  "home_cost": int,
  "bedrooms": int,
  "bathrooms": int,
  "home_address": string,
  "sf": int,
  "home_image": url string,
  "heart_filled": boolean
]
```

`/api/houses/{ houseId }/likes`

**Purpose**: Retrieving like status of a house.

**Data Params**

`{ houseId: <int> }`

**Response**: like status of a house.

```json
[
  {
        "heart_filled": <int>
    }
]
```

`/api/neighborhoods`

**Purpose**: Retriving the neighborhood information.

**Data Params**

`{ name: <neighborhood name> }`

**Response**: like status of a house.

```json
{
 "id": int,
 "neighborhood": string,
 "transit_score": int,
 "walk_score": int,
 "value_inc_dec_past": int,
 "value_inc_dec_future": int,
 "median_value": int
  }
```
______________________________________________________
### PATCH

`/api/houses/{ houseId }/likes`

**Purpose**: Update like status of a house.

**Data Params**

`{ houseId: int }`
______________________________________________________
### DELETE

`/api/houses/{ houseId }/delete`

**Purpose**: Removing a house.

**Data Params**

`{ houseId: int }`
