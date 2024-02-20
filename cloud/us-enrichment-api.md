# Changelog - [US Enrichment API](https://www.smarty.com/docs/cloud/us-enrichment-api)

All notable changes to the US Enrichment API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
