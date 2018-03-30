# [International Street Address API](https://smartystreets.com/docs/local/international-street-api)

## 1.3.4 (March 30, 2018)

IMPROVEMENTS:

- The API executable has been compiled with Go v1.10.1 (https://golang.org/doc/devel/release.html#go1.10.minor). Previous versions were built with Go v1.9.4.


## 1.3.3 (March 28, 2018)

BUG FIXES:

- When the input `country` field contains an ISO-N value (3-digit numeric), it is standardized to its corresponding ISO-3 value before verification of the address. For example, when `076` (the ISO-N code for [Brazil](https://www.iso.org/obp/ui/#iso:code:3166:BR)) is submitted in the `country` field, it is now always standardized to `BRA` (the ISO-3) code before verification.

IMPROVEMENTS:

- The country name `CZECHIA` is now registered with the ISO-3 Country Code `CZE` (The Czech Republic).
- Internal restructuring and cleanup surrounding country validation.


## 1.3.2 (March 21, 2018)

IMPROVEMENTS:

- More structured logging of processing failures mentioned in [1.3.0](#1.3.0).
- Simplification of cloud hosting wireup (does not have any effect on local installations).


## 1.3.1 (March 16, 2018)

IMPROVEMENTS:

- Latest internal dependencies.


## 1.3.0 (March 7, 2018)

IMPROVEMENTS:

- Better handling of internal status checks.
- More verbose logging of certain kinds of processing failures.


## 1.2.8 (March 6, 2018)

IMPROVEMENTS:

- Internal logging simplified.


## 1.2.7 (January 16, 2018)

IMPROVEMENTS:

- All instances of the "Unicode Replacement Character" are removed from all input strings as a pre-processing step. See https://www.fileformat.info/info/unicode/char/fffd/index.htm


## 1.2.6 (January 11, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.5 (January 2, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.4 (January 2, 2018)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.3 (December 29, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.2 (December 28, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.1 (December 18, 2017)

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.0 (November 30, 2017)

FEATURES:

- New field added to Components structure: `PremisePrefixNumber`

IMPROVEMENTS:

- Code formatting enforced.

BUG FIXES:

- `address_format` field: Corrected ordering of sub-building fields during composition of this field to ensure correct result.
