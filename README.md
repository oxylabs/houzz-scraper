# Houzz Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Houzz Scraper](https://oxylabs.io/products/scraper-api/ecommerce/houzz?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Houzz website effortlessly. This brief guide explains how an Houzz Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Houzz results by providing your own URLs to our service. We can return the HTML for any Houzz page you like.

#### Python code example

The example below illustrates how you can get HTML of Houzz page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.houzz.com/photos/kitchen-ideas-and-designs-phbr0-bp~t_709'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/houzz-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-US\"><head><title>75 Kitchen Ideas You&#x27;ll Love - December, 2023 |  ... </html>",
      "created_at": "2023-12-18 10:28:06",
      "updated_at": "2023-12-18 10:28:09",
      "page": 1,
      "url": "https://www.houzz.com/photos/kitchen-ideas-and-designs-phbr0-bp~t_709",
      "job_id": "7142460512167555073",
      "status_code": 200
    }
  ]
}
```
With our Houzz Scraper, you can conveniently draw out public data from any Houzz webpage. This tool allows you to amass desired information related to home design, remodeling ideas, landscaping diagrams or furniture specifications. Use this data to understand the latest trends and keep your business innovative and competitive. For any inquiries, do not hesitate to reach out to our support team through live chat, or send us an e-mail at hello@oxylabs.io.