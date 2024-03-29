# Changelog - [US Extract API](https://www.smarty.com/docs/local/us-extract-api)

Since 2019-08-16 the changelogs for the cloud and local installations of the US Extract API have been merged and now reside where the [cloud installation changelog](https://github.com/smartystreets/changelog/blob/master/cloud/us-extract-api.md) exists.

--------------

All notable changes to the US Extract API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## Unreleased


## 2.3.0 - 2019-06-17

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.
- Internal refactoring.
- Overhauled build pipeline used for packaging new versions.

NOTES:

- Skipped 2.2.x because of a tag conflict on an internal release


## 2.1.63 - 2018-09-20

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.62 - 2018-04-06

IMPROVEMENTS:

- This release marks a more concrete separation between the core logic and the hosting environment (configuration/wireup). This allows us to seprate wireups for cloud and local installations more cleanly. These changes do not modify the external interfaces and contracts.
- Sanitization logic is now executed closer to the core extraction algorithm (as a result of the previously mentioned improvement).


## 2.1.61 - 2018-03-16

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.60 - 2018-02-15

BUG FIXES:

- More corrections to formatting of messages related to error logging.


## 2.1.59 - 2018-02-15

BUG FIXES:

- Corrected format string in pcre tests.

IMPROVEMENTS:

- Modified severity of language surrounding error logging.


## 2.1.58 - 2018-01-11

IMPROVEMENTS:

- Latest internal dependencies (we're on a roll lately).


## 2.1.57 - 2018-01-05

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.56 - 2017-12-22

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.55 - 2017-12-20

IMPROVEMENTS:

- Now using version 7.0.0 of the Smarty Go SDK (https://www.smarty.com/docs/sdk/go) which introduces function configuration/wireup.
- Downgraded severity of internal log entries.


## 2.1.54 - 2017-12-18

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.53 - 2017-12-15

IMPROVEMENTS:

- Error condition log messages more clear.
