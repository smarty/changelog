# [Rust SDK](https://www.smarty.com/docs/sdk/rust)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.12] - 2023-11-15

### Changed:

- Update International Autocomplete to v2
- Changed default endpoint of international-autocomplete-api to: "https://international-autocomplete.api.smarty.com/v2/lookup"
- Removed `super-administrative-area` and `sub-administrative-area` fields from `Suggestion`
- Added `entries` (int) , `address_text` (string), and `address_id` (string) fields to `Suggestion`
- Added functionality to append `address_id` to URL path, not as query parameter
- Removed `distance` , `geolocation` , `include_only_administrative_area` , `latitude` , and `longitude` fields from `Lookup`
- Removed `international_geolocate_type`
- Fixed example for us-autocomplete-pro

## [0.2.10] - 2023-10-24

### Changed:

- Removed unused value in us-street api.


## [0.2.9] - 2023-10-24

### Changed:

- Updated us-street and us-extract api tests.


## [0.2.8] - 2023-10-24

### Changed:

- Added format field to us-street api.