# [.Net SDK](https://smartystreets.com/docs/sdk/dotnet)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [8.4.0] - 2019-12-03

### Changed:

- Added custom header sender.

## [8.3.1] - 2019-11-25

### Changed:

- Fixed syntax error in international street example.
- Comment added to clarify match strategy.


## [8.3.0] - 2019-09-25

### Changed:

- Populated relevant input fields in examples.
- Added notes for readability.
- US Street example (.vb) updated to work with library.
- Made USStreetSingleAddressExample.vb compile.
- 'inputID' added to the response.


## [8.2.0] - 2019-03-13

### Changed:

- Added Match Strategy to examples.
- Moved changelog.
- 'changes' field added to International Street Analysis, Rootlevel created to assist.


## [8.1.1] - 2019-02-26

### Changed:

- Made Analysis compile.


## [8.1.0] - 2019-02-26

### Changed:

- Update integration test to check environment variables to enable alternative API URLs (`SMARTY_URL_INTERNATIONAL_STREET`, `SMARTY_URL_US_AUTOCOMPLETE`, `SMARTY_URL_US_EXTRACT`, `SMARTY_URL_US_STREET`, `SMARTY_URL_US_ZIP`).
- Deprecated Analysis.IsEWS_Match


## [8.0.15] - 2019-01-15

### Changed:

- By default add `Accept-Encoding: gzip` header to request and handle gzipped response.


## [8.0.14] - 2018-09-18

### Changed:

- Settled on approach to leveraging docker to develop and publish.


## [Earlier]

For details on earlier changes, please see the [releases listing](https://github.com/smartystreets/smartystreets-dotnet-sdk/releases).

------------

[Unreleased]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...HEAD
[8.0.15]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.14...8.0.15
[8.0.14]: https://github.com/smartystreets/smartystreets-dotnet-sdk/compare/8.0.13...8.0.14
[Earlier]: https://github.com/smartystreets/smartystreets-dotnet-sdk/releases
