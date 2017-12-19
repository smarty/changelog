# [Go SDK](https://smartystreets.com/docs/sdk/go)


## 6.5.1 (December 4, 2017)

FEATURES:

- International Street API: New repsonse field: PremisePrefixNumber


## 6.5.0

NO CHANGES (This version number was, for some unknown reason, skipped by the development team.)


## 6.4.1 (September 29, 2017)

BUG FIXES:

- US Street API: Prevent nil-reference panic upon deserialization of response.


## 6.4.0 (September 12, 2017)

FEATURES:

- US Extract API: Exported 'HTML' enum type


## 6.3.0 (September 11, 2017)

FEATURES:

- International Street API: Exported 'Language' enum type
- US Autocomplete API: Exported 'Geolocation' enum type


## 6.2.0 (August 30, 2017)

FEATURES:

- International Street API: Reinstated the AddressFormat field (removed at version 6.0.0).


## 6.1.1 (August 23, 2017)

IMPROVEMENTS:

- CSV reader and writer abstractions simplified.


## 6.1.0 (August 1, 2017)

FEATURES:

- US Autocomplete API: PreferRatio added to lookup.


## 6.0.0 (June 15, 2017)

BREAKING CHANGES:

- International Street API: Removed AddressFormat field

FEATURES:

- Wireup Client Builder: WithHTTPRequestTracing() method provides more detailed HTTP-level tracing.
