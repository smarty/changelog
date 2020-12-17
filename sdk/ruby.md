# [Ruby SDK](https://smartystreets.com/docs/sdk/ruby)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [5.9.2] - 2020-11-30

### Changed:

- Checking if candidates are nil before iterating in International Street Client.


## [5.9.1] - 2020-11-23

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [5.9.0] - 2020-10-29

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [5.8.0] - 2020-08-25

### Changed:

- User can now specify the license to be used.


## [5.7.1] - 2019-11-25

### Changed:

- Comment added to clarify match strategy.


## [5.7.0] - 2019-03-13

### Changed:

- Added Changes structure to InternationalStreet Analysis, created Rootlevel structure to accomodate.


## [5.6.2] - 2019-03-04

### Changed:

- Revert "Renamed log method for fake logging."


## [5.6.1] - 2019-02-28

### Changed:

- Match strategy added to examples.
- Moved changelog.


## [5.6.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)
- Using `warn` instead of `log` to avoid conflict with builtin function.


## [5.5.4] - 2018-09-18

### Changed:

- Standardized `Makefile`.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-ruby-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.4...HEAD
[5.5.4]: https://github.com/smartystreets/smartystreets-ruby-sdk/compare/5.5.3...5.5.4
[Earlier]: https://github.com/smartystreets/smartystreets-ruby-sdk/releases
