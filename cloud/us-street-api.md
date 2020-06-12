# Changelog - [US Street Address API](https://smartystreets.com/docs/cloud/us-street-api)

All notable changes to the US Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## UNRELEASED

- n/a

## 4.2.4 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.


## 4.2.3 - 2020-06-10

CHANGES:

- Compiled against Go v1.14.4.
- Adjusted internal metrics reporting frequency.

## 4.2.2 - 2020-05-28

CHANGES:

- Compiled against Go v1.14.3.
- Includes the new usps/ams libraries.

## 4.2.1 - 2020-05-05

CHANGES:

- Internal behavior surrounding subscription management.


## 4.2.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 4.1.1 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.1.0 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.0.30 - 2020-03-17

BUG FIXES:

- Corrected concurrent access bug that caused intermittent geocode inaccuracies.


## 4.0.29 - 2020-03-16

CHANGES:

- Latest internal dependencies.


## 4.0.28 - 2020-03-13

CHANGES:

- Replace common misspellings in street input field

## 4.0.27 - 2019-12-20

CHANGES:

- Internal refactoring 


## 4.0.26 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.


## 4.0.21 - 2019-10-22

CHANGES:

- Latest version of internal dependencies.


## 4.0.20 - 2019-10-17

CHANGES:

- Refined certain log messages and updated to latest internal dependencies.


## 4.0.19 - 2019-09-18

CHANGES:

- Better handling of freeform inputs with stray punctuation.


## 4.0.18 - 2019-09-06

CHANGES:

- Internal refactoring.


## 4.0.17 - 2019-09-06

CHANGES:

- Latest version of internal, upstream dependencies.


## 4.0.16 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 4.0.15 - 2019-08-02

CHANGES:

- Latest internal dependencies.


## 4.0.14 - 2019-07-26

CHANGES:

- Slight change to internal boilerplate code used in development and testing.


## 4.0.12 - 2019-07-26

CHANGES:

- Latest internal dependencies.


## 4.0.11 - 2019-07-26 [YANKED: cloud installation]

BUG FIXES:

- Reinstated top-level /lib folder into the local installation package (required reworking much of the source code boilerplate).

CHANGES:

- Internal refactoring.
 

## 4.0.10 - 2019-07-12 [YANKED: local installation]

BUG FIXES:

- Corrected mishandling of lookups that contain no street information, introduced in the 4.0.0 release.


## 4.0.7 - 2019-07-09 [YANKED: local installation]

BUG FIXES:

- With the 4.0.0 release a concurrency-related bug was introduced in a hash calculation which caused the application to panic and shut down. (See incident details: https://status.smartystreets.com/incidents/dk5ghfl03vjf) This release fixes that issue.


## 4.0.0 - 2019-07-01 [YANKED]

This release, while a major version release represents a merging of internal code repositories and does not introduce any changes to the input/output contracts [as currently documented](https://smartystreets.com/docs/cloud/us-street-api).

CHANGES:

- Local installations can now make use of up to 64 cores (previously the max was 8).
- Local installations should log slow status check durations less frequently (when applicable).
- Local installations no longer limit the size of request payloads. 
- Clients of local installations must now submit a `Content-Type` header with `application/json; charset=utf-8` for `JSON` payloads. Failure to do so will result in `HTTP 400 Malformed Request`.
    - One option would be to put the local installation behind your own proxy that performs an override in the case of certain common content types submitted by tools such as cURL (`x-www-formurlencoded` to `application/json; charset=utf-8`).

## 3.3.2 - 2019-06-24

- Updated internal dependencies. Incrementing the minor version number in this case was a mistake.


## 3.2.22 - 2019-04-30

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.27 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.26 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.25 - 2019-03-08

CHANGES:
- Internal refactoring.


## 3.0.24 - 2019-03-06

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.

CHANGES:

- Overhauling module and deployment system. (No public-facing changes expected.)


## 3.0.23 - 2019-02-22

IMPROVEMENTS:

- Freeform inputs containing underscores (instead of spaces) will be sanitized and handled correctly.
- Updated all internal dependencies to latest versions.

BUG FIXES:

- Wireup race condition fixed in inner verification engine.


## 3.0.22 - 2018-11-29

IMPROVEMENTS:

- Latest internal dependencies


## 3.0.21 - 2018-11-29

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
