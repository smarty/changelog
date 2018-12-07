# [US Autocomplete API](https://smartystreets.com/docs/local/us-autocomplete-api)


## 2.1.56 (December 6, 2018)

- Modifications to schema of R&D logging.

## 2.1.55 (December 6, 2018)

IMPROVEMENTS:

- Updated internal dependencies.
- Made provision for R&D logging when hosted in the SmartyStreets production environment.


## 2.1.54 (September 20, 2018)

BUG FIXES:

- Corrected logic that selects the remote address of the incoming request. We now select the first address (which should be the most reliable).

IMPROVEMENTS:

- Updated internal dependencies.
- Some cleanup and refactorings.

## 2.1.53 (May 15, 2018)

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


## 2.1.47 (January 17, 2018)

BUG FIXES:

- Corrected bug introduced in 2.1.44 which prevented correct inspection and recording of the remote address, which in turn prevented [geolocated preferencing](https://smartystreets.com/docs/cloud/us-autocomplete-api#geolocate).


## 2.1.46 (January 11, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.45 (January 5, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.44 (December 28, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.43 (December 18, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.42 (December 13, 2017)

IMPROVEMENTS:

- Updated internal csv scanner


## 2.1.41 (December 11, 2017)

IMPROVEMENTS:

- Now using an open-source csv scanner for reading data files (github.com/smartystreets/scanners/csv).