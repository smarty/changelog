# [Go SDK](https://smartystreets.com/docs/sdk/go)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [v1.10.0] - 2021-03-23

### Changed:

- Defined new fields for us-street-api analysis object: `dpv_no_stat`
- Functionality added to handle the US Autocomplete Pro API.


## [v1.9.0] - 2021-02-19

## Changed;

- Defined new fields for us-street-api analysis object: `dpv_no_stat`


## [v1.8.1] - 2020-09-28

## Changed:

- Fixes to makefile for publishing new versions.


## [v1.8.0] - 2020-09-17

### Changed:

- Functionality added to handle the new US Reverse Geocoding API.


## [v1.6.3] - 2020-08-28

### Changed:

- Retry client now employs exponential backoff strategy complete with 'jitter'. (Fixes [Issue #17](https://github.com/smartystreets/smartystreets-go-sdk/issues/17) via [PR #18](https://github.com/smartystreets/smartystreets-go-sdk/pull/18))



## [v1.6.2] - 2020-08-25

### Bug Fixes:

- Incorporate the path of supplied `WithBaseURL` value into the http request. This allows the client to send requests to locally hosted APIs that reside behind a non-blank path. From the most recent version of the godocs:

> The address provided will be consulted for scheme, host, and path values. Any other URL components such as the query string or fragment will be ignored.


## [v1.6.1] - 2020-08-14

### Bug Fixes:

- Filter out blank values passed to `WithLicenses` function option.


## [v1.6.0] - 2020-08-13

### Changed:

- Introduced a new function option for wireup: `WithLicenses`. This option is useful when targeting specific capabilities of an API based on the subscription level. See the documentation for possible values. Most callers need not supply this flag.


## [v1.5.1] - 2020-07-30

### Changed:

- Incremented version.


## [v1.5.0] - 2020-07-30

### Changed:

- WithContext option now available for all clients.


## [v1.4.3] - 2020-06-12

### Changed:

- Latest dependencies and build instructions.


## [v1.4.2] - 2020-04-30

### Changed:

- Version is not incrementing properly.


## [v1.4.1] - 2020-04-30

### Changed:

- Incremented version.


## [v1.4.0] - 2020-04-29

### Changed:

- Option to allow caller to pass in their own http.Client.


## [v1.3.5] - 2020-03-16

### Changed:

- Latest internal testing dependencies.


## [v1.3.4] - 2019-11-26

### Changed:

- Revising build process


## [v1.3.3] - 2019-11-25

### Changed:

- Incremented version


## [v1.3.2] - 2019-11-25

### Changed:

- Comment added to clarify match strategy


## [v1.3.1] - 2019-11-25

### Changed:

- Incremented version.


## [v1.3.0] - 2019-11-25

### Changed:

- Updated tests.


## [v1.2.1] - 2019-09-25

### Changed:

- Incremented version.


## [v1.2.0] - 2019-09-25

### Changed:

- Input ID added to result in examples.


## [v1.1.0] - 2019-06-13

### Changed:

- New client builder option for disabling http2.


## [v1.0.0] - 2019-06-03

### Changed:

- Populated relevant input fields in examples.
- Moved to GoMods.
- Fixed lack of parameters in Zip query.
- Additional wireup option for website key in client builder.


## [8.3.0] - 2019-03-13

### Changed:

- Moved changelog.
- Introduced changes struct to International Street API, added RootLevel to accomodate.


## [8.2.1] - 2019-02-26

### Changed:

- Match strategy added to examples, set to invalid.
- Altered log message when running 'make publish'.


## [8.2.0] - 2019-02-07

### Changed:

- Tests for json response deserialization.
- ews_match moved from analysis to metadata.

## [8.1.6] - 2018-09-26

### Changed:

- Now running `make` targets on the host environment.

## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-go-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-go-sdk/compare/8.1.6...HEAD
[8.1.6]: https://github.com/smartystreets/smartystreets-go-sdk/compare/8.1.5...8.1.6
[Earlier]: https://github.com/smartystreets/smartystreets-go-sdk/releases
