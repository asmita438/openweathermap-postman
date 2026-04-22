## OpenWeatherMap API Testing - Postman Collection

A Postman collection with 4 test cases for the OpenWeatherMap API, querying current weather data for London, UK.

## Test Cases

| # | Name | What it tests |
|---|------|--------------|
| TC-01 | Verify Latitude and Longitude | `coord.lat === 51.51` and `coord.lon === -0.13` |
| TC-02 | Verify Response Status Code | HTTP 200, JSON Content-Type, response time < 5s |
| TC-03 | Verify City Name in Response | `name === "London"` and `sys.country === "GB"` |
| TC-04 | Verify Temperature Data | `main.temp`, `main.humidity`, `wind.speed` exist and are numbers |

## Files

- `OpenWeatherMap_Collection.postman_collection.json` — Postman collection with all 4 requests and test scripts
  

## How to Run

1. Import  JSON files into Postman via **Import**
2. Click **Run collection**

## Variables Used

| Variable | Description |
|---|---|
| `{{base_url}}` | OpenWeatherMap API base URL |
| `{{api_key}}` | API key for authentication |
| `{{city}}` | City query (`London,uk`) |
| `{{expected_lat}}` | Expected latitude (`51.51`) |
| `{{expected_lon}}` | Expected longitude (`-0.13`) |
