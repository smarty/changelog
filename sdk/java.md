# [Java SDK](https://www.smarty.com/docs/sdk/java)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.18.3] - 2024-10-31

- us-address-enrichment-api
  - Added address search

## [3.18.2] - 2024-10-18

- international-street-api
  - Added new return fields additionalContent
    - deliveryInstallation
    - deliveryInstallationType
    - deliveryInstallationQualifierName
    - route
    - routeNumber
    - routeType

## [3.18.0] - 2024-08-22

- us-address-enrichment-api
  - Added support for secondary data and secondary count

## [3.17.5] - 2024-07-03

- International Autocomplete API
  - Added two new fields to expose the administrative area long name and short (abbreviated) form:
    - administrative_area_short
    - administrative_area_long


## [3.17.4] - 2024-06-19

### Changed:

- Fixed a null pointer exception when processing empty headers.
- Added deprecated temporary flags for legacy ct counties.

## [3.17.0] - 2024-05-17

### Changed:

- Upgraded maven dependencies to mitigate risk from upstream dependency on com.squareup.okio-jvm library.

## [3.16.1] - 2023-11-28

### Changed:

- Remove a duplicate method from the code.

## [3.16.0] - 2023-11-27

### Changed:

- Add support for US Enrichment API

## [3.15.2] - 2023-11-14

### Changed:

- Updated International Autocomplete SDK example license value with correct value for v2


## [3.15.1] - 2023-11-14

### Changed:

- Updated US Autocomplete Pro SDK example to reflect correct use of Preferred City filter


## [3.15.0] - 2023-11-10

### Changed:

- Update International Autocomplete to v2
 - Change default endpoint of international-autocomplete-api to: "https://international-autocomplete.api.smarty.com/v2/lookup"
 - Remove `super-administrative-area` and `sub-administrative-area` fields from `Candidate`
 - Add `entries` (int) , `address_text` (string), and `address_id` (string) fields to `Candidate`
  - Add functionality to append `address_id` to URL path, not as query parameter
 - Remove `distance` , `geolocation` , `include_only_administrative_area` , `latitude` , and `longitude` fields from `Lookup`
 - Remove `international_geolocate_type`
 - In `international_autocomplete/client` `send()` function, add check to ensure i) `country` field on lookup is set and ii) `search` || `address_id` field is set
 - Update unit tests to cover behavior above

## [3.14.1] - 2023-10-25

### Changed:

- Added format field to us-street api.
- Changed default domain for all apis to *.api.smarty.com (was *.api.smartystreets.com). This change could affect firewall rules that allowed only the previous domain name

## [3.14.0] - 2023-07-06

### Changed:

- Added smarty_key field to us-street api.


## [3.13.16] - 2023-06-27

### Changed:

- Added "source" input and output fields to US Reverse Geo.


## [3.13.15] - 2023-01-23

### Changed:

- Adding match type and example to us extract api.

## [3.13.12] - 2023-01-23

### Changed:

- Added new fields in international-autocomplete-api results:
  - super_administrative_area, sub_administrative_area

## [3.13.11] - 2023-01-13

### Changed:

- Added new fields in international-autocomplete-api:
  - max_results, distance, geolocation, latitude, longitude

## [3.13.3] - 2022-11-08

### Changed:

- Added new fields in international-street:
  - administrative_area_short, administrative_area_long, level_type, level_number


## [3.13.2] - 2022-11-10

- Latest versions of dependencies.
- Fix to our deserializer so it won't fail when we add new fields to our REST endpoints.

### Changed:

- Reworking the rate limit code to continue trying. Looks at the returned header to know how long to wait before trying again.
- Add OKHttp as our client. This will add support back for java 8.

## [3.13.0] - 2022-08-10

### Changed:

- Reworking the rate limit code to continue trying. Looks at the returned header to know how long to wait before trying again.
- Add OKHttp as our client. This will add support back for java 8.


## [3.12.11] - 2022-05-10

### Changed:

- Removed unnecessary import.
- US Street examples default to us-core-cloud license.


## [3.12.10] - 2022-05-03

### Changed:

- MatchType is made lowercase on the payload.


## [3.12.9] - 2022-04-20

### Changed:

- Sleep for 5 seconds on 429 status code.


## [3.12.8] - 2022-04-05

### Changed:

- Dropped unnecessary commons-lang3 dependency.


## [3.12.7] - 2022-04-05

### Changed:

- Fixes for prefer_ratio in US Autocomplete Pro.
- Eliminating dependency on google http-client.


## [3.12.6] - 2022-03-16

### Changed:

- Setting "content-type" header.


## [3.12.5] - 2022-03-02

### Changed:

- Messages in US Street examples are more accurate pertaining to address validity.


## [3.12.4] - 2022-01-12

### Changed:

- Default candidates is 5 for enhanced matching.


## [3.12.3] - 2021-12-14

### Changed:

- Code to access static credentials in US Autocomplete Pro provided in example.


## [3.12.2] - 2021-10-20

### Changed:

- Correct naming on lookup query fields.


## [3.12.1] - 2021-10-14

### Changed:

- Tests for new International Autocomplete functions.


## [3.12.0] - 2021-10-14

### Changed:

- Make release accomodates later JDK version.
- Support for International Autocomplete API.


## [3.11.1] - 2021-10-11

### Changed:

- Docker build pointing to Java 11.


## [3.11.0] - 2021-10-07

### Changed:

- Changed ArrayList for input parameters to List.
- Moving from Google Sender to built in HTTP Sender.
- Source field added to US Autocomplete Pro lookup.
- Moved to Java 11 to support HTTP Client. This is a breaking change for anyone using earlier versions of Java.


## [3.10.7] - 2021-08-20

### Changed:

- Removed Autocomplete Basic example.


## [3.10.6] - 2021-08-10

### Changed:

- Fixes to test environment.


## [3.10.5] - 2021-08-10

### Changed:

- Eliminating deprecated java library method.


## [3.10.4] - 2021-08-10

### Changed:

- Match being set properly on the query.


## [3.10.1] - [3.10.3] - 2021-08-06

### Changed:

- Resolving issues with publishing to Maven.


## [3.10.0] - 2021-07-14

### Changed:

- New match strategy "enhanced".


## [3.9.1] - 2021-07-06

### Changed: 

- Removed match_mode, renamed match_details to enhanced_match.


## [3.9.0] - 2021-06-11

### Changed:

- Updated README
- License field descriptions in the examples.
- US Street enhanced matching integration fields in Analysis.


## [3.8.1] - 2021-05-29

### Changed:

- Fixed complication with jackson deserialization.
- Jeffrey fixed some comments.


## [3.8.0] - 2021-03-12

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`


## [3.7.2] - 2020-11-19

### Changed:

- Latest dependencies.


## [3.7.1] - 2020-11-19

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [3.7.0] - 2020-09-17

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [3.6.1] - 2020-08-31

### Changed:

- License array must be instantiated.


## [3.6.0] - 2020-08-25

### Changed:

- User can now specify the license to be used.


## [3.5.2] - 2020-06-19

### Changed:

- Set key for input_id field.


## [3.5.1] - 2019-12-03

### Changed:

- Updated code examples.


## [3.5.0] - 2019-11-22

### Changed:

- Now implementing US-Autocomplete-Pro API.


## [3.4.1] - 2019-11-12

### Changed:

- Updates to pom.xml.
- Input ID returned with the result.


## [3.3.8] - 2019-04-05

### Changed:

- Additional changes field in International Street Analysis (Rootlevel added).
- Input fields populated in examples.


## [3.3.7] - 2019-02-26

### Changed:

- Moved Changelog to separate repo.
- Moved EWS Match to correct field.


## [3.3.6] - 2019-01-14

### Changed:

- No longer publishing anadorned `.jar` file.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-java-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-java-sdk/compare/3.3.6...HEAD
[3.3.6]: https://github.com/smartystreets/smartystreets-java-sdk/compare/3.3.5...3.3.6
[Earlier]: https://github.com/smartystreets/smartystreets-java-sdk/releases
