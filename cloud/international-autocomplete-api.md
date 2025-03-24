# Changelog - [International Autocomplete Address API](https://www.smarty.com/docs/cloud/international-address-autocomplete-api)

All notable changes to the International Autocomplete API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 2.2.4 - 2025-03-24
CHANGES:

- Improved NLD (Netherlands) results.


## 2.2.2 - 2025-03-10
CHANGES:

- Improved NLD (Netherlands) searching and results.


## 2.2.1 - 2025-02-27
CHANGES:

- Improved result sorting.
- Added geolocation feature to prefer results by ip address.
- Added max_group_results to limit the number of results from group expansion.


## 2.2.0 - 2025-02-13
CHANGES:

- Improved NLD (Netherlands) searching and results.


## 2.1.7 - 2024-11-12
CHANGES:

- Internal bug fixes that do not affect user results.


## 2.1.6 - 2024-11-07
CHANGES:

- Internal bug fixes that do not affect user results.


## 2.1.3 - 2024-11-06
CHANGES:

- Internal bug fixes that do not affect user results.


## 2.1.0 - 2024-07-02
CHANGES:

- Added two new fields to represent the long and short administrative area names.
  - administrative_area_short
  - administrative_area_long
- This deployment will last 3 days.

## 2.0.0 - 2024-06-28
CHANGES:

- Removed support for the original API URL. Only v2 calls are now supported.  


## 1.0.27 - 2024-05-20
CHANGES:

- Results are sorted (deployed over the next two days). 


## 1.0.22 - 2024-04-09
CHANGES:

- Internal code changes that will not affect results. 


## 1.0.20 - 2024-03-20
CHANGES:

- Removed support for Kosovo. 

## 1.0.18 - 2024-03-08
CHANGES:

- Restored support for Portugal. 

## 1.0.17 - 2024-02-20
CHANGES:

- Added support for Kosovo.
- Fixed issue where an extra hyphen appeared in some address text results. 

## 1.0.16 - 2024-01-29

CHANGES:

- Internal licensing changes that will not affect results.


## 1.0.14 - 2024-01-08

CHANGES:

- Completed preparations for the planned outage of v1 on Jan 16th.  See https://get.smarty.com/international-autocomplete-api-v2-migration.


## 1.0.13 - 2024-01-03

CHANGES:

- Fixed issue where some v2 customers would not be charged for evaluation lookups.


## 1.0.12 - 2023-12-18

CHANGES:

- Fixed issue where the address ID from a summary result that contains 1 entry, would not return a detailed result.


## 1.0.11 - 2023-12-13

CHANGES:

- Updated max_results when using Address IDs to return additional subunits.

## 1.0.10 - 2023-11-20

CHANGES:

- Fixed some internal issues that should not affect results.


## 1.0.7 - 2023-10-31

CHANGES:

- Initial public release for International Autocomplete v2.


## 1.0.4 - 2023-10-24

CHANGES:

- Internal modifications that does not affect functionality.


## 1.0.3 - 2023-10-20

CHANGES:

- Internal modifications that does not affect functionality.


## 1.0.2 - 2023-10-16

CHANGES:

- No modifications to the current functionality.
- Added the new v2 of the API which will be available shortly.


## 0.9.10 - 2023-10-12

CHANGES:

- Internal modifications in preparation for a major update. Should not affect current operations.


## 0.9.4 - 2023-02-16

CHANGES:

- Data update.


## 0.9.4 - 2023-01-10

CHANGES:

- Data update.
- No longer return NLD addresses with incomplete postal codes.


## 0.9.2 - 2022-11-18

CHANGES:

- Fixed data issue where CAN queries less than 4 chars in length would return no results.


## 0.9.2 - 2022-11-15

CHANGES:

- Added countries to the super administrative areas list [AZE,PRT,RUS]
- Compiled with Go 1.19.3
- Fixed an issue where specific user input could cause a panic.
- Updated all data.

## 0.8.17 - 2022-09-29

CHANGES:

- Resolve an issue with invalid result removal.
- Do not return CAN results with an incomplete Postal Code.
- Fixed intermittent issue where no results are returned.


## 0.8.14 - 2022-09-20

CHANGES:

- Handle countries that use sub administrative areas such as BGR. In these cases, administrative area would not be populated.
- Handle countries that use super administrative areas such as [BEL,BOL,ESP,FRA,HKG,ITA,LIE,LUX,MDG,MDV,PAK,PHL,SRB,TUN]


## 0.8.13 - 2022-08-31

CHANGES:

- Filter IRL results with incomplete postal codes.


## 0.8.12 - 2022-08-30

CHANGES:

- Fix casing of cardinal directions in street field.
- Fix postal code issue that could return an IRL postal code for a non-IRL country.
- Filter results with incomplete postal codes for IRL.


## 0.8.9 - 2022-07-29

CHANGES:

- Fixed postal code formatting for several countries. [CZE, GRC, SVK, SWE, LVA, POL]
- Fixed incomplete postal code issues for IRL.


## 0.8.8 - 2022-07-28

CHANGES:

- Fixed inconsistent casing issues.


## 0.8.6 - 2022-07-26

CHANGES:

- Removed the entries field from the response as it is a future feature that is not yet supported by the SDKs.


## 0.8.5 - 2022-07-19

CHANGES:

- Updated the supported countries list. Added back KOR which was accidentally removed.
- Added distance parameter for use with geolocation services.


## 0.8.4 - 2022-07-19

CHANGES:

- Use a postal extension field when available; affect NLD and others.


## 0.8.2 - 2022-07-14

CHANGES:

- Improvements on how PO BOX address formatting.
- Improved lookups for PO BOX addresses in CAN and GBR.
- Added ability to bias results based on location, geolocation and proximity.

## 0.8.0 - 2022-07-07

CHANGES:

- Updated data for improved results.
- Several improvements to CAN and GBR searching:
  - Only return results with full Postal Codes
  - Allow entry of units that would previously cause no results to be returned.
    - (Units are not returned but is planned for a future release).

## 0.3.0 - 2021-09-27

CHANGES:

- Initial release.

