# [US ZIP Code API](https://smartystreets.com/docs/local/us-zipcode-api)

## [3.0.0] - 2018-12-26

IMPROVEMENTS:

- ZIP Code inputs that consist only of zeros are now discarded as if they were blank, but only if supplied along with non-blank City and State input values.


## [2.2.2] - 2018-12-12

BUG FIXES:

- Corrected aggressive CPU usage in case where errant default configuration value related to logging was used.


## [2.2.1] - 2018-12-11

IMPROVEMENTS:

- ZIP Code inputs submitted without leading zeros no longer result in a 'blank lookup' status (example: `501` -> `00501`).
- ZIP Code inputs that consist only of zeros are now discarded as if they were blank. This allows requests such as the following to be processed as city/state lookups:

`/verify?zipcode=0&city=PROVO&state=UT`

## [2.2.0] - 2018-12-05

IMPROVEMENTS:

- Latest internal dependencies.
- Made provision for R&D logging when hosted in the SmartyStreets production environment.

## [Underlying Data Package] - 2018-12-01

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
 

## [2.1.44] - 2018-09-19

IMPROVEMENTS:

- Latest internal dependencies and some cleanup.


## [2.1.43] - 2018-05-23

IMPROVEMENTS:

- Latest internal dependencies.


## [2.1.42] - 2018-05-21

IMPROVEMENTS:

- Slightly better resolution of city names that contain apostrophes (ie. O'Fallon, IL).


## [2.1.41] - 2018-05-09

IMPROVEMENTS:

- Restructured large swaths of code. No changes to the public HTTP application contract are expected.
- Updated internal dependencies.


## [2.1.40] - 2018-03-16

IMPROVEMENTS:

- Updated internal dependencies.


## [2.1.39] - 2018-01-11

IMPROVEMENTS:

- Updated internal dependencies (we're on a roll latetly).


## [2.1.38] - 2018-01-05

IMPROVEMENTS:

- Updated internal dependencies.


## [2.1.37] - 2017-12-28

IMPROVEMENTS:

- Updated internal dependencies.


## [2.1.36] - 2017-12-18

IMPROVEMENTS:

- Updated internal dependencies.

