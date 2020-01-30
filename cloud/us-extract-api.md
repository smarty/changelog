# Changelog - [US Extract API](https://smartystreets.com/docs/cloud/us-extract-api)

All notable changes to the US Extract API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## UNRELEASED

- n/a


## 3.3.1 - 2019-12-20

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.
- Local Installations Only:
	- It is now required that clients send requests with `Content-Type` of `text/plain; charset=utf-8`. Failure to do so may result in `HTTP 400 Bad Request`.
	- The server now longer limits the size of the request body or provides CORS response headers. If desired, this is now the responsibility of the organization hosting the local installation.


## 3.3.0 - 2019-09-06

CHANGES:

- Additional configuration values for cloud version to make downstream URL dynamic.
- Latest dependencies.

## 3.2.4 - 2019-08-16

CHANGES:

- Reworking build/publish boilerplate.


## 3.2.3 - 2019-08-16 [YANKED]

CHANGES:

- Reworking build/publish boilerplate.


## 3.2.2 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.

## 3.1.13 - 2019-04-18

- Rolled back changes introduced in 3.1.12 once issue was identified.


## 3.1.12 - 2019-04-18

- Includes additional http tracing to help debug an issue in production. (https://status.smartystreets.com/incidents/6052sfzh0xhh)


## 3.1.11 - 2019-04-04

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.5 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.4 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.3 - 2019-03-08

IMPROVEMENTS:
- Internal refactoring.

## 3.0.2 - 2019-03-06

IMPROVEMENTS:

- Overhauling module and deployment system. (No public-facing changes expected.)
- Updated internal dependencies.
- Compiled using Go v1.12.


## 3.0.1 - 2018-07-03

CHANGES:

- Final cleanup related to 3.0.0 release. Mostly just removed unneeded packaging declarations.


## 3.0.0 - 2018-07-03

CHANGES:

- Separated all authentication and authorization checkpoints to separate process, greatly slimming down wireup and configuration.
