# [US Street API (local installation)](https://smartystreets.com/docs/local/us-street-api)

## 2.2.8 (March 28, 2018)

IMPROVEMENTS:

- The ZIP Code value is now consistently sanitized in preparation for processing regardless of where it resides in the request, which could be any of the following locations:
	1. The `zipcode` field (the was previously the only properly sanitized location)
	2. The last word of the `city` field
	3. The last word of the `lastline` field
	4. The last word of the `street` field (freeform input)
- Latest internal dependencies.


## 2.2.7 (March 23, 2018)

IMPROVEMENTS:

- We now remove 'smart quotes' (double and single) and reverse back-ticks from all input strings.

## 2.2.6 (February 14, 2018)

BUG FIXES:

- Incorporated patch from upstream provider to address a rare SEGFAULT caused by inputs with "too many parsed words".


## 2.2.5 (January 11, 2018)

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.4 (January 3, 2018)

BUG FIXES:

- Preventing a runtime panic related to absence of any Account ID (which is never present in requests sent to local installations of the US Street API).


## 2.2.3 (December 28, 2017)

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.2 (December 20, 2017)

IMPROVEMENTS:

- Better sanitization of long input strings.


## 2.2.1 (December 18, 2017)

IMPROVEMENTS:

- Latest internal dependencies.


## 2.2.0 (December 14, 2017)

IMPROVEMENTS:

- In the case of input that results in an invalid address, we now return county information if a valid ZIP Code was part of the input.
