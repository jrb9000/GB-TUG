# Open Page Rank

{% embed url="https://www.domcop.com/openpagerank/what-is-openpagerank" %}
Open PageRank
{% endembed %}

> The Open PageRank initiative was created to bring back Page Rank metrics so that different domains could easily be compared. We do this using Open Source data provided by [Common Crawl](http://commoncrawl.org) and [Common Search](https://about.commonsearch.org).

###

### Limits

* You can call the API 1800 times in a single hour.
* max 100 domains can be sent in a single API call

### Python Example

```python
import requests
from urllib.parse import urlencode

base_url = 'https://openpagerank.com/api/v1.0/getPageRank'
headers = {'API-OPR': f'{FREE_API_KEY}'}
payload = {'domains[]': ['google.com', 'apple.com', 'unknowndomain.com']}

query_str = urlencode(payload, doseq = True)

url = f'{base_url}?{query_str}'

resp = requests.get(url, headers = headers)
resp.json()

```



