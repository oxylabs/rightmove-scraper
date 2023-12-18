# Rightmove Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Rightmove Scraper](https://oxylabs.io/products/scraper-api/web/rightmove?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Rightmove website effortlessly. This brief guide explains how an Rightmove Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Rightmove results by providing your own URLs to our service. We can return the HTML for any Rightmove page you like.

#### Python code example

The example below illustrates how you can get HTML of Rightmove page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.rightmove.co.uk/property-for-sale.html'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/rightmove-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width=dev ... </html>",
      "created_at": "2023-12-18 11:20:40",
      "updated_at": "2023-12-18 11:20:51",
      "page": 1,
      "url": "https://www.rightmove.co.uk/property-for-sale.html",
      "job_id": "7142473742176776193",
      "status_code": 200
    }
  ]
}
```
With our Rightmove Scraper, you can seamlessly amass public data from any Rightmove web page. Compile crucial real estate data like property prices, property reviews, number of bedrooms, property location or descriptions to evaluate the real estate market and gain an edge over your rivals. If you require any assistance, feel free to reach out to our support team through live chat or drop an email at hello@oxylabs.io.