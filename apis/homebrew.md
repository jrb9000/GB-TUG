# 🍺 Homebrew

{% embed url="https://formulae.brew.sh/docs/api" %}

### Metadata

#### List formulae metadata for all [core](https://github.com/Homebrew/homebrew-core) or [cask](https://github.com/Homebrew/homebrew-cask) formulae...

```python
# Get a list of all current homebrew/homebrew-core formula
requests.get('https://formulae.brew.sh/api/formula.json').json()

# Get a list of all current homebrew/homebrew-cask formula
requests.get('https://formulae.brew.sh/api/cask.json').json()
```

### Analytics

{% embed url="https://formulae.brew.sh/analytics" %}

#### List one category of analytics events&#x20;

List all analytics events for a specified category over a number of days, ordered by event frequency count. This is the data source for `brew info --analytics`.

```python
# Get homebrew analytics data for event category
def get_homebrew_analytics(analytics_event_category, num_days):
    base = 'https://formulae.brew.sh/api'
    path = f'/analytics/{analytics_event_category}/{num_days}.json'
    url = base + path
    return requests.get(url).json()
```

Available analytics event categories are

* `install` _- The installation of all formulae_
* `install-on-request` _- The requested installation of all formulae (i.e. not as a dependency of other formulae)_
* `cask-install` _- The installation of all casks_
* `build-error` _- The installation failure of all formulae_
* `os-version` _- The macOS version of all machines that have submitted an event_

