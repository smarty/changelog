# Changelog - [US ZIP Code API](https://www.smarty.com/docs/cloud/us-zipcode-api)

All notable changes to the US ZIP Code API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 5.12.14 - 2023-10-11

### Added

- Added error response for unsupported XML content-type.

### Changes

- Increased idle client connection timeout.

### Fixed

- Improved json decoding process to stop the sporadic failing of valid requests caused from a previous malformed request.

## 5.12.7 - 2023-03-21

- Support expansion of abbreviations to improve hit rates. e.g. St=Saint, Ft=Fort, N=North, etc.


## 5.12.2 - 2023-03-21

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.
- Compiled using Go v1.19.7.

## 5.11.4 - 2022-10-12

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.
- Compiled using Go v1.19.2.

## 5.10.2 - 2022-06-06

CHANGES:

- Compiled using Go v1.18.3.
- Upgrade to latest dependencies.

BUG FIXES:

- Local install no longer gives startup error if `config.json` is not present.

## 5.10.0 - 2022-05-31

CHANGES:

- Reduce memory requirements.
- Upgrade to latest dependencies.

## 5.9.14 - 2022-05-19

CHANGES:

- Updated internal memory management.
- For local installations, updated CLI flag descriptions.

## 5.9.12 - 2022-04-01

CHANGES:

- Compiled using Go v1.17.8.
- Internal restructuring of small bits of code.
- Allowing config file location to be specified using a CLI flag.

## 5.9.6 - 2022-03-02

CHANGES:

- Compiled using Go v1.17.7.
- Recognizing alternate spelling of state abbreviations

## 5.9.2 - 2022-02-21

CHANGES:

- Compiled using Go v1.17.7.
- Overhauled internals of the engine and how it processes lookup.
- Maintains CLI argument compatibility for local installations.

## 5.5.2 - 2020-11-25

CHANGES:

- Updated internal performance monitoring for cloud release.

## 5.5.1 - 2020-11-25

CHANGES:

- Updated internal performance monitoring for cloud release.

## 5.5.0 - 2020-11-24

CHANGES:

- Updated internal performance monitoring for cloud release.


## 5.4.0 - 2020-06-24

CHANGES:

- Upgrade to latest dependencies which allowed removal of various internal dependencies.
- Compiled using Go v1.15.x.
- Using latest internal (v2) geocoding library.


## 5.3.0 - 2020-06-24

CHANGES:

- Upgrade to latest dependencies which allowed removal of various internal dependencies.


## 5.2.2 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.
- Compiled using Go v1.14.x.


## 5.2.1 - 2020-05-05

CHANGES:

- Internal behavior surrounding subscription management.


## 5.2.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 5.1.14 - 2020-03-16

CHANGES:

- Latest internal dependencies.

## 5.1.13 - 2019-12-20

CHANGES:

- Internal refactoring 


## 5.1.12 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.


## 5.1.8 - 2019-11-02

CHANGES:

- Latest version of internal dependencies.


## 5.1.7 - 2019-10-22

CHANGES:

- Latest version of internal dependencies.


## 5.1.6 - 2019-09-06

CHANGES:

- Latest version of internal dependencies.


## 5.1.5 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 5.1.0 - 2019-05-29

CHANGES:

- Local installation users now benefit from the same middleware handlers as cloud installation users as far as preparing the request for handling (rejecting any GET requests with payload).
- There is now a new endpoint at `/version`. A GET request to this endpoint will result in HTTP 200 and a `text/plain` repsonse body containing software version information. The syntax/contract of the body is documented within itself.


## 5.0.0 - 2019-05-23

CHANGES:

- Restructured and consolidated all code for running the US ZIP Code API in the Smarty cloud or as a local installation. As such, this changelog (moving forward) will contain changes that apply to both isntallations.
- CORS headers will no longer be provided to responses served by local installations. This is now the responsibility of organizations running their own local installation. There is no change to CORS header handling for users of the Smarty cloud installation (https://us-zipcode.api.smartystreets.com).


## 4.1.3 - 2019-04-08

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 4.0.4 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 4.0.3 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 4.0.2 - 2019-03-08

CHANGES:
- Internal refactoring.


## 4.0.1 - 2019-03-06

IMPROVEMENTS:

- Overhauling module and deployment system. (No public-facing changes expected.)
- Updated internal dependencies.
- Compiled using Go v1.12.


## 4.0.0 - 2018-12-26

IMPROVEMENTS:

- ZIP Code inputs that consist only of zeros are now discarded as if they were blank, but only if supplied along with non-blank City and State input values.
