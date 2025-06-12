# Changelog - [US Reverse Geocoding API](https://www.smarty.com/docs/cloud/us-reverse-geo-api)

All notable changes to the US Reverse Geocoding API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.24.14 - 2025-06-12
We are beginning our phased rollout of us-reverse-geo-api 0.24.14. This process is scheduled to be completed by 2025-06-13 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### Changed:
- The addition of smarty_key in the result.
- The data includes the latest updates from all upstream packages and providers.


## 0.24.13 - 2025-05-22
We are beginning our phased rollout of us-reverse-geo-api 0.24.13. This process is scheduled to be completed by 2025-05-23 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### Changed:

- Latest upstream data.


## 0.24.4 - 2023-06-27

### Changed:

- Added "source" input and output fields to return non-postal addresses.
- The street and city fields are now cased correctly.


## 0.24.3 - 2023-06-23

- Fixed an issue where the directionals were not being returned in the address components.

## 0.23.3 - 2023-02-20

- Small internal changes regarding plans and subscriptions.
- Compiled using Go v1.19.5.


## 0.23.1 - 2022-12-13

- Fix issue with lowercase state abbreviations.


## 0.22.0 - 2022-10-12

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.
- Compiled using Go v1.19.2.


## 0.19.0 - 2021-02-10

CHANGES:

- Latest internal dependencies.
- Updated mechanism for counting lookups.


## 0.18.1 - 2021-02-03

CHANGES:

- Compiled using Go v1.15.x.
- Removed deprecated fields from 0.15.0 changes.
- Latest internal dependencies.


## 0.15.0 - 2020-09-09

CHANGES:

- Renamed result field from `license` to `coordinate_license` to better distinguish between upstream data provider licensing restrictions
  as compared to Smarty licensing relative to subscriptions.
- Added `accuracy` field to properly indicate the level of accuracy of a particular geographic coordinate.
- As a result of the `accuracy` field addition, the data file structural changes. All previous versions of the data field will not properly
  return either the `coordinate_license` or `accuracy` fields when using an older data set.


## 0.14.1 - 2020-09-01

CHANGES:

- Internal structural changes.


## 0.14.0 - 2020-09-01

CHANGES:

- BREAKING CHANGE: JSON output field `state` has been renamed to `state_abbreviation`.


## 0.13.8 - 2020-08-08

CHANGES:

- Internal performance optimizations.


## 0.13.7 - 2020-08-07

CHANGES:

- First public (beta) release.


## 0.9.15 - 2019-12-20

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence. 


## 0.9.6 - 2019-09-25


CHANGES:

- Initial Beta Release
