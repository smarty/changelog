# Changelog - [US Autocomplete API](https://smartystreets.com/docs/cloud/us-autocomplete-api)

All notable changes to the US Autocomplete API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## UNRELEASED

## 3.7.3 - 2020-07-27

CHANGES:
- Fixed an issue where in some cases, the same suggestion would be returned multiple times.


## 3.7.1 - 2020-07-23

CHANGES:
- Compiled using Go v1.16.x.
- Replaced several internal libraries


## 3.5.2 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.
- Compiled using Go v1.14.x.


## 3.5.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 3.4.4 - 2020-03-16

CHANGES:

- Latest internal dependencies.

## 3.4.3 - 2019-12-20

CHANGES:

- Internal refactoring 


## 3.4.2 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.


## 3.4.1 - 2019-09-06

BUG:

- Software version not correctly printed using command line flag.


## 3.4.0 - 2019-09-06

CHANGES:

- Internal dependency changes.

## 3.3.2 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 3.3.1 - 2019-08-09

CHANGES:

- Internal restructurings and refactorings.


## 3.2.8 - 2019-03-18

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.4 - 2018-12-06

Changes:

- Latest internal dependencies.