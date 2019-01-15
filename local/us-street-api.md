# Changelog - [US Street Address API](https://smartystreets.com/docs/local/us-street-api)

All notable changes to the US Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## 2.2.25 - 2018-11-29

IMPROVEMENTS:

- Latest internal dependencies


## 2.2.24 - 2018-11-29

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.


## 2.2.23 - 2018-11-26

IMPROVEMENTS:

- The `default_city_field` within the `components` output structure is not always populated, even when it matches the `city` field.


## 2.2.22 - 2018-11-12

IMPROVEMENTS:

- Improved logging message prefix.


## 2.2.21 - 2018-11-11

IMPROVEMENTS:

- Installed additional logging around failure conditions related to freeform address processing.


## 2.2.20 - 2018-11-06

BUG FIXES:

- Fixed a but introduced with 2.2.17 (a release that really did rock the boat) that prevented fully spelled state names from being recognized in component inputs. 


## 2.2.19 - 2018-11-05

BUG FIXES:

- Fixed another bug related to freeform processing improvements mentioned in 2.2.17. This one had to do with us trying to do too much for addresses that present a ZIP Code in the wrong place, but our logic was too aggressive and somehow it got past our rigorous acceptance test suite. (Who submits the ZIP Code in the wrong place, anyway?)


## 2.2.18 - 2018-11-05

BUG FIXES:

- Fixed bug related to freeform processing improvements mentioned in 2.2.17 that slipped through the cracks in that release. This bug only affected freeform requests where the data submitted only consisted of a state and a ZIP Code. (Who does that, anyway?)


## 2.2.17 - 2018-11-02

IMPROVEMENTS:

- Freeform Processing: We now do a much better job of selecting the boundary between the delivery line and the last line (City, State, ZIP Code) which improves matching and the quality of the output, especially in situations where the input contains secondary information, the city is several words long, and/or the state is fully spelled out (rather than abbreviated to two characters).
- Start-up behavior: We now allow the entire process to die if any data files are missing or cannot be loaded. See the stderr stream for explanatory log entries. "Dead programs tell no lies." (The Pragmatic Programmer, Andrew Hunt & Dave Thomas)
- Updated many internal dependencies.


## 2.2.16 - 2018-09-06

IMPROVEMENTS:

- Various internal improvements and optimizations.

BUG FIXES:

- Algorithm that prioritizes between single and batched lookups no longer causes excessively high CPU idling.


## 2.2.15 - 2018-06-06

IMPROVEMENTS:

- While we don't remove apostrophes from city and street names we get from the USPS, we no longer attempt to insert apostrophes in city and street names either.


## 2.2.14 - 2018-06-06

BUG FIXES:

- No longer requiring a config.json file (caused a crash at startup; mistakenly introduced in 2.2.12).


## 2.2.13 - 2018-06-04

IMPROVEMENTS:

- Result candidates of freeform inputs with 3-word city names are now selected with greater care. For example, the freeform input `PO Box 160 Cold Spring Harbor NY 11724` would previously return a result from `Spring Brook NY 14140` rather than `Cold Spring Harbor NY 11724` as expected at the time of this writing.


## 2.2.12 - 2018-05-23

IMPROVEMENTS:

- More internal restructuring and standardization.
- In the case that required shared libraries have not been correctly installed, the resulting error message now points to the online installation instructions: https://smartystreets.com/docs/local/us-street-api#install


## 2.2.11 - 2018-04-05

BUG FIXES:
    
- Version 2.2.10 incorrectly displayed "dev" as its version when run with the -version flag. This has been fixed for future versions.


## 2.2.10 - 2018-04-04

IMPROVEMENTS:

- Updated internal dependencies
- Restructured configuration and wireup components (no changes to any external behavior)


## 2.2.9 - 2018-03-30

IMPROVEMENTS:

- The API executable has been compiled with Go v1.10.1 (https://golang.org/doc/devel/release.html#go1.10.minor). Previous versions were built with Go v1.9.4.


## 2.2.8 - 2018-03-28

IMPROVEMENTS:

- The ZIP Code value is now consistently sanitized in preparation for processing regardless of where it resides in the request, which could be any of the following locations:
	1. The `zipcode` field (the was previously the only properly sanitized location)
	2. The last word of the `city` field
	3. The last word of the `lastline` field
	4. The last word of the `street` field (freeform input)
- Latest internal dependencies.


## 2.2.7 - 2018-03-23

IMPROVEMENTS:

- We now remove 'smart quotes' (double and single) and reverse back-ticks from all input strings.

## 2.2.6 - 2018-02-14

BUG FIXES:

- Incorporated patch from upstream provider to address a rare SEGFAULT caused by inputs with "too many parsed words".


## 2.2.5 - 2018-01-11

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.4 - 2018-01-03

BUG FIXES:

- Preventing a runtime panic related to absence of any Account ID (which is never present in requests sent to local installations of the US Street API).


## 2.2.3 - 2017-12-28

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.2 - 2017-12-20

IMPROVEMENTS:

- Better sanitization of long input strings.


## 2.2.1 - 2017-12-18

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.0 - 2017-12-14

IMPROVEMENTS:

- In the case of input that results in an invalid address, we now return county information if a valid ZIP Code was part of the input.
