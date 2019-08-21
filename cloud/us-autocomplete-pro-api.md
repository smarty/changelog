# Changelog - [US Autocomplete Pro API](https://smartystreets.com/docs/cloud/us-autocomplete-api#pro)

All notable changes to the US Autocomplete Pro API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## UNRELEASED


## 1.1.18 2019-08-21

CHANGES:

- Fixed issue with expanding secondaries.


## 1.1.17 2019-08-19

CHANGES:

- Changed default for the prefer_geolocation parameter from 'none' to 'city'.


## 1.1.16 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 1.1.15 - 2019-08-15

CHANGES:

- In the case of HTTP 422 response the error message presents much like an unordered markdown listing with each entry/error on its own line.


## 1.1.14 - 2019-08-13

CHANGES:

- Invalid `prefer_ratio` value no longer trips other unrelated error messages.
- Error message for `max_results` corrected.
- Moved some sanitization logic closer to the core of the application.
- Implemented handling of limited variations of `PO Box`.


## 1.1.13 - 2019-08-06

CHANGES:

- Names of input fields starting with `include_` now start with `include_only_`. (While normally a breaking change requiring the major version to be incremented, we are currently in private beta and opted against that course of action.)


## 1.1.12 - 2019-08-05

CHANGES:

- Better sanitization/trimming of `search` value.


## 1.1.11 - 2019-08-05

CHANGES:

- Near complete reworking of the input fields.


## 1.1.10 - 2019-07-17

CHANGES:

- Removed a few fields from the output.


## 1.1.9   2019-07-09

- Pre-release version


## 1.1.8 - 2019-06-28

- Pre-release version


## 1.1.7 - 2019-06-28

- Pre-release version


## 1.1.6 - 2019-06-28

- Pre-release version


## 1.1.5 - 2019-06-26

- Pre-release version


## 1.1.4 - 2019-06-25

- Pre-release version


## 1.1.3 - 2019-06-14

- Pre-release version


## 1.1.2 - 2019-06-10

- Pre-release version


## 1.1.1 - 2019-06-10

- Pre-release version


## 1.1.0 - 2019-06-10

- Pre-release version


## 1.0.18 - 2019-05-20

- Pre-release version


## 1.0.17 - 2019-05-20

- Pre-release version


## 1.0.16 - 2019-05-17

- Pre-release version


## 1.0.15 - 2019-05-17

- Pre-release version


## 1.0.14 - 2019-05-17

- Pre-release version


## 1.0.13 - 2019-05-17

- Pre-release version


## 1.0.12 - 2019-05-16

- Pre-release version


## 1.0.11 - 2019-05-16

- Pre-release version


## 1.0.10 - 2019-04-25

- Pre-release version


## 1.0.9 - 2019-04-25

- Pre-release version


## 1.0.8 - 2019-04-23

- Pre-release version


## 1.0.7 - 2019-04-23

- Pre-release version


## 1.0.6 - 2019-04-23

- Pre-release version


## 1.0.5 - 2019-04-12

- Pre-release version


## 1.0.4 - 2019-04-12

- Pre-release version


## 1.0.3 - 2019-04-10

- Pre-release version


## 1.0.2 - 2019-04-10

- Pre-release version


## 1.0.1 - 2019-04-09

- Pre-release version


## 1.0.0 - 2019-04-09


