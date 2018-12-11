# [US ZIP Code API](https://smartystreets.com/docs/local/us-zipcode-api)

## 2.2.1 (December 11, 2018)

IMPROVEMENTS:

- ZIP Codes inputs submitted without leading zeros no longer result in a 'blank lookup' status (example: `501` -> `00501`).
- ZIP Codes inputs that consist only of zeros are now discarded as if they were blank. This allows requests such as the following to be processed as city/state lookups:

`/verify?zipcode=0&city=PROVO&state=UT`

## 2.2.0 (December 5, 2018)

IMPROVEMENTS:

- Latest internal dependencies.
- Made provision for R&D logging when hosted in the SmartyStreets production environment.

## Underlying Data Package (December 2018)

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
 

## 2.1.44 (September 19, 2018)

IMPROVEMENTS:

- Latest internal dependencies and some cleanup.


## 2.1.43 (May 23, 2018)

IMPROVEMENTS:

- Latest internal dependencies.


## 2.1.42 (May 21, 2018)

IMPROVEMENTS:

- Slightly better resolution of city names that contain apostrophes (ie. O'Fallon, IL).


## 2.1.41 (May 9, 2018)

IMPROVEMENTS:

- Restructured large swaths of code. No changes to the public HTTP application contract are expected.
- Updated internal dependencies.


## 2.1.40 (March 16, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.39 (January 11, 2018)

IMPROVEMENTS:

- Updated internal dependencies (we're on a roll latetly).


## 2.1.38 (January 5, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.37 (December 28, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 2.1.36 (December 18, 2017)

IMPROVEMENTS:

- Updated internal dependencies.

