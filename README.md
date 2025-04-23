# 2.4.-BaseDades_N1

# MongoDB Queries for Restaurants Collection
This project contains a collection of MongoDB queries for interacting with the `Restaurants` collection. The queries are written in JSON format and are intended to explore MongoDB’s querying capabilities.


## File
- `queries.json` – A structured list of queries using MongoDB's `find()` with filters and projections.

## Query List

### 1. Retrieve all documents
- Returns all documents in the collection.

### 2. Basic Projection
- Show `restaurant_id`, `name`, `borough`, and `cuisine`.

### 3. Projection without `_id`
- Same as above but excludes the `_id` field.

### 4. Projection with zipcode (no `_id`)
- Show `restaurant_id`, `name`, `borough`, and `address.zipcode`, excluding `_id`.

### 5. Restaurants in the Bronx
- Filters by `borough: "Bronx"`.

### 6. First 5 restaurants in the Bronx
- Uses `.limit(5)` to show first five entries.

### 7. Next 5 restaurants in the Bronx
- Skips the first 5, then limits to the next 5.

### 8. Restaurants with score > 90
- Searches for restaurants where any score is greater than 90.

### 9. Restaurants with score between 80 and 100
- Filters for scores greater than 80 but less than 100.

### 10. Latitude less than -95.754168
- Filters based on latitude from `address.coord[1]`.

### 11. Non-American cuisine, score > 70, and longitude < -65.754168 (**with `$and`**)
- Uses `$and` to combine all three filter conditions.

### 12. Same as 11, but without `$and` (implicit AND)
- Same logic, but without explicitly writing `$and`.

### 13. Non-American cuisine, grade "A", not in Brooklyn
- Sorted descending by `cuisine`.

### 14. Name starts with "Wil"
- Regex search using `^Wil`.

### 15. Name ends with "ces"
- Regex search using `ces$`.

### 16. Name contains "Reg"
- Regex search using `Reg`.

### 17. Restaurants in Bronx with American or Chinese cuisine
- Combines `borough` with `$in` operator for cuisines.

### 18. Restaurants in specific boroughs
- Filters for Staten Island, Queens, Bronx, or Brooklyn.

### 19. Restaurants not in specific boroughs
- Uses `$nin` to exclude the four main boroughs.

### 20. Restaurants with score no more than 10
- Filters with `$lte: 10`.



## Usage
You can use these queries with:
- **MongoDB Compass** – by importing the `.json` file
- **Mongo Shell / mongosh**
- **Your own Node.js/Python/Mongo scripts**




