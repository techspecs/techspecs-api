[![GitHub stars](https://img.shields.io/github/stars/techspecs/api.svg)](https://github.com/techspecs/api/stargazers)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/shakee93/fonoapi/master/LICENSE)

# Getting Started With TechSpecs API

TechSpecs API provides the easiest way to get instant access to the official technical specifications of the worlds' consumer electronics. Our database is the largest and most up-to-date in the world so you can be sure you're always getting the latest information. 

**Available categories;**
* Smartphones
* Tablets
* Smartwatches
* Laptops

**Available Endpoints;**
* Product Search
* Product Details
* Get All Categories
* Get All Brands
* Get All Products

**Available Datapoints;**
* Specifications: **Dimension, Weight, Display, Camera, Battery, CPU, GPU, and over 200 more…**
* Images: **Front view, Back view**
* Launch Prices: Available for iOS devices


## Prerequisite: Get your TechSpecs API Key & URL
Visit https://techspecs.io to signup and get your API key. Registration is free, no credit card required.

## 1. Product Search
### Python Example

```python
import requests

url = "https://api.techspecs.io/v4/product/search?query=iPhone%2014"

headers = {
    "accept": "application/json",
    "Authorization": "Bearer techspecs_api_key",
    "content-type": "application/json"
}

response = requests.post(url, headers=headers)

print(response.text)
```

### Node Example 
```node
const sdk = require('api')('@techspecs/v3.0#5dlse1lclezifmcf');

sdk.searchProducts({query: 'iPhone%2014', authorization: 'Bearer techspecs_api_key'})
  .then(({ data }) => console.log(data))
  .catch(err => console.error(err));
```
### PHP Example
```php
<?php
require_once('vendor/autoload.php');

$client = new \GuzzleHttp\Client();

$response = $client->request('POST', 'https://api.techspecs.io/v4/product/search?query=iPhone%2014', [
  'headers' => [
    'Authorization' => 'Bearer techspecs_api_key',
    'accept' => 'application/json',
    'content-type' => 'application/json',
  ],
]);

echo $response->getBody();
```
## Docs and code samples
Visit https://techspecs.readme.io to read the documentation. 

## Feedback
Visit https://feedback.techspecs.io/ to share your feedback and/or feature requests.

## Support
Email: support@techspecs.io

