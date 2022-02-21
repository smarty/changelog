# Changelog - [US Autocomplete API](https://www.smarty.com/docs/local/us-autocomplete-api)

Since 2019-08-09 the changelogs for the cloud and local installations of the US Autocomplete API have been merged and now reside where the [cloud installation changelog](https://github.com/smartystreets/changelog/blob/master/cloud/us-autocomplete-api.md) exists.

-------------------

All notable changes to the US Autocomplete API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased


## 2.2.1 - 2019-06-17

IMPROVEMENTS:

- Updated internal dependencies.

## 2.2.0 - 2019-04-29

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.
- Internal refactoring.
- Overhauled packaging and publishing mechanism.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 2.1.57 - 2018-12-17

BUG FIXES:

- Corrected aggressive CPU usage in case where errant default configuration value related to logging was used.


## 2.1.56 - 2018-12-06

- Modifications to schema of R&D logging.


## 2.1.55 - 2018-12-06

IMPROVEMENTS:

- Updated internal dependencies.
- Made provision for R&D logging when hosted in the Smarty production environment.


## 2.1.54 - 2018-09-20

BUG FIXES:

- Corrected logic that selects the remote address of the incoming request. We now select the first address (which should be the most reliable).

IMPROVEMENTS:

- Updated internal dependencies.
- Some cleanup and refactorings.

## 2.1.53 - 2018-05-15

IMPROVEMENTS:

- This release marks a more concrete separation between the core logic and the hosting environment (configuration/wireup). This allows us to separate wireups for cloud and local installations more cleanly. These changes do not modify the external interfaces and contracts.


## 2.1.52

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.51

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.50

IMPROVEMENTS:

- Disabled logging enabled in 2.1.48


## 2.1.49

BUG FIXES:

- Restored a slight variation on remote address selection behavior used for geocoding.


## 2.1.48

IMPROVEMENTS:

- Additional logging for cloud installations.


## 2.1.47 - 2018-01-17

BUG FIXES:

- Corrected bug introduced in 2.1.44 which prevented correct inspection and recording of the remote address, which in turn prevented [geolocated preferencing](https://www.smarty.com/docs/cloud/us-autocomplete-api#geolocate).


## 2.1.46 - 2018-01-11

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.45 - 2017-01-05

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.44 - 2017-12-28

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.43 - 2017-12-18

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.42 - 2017-12-13

IMPROVEMENTS:

- Updated internal csv scanner


## 2.1.41 - 2017-12-11

IMPROVEMENTS:

- Now using an open-source csv scanner for reading data files (github.com/smartystreets/scanners/csv).
