# Changelog - [US Enrichment API](https://www.smarty.com/docs/cloud/us-enrichment-api)

All notable changes to the US Enrichment API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 1.3.6 - 2025-06-09

CHANGES:
- June data release of Property and Secondary data


## 1.3.6 - 2025-06-05

CHANGES:
- June data release of GeoReference data
- Normal code maintenance.


## 1.2.38 - 2025-04-07

CHANGES:
- April data release
- Normal code maintenance.


## 1.2.36 - 2025-02-27

CHANGES:
- Resolved spurious 500 errors when performing an address search.


## 1.2.33 - 2025-01-07

CHANGES:
- Normal code maintenance.


## 1.2.31 - 2024-12-12

CHANGES:
- Introducing geo-reference vintage census data subsets.
  - Get current census data: geo-reference
  - Get 2010 census data:    geo-reference/2010
  - Get 2020 census data:    geo-reference/2020
  - A new output field has been added to show the census version date:
    - Example: "data_set_version": "census-2024"


## 1.2.11 - 2024-10-09

CHANGES:
- Normal code maintenance.


## 1.2.10 - 2024-09-27

CHANGES:
- Fixed an issue where getting secondary counts would use more than one lookup.


## 1.2.4 - 2024-09-09

CHANGES:
- Normal code maintenance.


## 1.2.1 - 2024-09-03

CHANGES:
- Added an internal feature that allows filtering of sensitive data.


## 1.2.0 - 2024-08-17

CHANGES:
- Added ability to perform queries by address in addition to SmartyKey. The capability requires a specific subscription.


## 1.1.6 - 2024-08-13

CHANGES:
- Code maintenance that does not affect results.


## 1.1.1 - 2024-05-14

CHANGES:
- Prepare for a new dataset to be launched soon.


## 1.0.29 - 2024-03-13

CHANGES:
- Fixed casing where letters follow numbers in the same word.
- Updated data. See: us-enrichment-data.md


## 1.0.27 - 2024-02-20

CHANGES:
- Added new GeoReference data set.
- Updated data. See: us-enrichment-data.md


## 1.0.25 - 2024-01-26

CHANGES:
- Added the ETag feature that allows you to query with the previous ETag value (returned with each query) to see if any data in the record was updated. If an ETag value is provided and the data has not been updated, you are not charged for the lookup. See the documentation for details.
- Updated data.


## 1.0.14 - 2024-01-11

CHANGES:
- Added a feature that allows attribute groups to be used to narrow the list of returned attributes. The documentation for this feature will be released Mon Jan 15.


## 1.0.8 - 2023-11-3

CHANGES:
- Added field "document_type_description" to help clarify financial data.
- Better standardized casing for many fields.
- Updated a few fields for clarity.

## 1.0.4 - 2023-10-25

CHANGES:
- Hide zero value fields when not providing value.
- Updated a few fields for clarity.

BUG FIXES:
- Fixed an issue where a few fields were not populating data.

## 1.0.1 - 2023-09-29
- Initial release of API
- Property Data with Principal and Financial data.
