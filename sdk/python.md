# [Python SDK](https://smartystreets.com/docs/sdk/python)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [4.8.4] - 2021-06-11

### Changed:

- US Street V2 integration fields in Analysis.
- Makefile updates for latest python version.


## [4.8.3] - 2021-05-26

### Changed:

- Fixes to the way licenses are handled.


## [4.8.2] - 2021-05-26

### Changed:

- License field descriptions in the examples.
- More output fields in us-street examples.


## [4.8.1] - 2021-05-25

### Changed:

- Autocomplete Pro added to setup.
- Using key instead of auth-id for embedded (website) key authentication.


## [4.8.0] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [4.7.3] - 2021-02-24

### Changed:

- dpv_no_stat field added on the response.


## [4.7.2] - 2020-11-20

### Changed:

- License parameter is decoded from the US Reverse Geocoding API response.


## [4.7.1] - 2020-10-30

### Changed:

- Updates to setup file, making US Reverse Geo visible.


## [4.7.0] - 2020-10-30

### Changed:

- Update to examples to accurately represent match field accepted inputs.
- Functionality added to handle the new US Reverse Geocoding API.


## [4.6.1] - 2020-08-21

### Changed:

- Fixed broken tests surrounding mandatory population of street field.


## [4.6.0] - 2020-08-21

### Changed:

- Street field needs to be populated.
- User can now specify the license to be used.


## [4.5.0] - 2020-04-03

### Changed:

- Support configuring CA bundle & proxy via env vars. 


## [4.4.1] - 2020-02-26

### Changed:

- Fixed bug that made the autocomplete client crash if there are no suggestions in the response.

## [4.4.0] - 2019-11-25

### Changed:

- Return input id with result.
- Comment added to clarify match strategy.


## [4.3.0] - 2019-06-05

### Changed:

- Populated relevant input fields in examples.
- New custom header option available in client builder.


## [4.2.0] - 2019-03-13

### Changed:

- Moved changelog.
- Changes structure added to analysis in international street API. Rootlevel created to accomodate.


## [4.1.0] - 2019-02-25

### Changed:

- Introduced the `ews_field` to the `metadata` section of the US Street API response.
- Deprecated the `ews_field` on `analysis` section of US Street API response. (The `ews_match` field has never been part of the analysis section.)


## [4.0.1] - 2019-01-14

### Changed:

- Re-introduced dependency on twine for uploading new releases to PyPI.

## [4.0.0] - 2019-01-14

### Changed:

- Moved `__version__` variable to its own module to remove installation dependency on `requests` module.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-python-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.1...HEAD
[4.0.1]: https://github.com/smartystreets/smartystreets-python-sdk/compare/4.0.0...4.0.1
[4.0.0]: https://github.com/smartystreets/smartystreets-python-sdk/compare/3.3.2...4.0.0
[Earlier]: https://github.com/smartystreets/smartystreets-python-sdk/releases
