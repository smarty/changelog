# Changelog - [US Autocomplete Pro API](https://www.smarty.com/docs/cloud/us-autocomplete-api#pro)

All notable changes to the US Autocomplete Pro API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 1.12.5 - 2024-05-28

- Removes long deprecated JSONP support.
- Internal code changes that should not affect results.


## 1.12.0 - 2024-02-28

- Internal changes that should not affect results.


## 1.11.2 - 2023-07-10

- Internal changes that should not affect results.


## 1.11.0 - 2023-06-21

- Casing streets and cities is now similar to US Street API.


## 1.10.10 - 2023-04-28

- Deployed new data to fix issues with some secondaries not being grouped together under their parent address.


## 1.9.9 - 2022-10-12

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.


## 1.9.8 - 2022-10-11

CHANGES:
- Added secondary data to Autocomplete Basic results.


## 1.9.6 - 2022-10-07

CHANGES:
- Compiled against Go 1.19.2
- Eliminate duplicate candidates in the Autocomplete Basic results.


## 1.9.5 - 2022-10-04

CHANGES:
- Compiled against Go 1.19.1
- Internal changes that will not affect the user experience.


## 1.9.4 - 2022-09-22

CHANGES:
- When using preferences, an unmatched search term was sometimes returning results.


## 1.9.3 - 2022-09-15

CHANGES:
- Internal changes that do not affect the user experience.


## 1.9.1 - 2022-08-08

CHANGES:
- Internal changes that do not affect the user experience.


## 1.9.0 - 2022-07-05

CHANGES:
- Fixed issue where the source field would not be returned for postal addresses even when source is specified in the input.
- Fixed issue where some addresses with alternate cities would not be returned.


## 1.7.4 - 2022-03-18

CHANGES:
- Code refactor to increase performance and maintainability.


## 1.6.10 - 2022-03-08

CHANGES:
- Fixed issues with standalone secondary designators or secondary values. The secondary value would include a backticked city name.


## 1.6.9 - 2022-01-21

CHANGES:
- Fixed issue where if HEIGHTS were spelled out instead of HTS, it would eliminate all HTS addresses from the result set.


## 1.6.6 - 2021-09-03

CHANGES:
- Added back non-postal addresses with a parameter to include them in the results. By default non-postals are not returned. See documentation for the "source" parameter.


## 1.6.2 - 2021-08-18

CHANGES:
- Removed non-postals from the data as per customer feedback.


## 1.6.1 - 2021-08-03

CHANGES:
- Added 15+ million non-postal addresses to the data. 
  When these addresses are validated using us-street-api, the analysis section will look similar to:
  "analysis": {
      "dpv_footnotes": "A1",
      "active": "Y",
      "footnotes": "F#",
      "enhanced_match": "non-postal-match"
  }


## 1.5.5 - 2021-06-10

CHANGES:
- Fixed issue where excluded states or territories could not be excluded from results.


## 1.5.3 - 2021-02-16

CHANGES:
- Fixed issue when a dot is entered following a secondary designator (e.g. APT.) which resulted in no results.
- Fixed issue with over 30 ZIPCodes in the filter. List is now limited to 100. 


## 1.5.2 - 2021-02-10

CHANGES:
- Fixed issue when searching addresses that contain dots.


## 1.4.2 - 2020-11-20

CHANGES:
- Compiled using Go v1.15.x.
- New, local-install version now available for download.


## 1.3.18 - 2020-10-14

CHANGES:

- Fixed issue that abnormally terminated a user request with specific input


## 1.3.17 - 2020-09-15

CHANGES:

- Changed default for prefer_ratio to 100.


## 1.3.14 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.
- Compiled using Go v1.14.x.


## 1.3.13 - 2020-03-16

CHANGES:

- Latest internal dependencies.

## 1.3.11 - 2020-02-10

CHANGES:

-  Fixed issue that was preventing the use of the CONTIGUOUS and ALLSTATES keywords in include_only_states. 

## 1.3.10 - 2020-01-31

CHANGES:

- Fixed a display and data issue when addresses do not have a secondary designator but yet have a secondary value. 


## 1.3.9 - 2020-01-03

CHANGES:

- When using the _zip_codes parameters, the prefer_geolocation parameter will default to none. Before this change, it needed to be set to none explicitly.
- Clarified error messages related to this change.
- Updated the documentation. 


## 1.3.8 - 2019-12-20

CHANGES:

- Internal refactoring 


## 1.3.7 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.

## 1.3.6 - 2019-12-30

CHANGES:

- Added more street suffix aliases with misspellings for greater tolerance
- Added building default addresses back into the data

## 1.3.5 - 2019-11-05

CHANGES:

- Fixed issue when using 'selected' and in results Apt could return as Bpt.
- Fixed panic in specific search scenarios.

## 1.3.4 - 2019-11-04

CHANGES:

- Added support for secondaries that contain spaces
- Fixed many issues related to features delivered in 1.2.0 and 1.2.2.
- Returns 5 digit ZIP Codes in the suggestions

## 1.2.2 - 2019-10-10

CHANGES:

- Added additional fuzziness that will try ignoring secondary data in the `search` parameter.
  This allows the user to type secondary data and still get results when no such data is actually in the address.

## 1.2.1 - 2019-10-3

CHANGES:

- When using the `selected` parameter and the user has subsequently typed part of the secondary value,
  it now returns the limited list of secondaries that match what has been typed thus far.
- Fixed an issue with the `selected` parameter to handle partial secondary values.

## 1.2.0 - 2019-09-19

CHANGES:

- Implemented a new parameter named `selected` that is used to return up to 100 secondaries for an address.

## 1.1.21 - 2019-09-06

CHANGES:

- The response body for `HTTP 4xx` responses is now formatted more like other Smarty APIs. This response is not to be parsed and may change at any time.
- The wording and formatting of line items in the diagnostic response just mentioned have been reworked.
- Previously, a blank input `search` value resulted in `HTTP 200` and a response body containing `{"suggestions":null}` whereas it will now result in `HTTP 422` (unprocessable entity) with a diagnostic report in the response body.
- Latest internal dependencies

## 1.1.20 - 2019-08-22

CHANGES:

- Fixed the very last issues with expanding secondaries that we will ever encounter in our lifetimes.

## 1.1.19 - 2019-08-21

CHANGES:

- Fixed more issues with expanding secondaries.

## 1.1.18 - 2019-08-21

CHANGES:

- Fixed issues with expanding secondaries.


## 1.1.17 - 2019-08-19

CHANGES:

- Changed default for the prefer_geolocation parameter from 'none' to 'city'.


## 1.1.16 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 1.1.15 - 2019-08-15

CHANGES:

- In the case of HTTP 422 response the error message presents much like an unordered markdown listing with each entry/error on its own line.


## 1.1.14 - 2019-08-13

CHANGES:

- Invalid `prefer_ratio` value no longer trips other unrelated error messages.
- Error message for `max_results` corrected.
- Moved some sanitization logic closer to the core of the application.
- Implemented handling of limited variations of `PO Box`.


## 1.1.13 - 2019-08-06

CHANGES:

- Names of input fields starting with `include_` now start with `include_only_`. (While normally a breaking change requiring the major version to be incremented, we are currently in private beta and opted against that course of action.)


## 1.1.12 - 2019-08-05

CHANGES:

- Better sanitization/trimming of `search` value.


## 1.1.11 - 2019-08-05

CHANGES:

- Near complete reworking of the input fields.


## 1.1.10 - 2019-07-17

CHANGES:

- Removed a few fields from the output.


## 1.1.9   2019-07-09

- Pre-release version


## 1.1.8 - 2019-06-28

- Pre-release version


## 1.1.7 - 2019-06-28

- Pre-release version


## 1.1.6 - 2019-06-28

- Pre-release version


## 1.1.5 - 2019-06-26

- Pre-release version


## 1.1.4 - 2019-06-25

- Pre-release version


## 1.1.3 - 2019-06-14

- Pre-release version


## 1.1.2 - 2019-06-10

- Pre-release version


## 1.1.1 - 2019-06-10

- Pre-release version


## 1.1.0 - 2019-06-10

- Pre-release version


## 1.0.18 - 2019-05-20

- Pre-release version


## 1.0.17 - 2019-05-20

- Pre-release version


## 1.0.16 - 2019-05-17

- Pre-release version


## 1.0.15 - 2019-05-17

- Pre-release version


## 1.0.14 - 2019-05-17

- Pre-release version


## 1.0.13 - 2019-05-17

- Pre-release version


## 1.0.12 - 2019-05-16

- Pre-release version


## 1.0.11 - 2019-05-16

- Pre-release version


## 1.0.10 - 2019-04-25

- Pre-release version


## 1.0.9 - 2019-04-25

- Pre-release version


## 1.0.8 - 2019-04-23

- Pre-release version


## 1.0.7 - 2019-04-23

- Pre-release version


## 1.0.6 - 2019-04-23

- Pre-release version


## 1.0.5 - 2019-04-12

- Pre-release version


## 1.0.4 - 2019-04-12

- Pre-release version


## 1.0.3 - 2019-04-10

- Pre-release version


## 1.0.2 - 2019-04-10

- Pre-release version


## 1.0.1 - 2019-04-09

- Pre-release version


## 1.0.0 - 2019-04-09


