# [Rust SDK](https://www.smarty.com/docs/sdk/rust)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.4] - 2024-10-16

- international-street-api
    - Added new return fields additionalContent
        - deliveryInstallation
        - deliveryInstallationType
        - deliveryInstallationQualifierName
        - route
        - routeNumber
        - routeType

## [0.4.3] - 2024-07-03

- International Autocomplete API
    - Added two new fields to expose the administrative area long name and short (abbreviated) form:
        - administrative_area_short
        - administrative_area_long


## [0.4.2] - 2024-06-17

- Added with proxy to options.
- Includes fix for typos in json.

## [0.4.0] - 2024-04-05

### Changed:

- Adjusted the has_param function to use generics.
-  Adjusted OptionsBuilder to ensure that it can't fail.
-  Renamed SDKError to SmartyError
-  Changed the SmartyError type to be an enum and that will allow for catching errors for user side.

## [0.3.1] - 2024-03-19

### Changed:

- Updated return fields of `us-enrichment` to match the corresponding live api response

## [0.3.0] - 2024-01-10

### Changed:

- Added US Enrichment Api.

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