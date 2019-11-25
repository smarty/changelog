# [Ruby SDK](https://smartystreets.com/docs/sdk/ruby)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


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
