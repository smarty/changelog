# [.Net SDK](https://smartystreets.com/docs/sdk/dotnet)


## 7.1.1 (August 31, 2017)

FEATURES:

- International Street API: AddressFormat field has returned to response.


## 7.1.0 (August 1, 2017)

FEATURES:

- US Autocomplete API: Added PreferRatio to lookup.

IMPROVEMENTS:

- US Autocomplete API: MaxSuggestions and PreferRatio are not added to url query string if set to default values.


## 7.0.0 (July 18, 2017)

BREAKING CHANGES:

- Now using consistent collection types for results.
- Client.Send() now void for across all APIs.