# Changelog - [International Street Address API](https://smartystreets.com/docs/local/international-street-api)

All notable changes to the International Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

IMPROVEMENTS:

- If `address1` is not provided but `address2`, etc. exist, use those instead.
- Updated internal engine to close more cleanly during shutdown signal.


## 1.5.0 - 2019-03-14

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.

CHANGES:

- New object to appear in the `analysis` object, entitled `changes` which mirrors the structure of the address fields provided at the top-level object and in the components object. Each field describes what changes were made to the parsed input in order to deliver the final result. (Full documentation and SDK support pending.) Example:

```
curl "international-street.api.smartystreets.com/verify?auth-id=123&auth-token=abc&country=Australia&address1=200%20River%20Terrace&address2=&locality=Kangaroo%20Point&administrative_area=Queensland&postal_code=4169&geocode=true&experimental=true"
[
   {
      "analysis" : {
         "verification_status" : "Verified",
         "changes" : {
            "components" : {
               "locality" : "Verified-NoChange",
               "postal_code" : "Verified-NoChange",
               "thoroughfare_trailing_type" : "Identified-AliasChange",
               "country_iso_3" : "Added",
               "thoroughfare_name" : "Identified-ContextChange",
               "administrative_area" : "Verified-AliasChange",
               "premise" : "Verified-NoChange",
               "postal_code_short" : "Verified-NoChange",
               "premise_number" : "Verified-NoChange",
               "thoroughfare" : "Verified-AliasChange"
            },
            "address2" : "Verified-AliasChange",
            "address1" : "Verified-AliasChange"
         },
         "address_precision" : "Premise",
         "max_address_precision" : "DeliveryPoint"
      },
      "metadata" : {
         // ommitted for the sake of brevity
      },
      "address2" : "KANGAROO POINT QLD 4169",
      "components" : {
         // ommitted for the sake of brevity
      },
      "address1" : "200 River Tce"
   }
]
```


## 1.4.1 - 2018-09-06

BUG FIXES:

- For a relatively short time, invalid US addresses elicited a response of `null` instead of the expected empty array (`[]`). This is now fixed.


## 1.4.0 - 2018-07-17

IMPROVEMENTS:

- Implemented a way for customers interested in beta-testing features to get access to experimental behaviors. This isn't the changelog entry you were looking for. Move along.


## 1.3.18 - 2018-06-18

IMPROVEMENTS:

- Changes to the way the status route works internally (/status). No observable exterior changes in behavior are expected.

## 1.3.17 - 2018-07-12

IMPROVEMENTS:

- Latest internal dependencies.

## 1.3.16 - 2018-07-09

IMPROVEMENTS:

- Corrections to build parameters. No external changes.


## 1.3.15 - 2018-07-03

IMPROVEMENTS:

- Lots of internal restructuring in preparation for consolidating the differences between the SmartyStreets cloud installation and this 'local' installation. No external changes in behavior.


## 1.3.14 - 2018-06-15

IMPROVEMENTS:

- We now use the [SmartyStreets Go SDK](https://smartystreets.com/docs/sdk/go) for processing inputs where the `country` field is "USA".


## 1.3.13 - 2018-06-08

IMPROVEMENTS:

- Refactored several components, no external changes (all tests passing)


## 1.3.12 - 2018-05-26

IMPROVEMENTS:

- Moved rate-limit wireup closer to usage (only affects the SmartyStreets cloud installation).


## 1.3.11 - 2018-05-19

IMPROVEMENTS:

- Latest internal dependencies.


## 1.3.10 - 2018-05-18

IMPROVEMENTS:

- Fixes to build parameters (no behavior changes).


## 1.3.9 - 2018-05-16

IMPROVEMENTS:

- Improvements to logging interface (only affects the SmartyStreets cloud installation).

## 1.3.8 - 2018-05-16

IMPROVEMENTS:

- Corrected rate-limit config values (only affects the SmartyStreets cloud installation).

## 1.3.7 - 2018-05-16

IMPROVEMENTS:

- Latest internal dependencies.
- Updates to rate-limiting wireup (only affects the SmartyStreets cloud installation).

## 1.3.6 - 2018-05-14

IMPROVEMENTS:

- Updated configuration values for messaging systems (only affects the SmartyStreets cloud installation).

## 1.3.5 - 2018-05-14

IMPROVEMENTS:

- Latest internal dependencies.


## 1.3.4 - 2018-03-30

IMPROVEMENTS:

- The API executable has been compiled with Go v1.10.1 (https://golang.org/doc/devel/release.html#go1.10.minor). Previous versions were built with Go v1.9.4.


## 1.3.3 - 2018-03-28

BUG FIXES:

- When the input `country` field contains an ISO-N value (3-digit numeric), it is standardized to its corresponding ISO-3 value before verification of the address. For example, when `076` (the ISO-N code for [Brazil](https://www.iso.org/obp/ui/#iso:code:3166:BR)) is submitted in the `country` field, it is now always standardized to `BRA` (the ISO-3) code before verification.

IMPROVEMENTS:

- The country name `CZECHIA` is now registered with the ISO-3 Country Code `CZE` (The Czech Republic).
- Internal restructuring and cleanup surrounding country validation.


## 1.3.2 - 2018-03-21

IMPROVEMENTS:

- More structured logging of processing failures mentioned in [1.3.0](#1.3.0).
- Simplification of cloud hosting wireup (does not have any effect on local installations).


## 1.3.1 - 2018-03-16

IMPROVEMENTS:

- Latest internal dependencies.


## 1.3.0 - 2018-03-07

IMPROVEMENTS:

- Better handling of internal status checks.
- More verbose logging of certain kinds of processing failures.


## 1.2.8 - 2018-03-06

IMPROVEMENTS:

- Internal logging simplified.


## 1.2.7 - 2018-01-16

IMPROVEMENTS:

- All instances of the "Unicode Replacement Character" are removed from all input strings as a pre-processing step. See https://www.fileformat.info/info/unicode/char/fffd/index.htm


## 1.2.6 - 2018-01-11

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.5 - 2018-01-02

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.4 - 2018-01-02

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.3 - 2017-12-29

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.2 - 2017-12-28

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.1 - 2017-12-18

IMPROVEMENTS:

- Updated internal dependencies.


## 1.2.0 - 2017-11-30

FEATURES:

- New field added to Components structure: `PremisePrefixNumber`

IMPROVEMENTS:

- Code formatting enforced.

BUG FIXES:

- `address_format` field: Corrected ordering of sub-building fields during composition of this field to ensure correct result.
