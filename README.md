[![GitHub stars](https://img.shields.io/github/stars/techspecs/api.svg)](https://github.com/techspecs/api/stargazers)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/shakee93/fonoapi/master/LICENSE)

# Getting Started With TechSpecs API

TechSpecs API provides the easiest way to get instant access to the official technical specifications of the worlds' consumer electronics. Our database is the largest and most up-to-date in the world so you can be sure you're always getting the latest information. 

**Available categories;**
* Smartphones
* Tablets
* Smartwatches

**Available Features;**
* Search for a product
* Get the detailed specifications of a product
* Get a list of all product categories
* Get a list of all brands
* Get a list of all products from a specific brand

**Available Datapoints;**
* Specifications: **Dimension, Weight, Display, Camera, Battery, CPU, GPU, and over 200 more…**
* Images: **Front view, Back view**
* Launch Prices: Available for iOS devices


## Prerequisite: Get your TechSpecs API Key & URL
Visit https://developer.techspecs.io/ to signup and get your API key. Registration is free, no credit card required.

## 1. Product Search
### Python Example

```python
import requests

url = "YOUR URL"

payload = {"category": "smartphone"}
headers = {
    "Accept": "application/json",
    "x-blobr-key": "YOUR API KEY",
    "Content-Type": "application/json"
}

response = requests.request("POST", url, json=payload, headers=headers)

print(response.text)
```

### Node Example 
```node
const sdk = require('api')('@techspecs/v3.0#3co1cxkzu4d7xe');

sdk['search-products']({category: 'smartphone'}, {
  query: 'iPhone%2013',
  'x-blobr-key': 'YOUR API KEY'
})
  .then(res => console.log(res))
  .catch(err => console.error(err));
```
### PHP Example
```php
<?php
require_once('vendor/autoload.php');

$client = new \GuzzleHttp\Client();

$response = $client->request('POST', 'YOUR URL', [
  'body' => '{"category":"smartphone"}',
  'headers' => [
    'Accept' => 'application/json',
    'Content-Type' => 'application/json',
    'x-blobr-key' => 'YOUR API KEY',
  ],
]);

echo $response->getBody();
```
## Read the Docs
Visit https://techspecs.readme.io to read the documentation. 


## Search Engine Demo
Visit https://techspecs.io to try the frontend search engine

## Feedback
Visit https://feedback.techspecs.io/ to share your feedback and/or feature requests.

## Support
Email: support@techspecs.io

