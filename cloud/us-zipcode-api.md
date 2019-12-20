# Changelog - [US ZIP Code API](https://smartystreets.com/docs/cloud/us-zipcode-api)

All notable changes to the US ZIP Code API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## UNRELEASED


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

- Restructured and consolidated all code for running the US ZIP Code API in the SmartyStreets cloud or as a local installation. As such, this changelog (moving forward) will contain changes that apply to both isntallations.
- CORS headers will no longer be provided to responses served by local installations. This is now the responsibility of organizations running their own local installation. There is no change to CORS header handling for users of the SmartyStreets cloud installation (https://us-zipcode.api.smartystreets.com).


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
