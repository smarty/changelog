# [DEPRECATED] Changelog - [US ZIP Code API](https://www.smarty.com/docs/local/us-zipcode-api)

All notable changes to the US ZIP Code API will now be documented in the [cloud installation changelog](https://github.com/smartystreets/changelog/blob/master/cloud/us-zipcode-api.md). This file remains only for historical purpose.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 5.0.0 - 2019-05-24

CHANGES:

- Restructured and consolidated all code for running the US ZIP Code API in the Smarty cloud or as a local installation. As such, this changelog (moving forward) will contain changes that apply to both isntallations. **As a result, this changelog will no longer be needed. See the [cloud installation changelog](https://github.com/smartystreets/changelog/blob/master/cloud/us-zipcode-api.md) for all changes moving forward in time.**
- CORS headers will no longer be provided to responses served by local installations. This is now the responsibility of organizations running their own local installation. There is no change to CORS header handling for users of the Smarty cloud installation (https://us-zipcode.api.smartystreets.com).


## 3.1.0 - 2019-04-29

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.
- Internal refactoring.
- Overhauled packaging and publishing mechanism.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.0 - 2018-12-26

IMPROVEMENTS:

- ZIP Code inputs that consist only of zeros are now discarded as if they were blank, but only if supplied along with non-blank City and State input values.


## 2.2.2 - 2018-12-12

BUG FIXES:

- Corrected aggressive CPU usage in case where errant default configuration value related to logging was used.


## 2.2.1 - 2018-12-11

IMPROVEMENTS:

- ZIP Code inputs submitted without leading zeros no longer result in a 'blank lookup' status (example: `501` -> `00501`).
- ZIP Code inputs that consist only of zeros are now discarded as if they were blank. This allows requests such as the following to be processed as city/state lookups:

`/verify?zipcode=0&city=PROVO&state=UT`

## 2.2.0 - 2018-12-05

IMPROVEMENTS:

- Latest internal dependencies.
- Made provision for R&D logging when hosted in the Smarty production environment.

## Underlying Data Package] - 018-12-01

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
 

## 2.1.44 - 2018-09-19

IMPROVEMENTS:

- Latest internal dependencies and some cleanup.


## 2.1.43 - 2018-05-23

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.42 - 2018-05-21

IMPROVEMENTS:

- Slightly better resolution of city names that contain apostrophes (ie. O'Fallon, IL).


## 2.1.41 - 2018-05-09

IMPROVEMENTS:

- Restructured large swaths of code. No changes to the public HTTP application contract are expected.
- Updated internal dependencies.


## 2.1.40 - 2018-03-16

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.39 - 2018-01-11

IMPROVEMENTS:

- Updated internal dependencies (we're on a roll latetly).


## 2.1.38 - 2018-01-05

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.37 - 2017-12-28

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.36 - 2017-12-18

IMPROVEMENTS:

- Updated internal dependencies.

