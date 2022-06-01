# Changelog - [International Street Address API](https://www.smarty.com/docs/cloud/international-street-api)

All notable changes to the International Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 3.1.5 - 2022-06-01

CHANGES:

- Improved transliteration results for Japan.
- Fixed accuracy issues for many CAN and GBR addresses.
- Improved street suffix concatenation in Germanic language countries. 
     e.g. Agnes Straat vs. Agnesstraat


## 3.0.10 - 2022-05-05

CHANGES:

- Improved transliteration results for Japan.
- Fixed issue where input_id was not returned in some cases.
- Fixed accuracy issues for many GBR addresses.


## 3.0.3 - 2022-04-27

CHANGES:

- Data enhancement for International Street API including higher rates of DeliveryPoint matches for many countries.
- Premise matches now indicate that the house number was found within the range for a specific street segment.
- Language transliteration is now country-specific.
- Compiled against Go v1.17.8.
- Upgrade to latest dependencies.


## 2.8.5 - 2020-12-16

CHANGES:

- Upgrade to latest dependencies.
- Compiled using Go v1.15.x.
- Resolved another intermittent shutdown panic ("send on closed channel").


## 2.8.4 - 2020-09-04

CHANGES:

- Resolved intermittent shutdown panic ("send on closed channel").


## 2.8.1 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.
- Compiled using Go v1.14.x.


## 2.8.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 2.7.1 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 2.7.0 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 2.6.4 - 2020-03-16

CHANGES:

- Latest internal dependencies.


## 2.6.2 - 2019-12-20

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.

## 2.6.0 - 2019-09-06

- Latest version of internal, upstream dependencies.
- Allowing dynamic selection via configuration of US Street API (cloud version only).

## 2.5.7 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.

## 2.5.6 - 2019-08-07

CHANGES:

- Additional fix related to country of `Timor Leste` (see [2.5.2](#252---2019-08-02)).


## 2.5.5 - 2019-08-07

CHANGES:

- Further improvements and flexibility surrounding addresses from "Åland Islands" (see version [2.5.3](#253---2019-08-07)).


## 2.5.4 - 2019-08-07

CHANGES:

- Updated internal dependencies.


## 2.5.3 - 2019-08-07

CHANGES:

- The ISO3 code for some aliases of ["Åland Islands"](https://en.wikipedia.org/wiki/%C3%85land_Islands) (a province of Finland) was incorrect. We now recognize "Aland" as a valid alias. 


## 2.5.2 - 2019-08-02

CHANGES:

- The country of `Timor Leste` is now recognized by both `TLP` and `TLS` even though its proper ISO3 code is `TLS`.
- Many internal refactorings and restructurings.


## 2.4.13 - 2019-07-22

IMPROVEMENTS:

- A few more fixes surrounding a clean process shutdown.


## 2.4.12 - 2019-07-22

IMPROVEMENTS:

- Additional fixes surrounding a clean process shutdown.

BUG FIXES:

- Corrected ISO3 code for `Timor-Leste` to `TLS`.


## 2.4.11 - 2019-06-28

IMPROVEMENTS:

- Misc bug fixes to facilitate a clean process shutdown.


## 2.4.10 - 2019-06-05

CHANGES:

- Internal structural changes to better support subscription management.


## 2.4.9 - 2019-05-29

CHANGES:

- Removed temporary diagnostic/logging behavior.


## 2.4.8 - 2019-05-29

CHANGES:

- Additional diagnostic/logging information to monitor system health.


## 2.4.7 - 2019-05-04

CHANGES:

- Removed temporary diagnostic/logging behavior.


## 2.4.6 - 2019-05-03

CHANGES:

- Internal dependency changes.
- Additional diagnostic/logging information to monitor system health.


## 2.4.5 - 2019-04-12

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 2.3.6 - 2019-03-27

IMPROVEMENTS:

- If `address1` is not provided but `address2`, etc. exist, use those instead.
- Updated internal engine to close more cleanly during shutdown signal.


## 2.3.5 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 2.3.4 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 2.3.3 - 2019-03-25

CHANGES:
- Internal release.


## 2.3.2 - 2019-03-13

CHANGES:

- Internal refactoring: Partitioning workload based upon account information.


## 2.3.1 - 2019-03-13

CHANGES:

- Making internal messages routed between various internal systems durable/persistent.


## 2.3.0 - 2019-03-12

CHANGES:

- New object nested within the `analysis` object, entitled `changes` which mirrors the structure of the address fields provided at the top-level object and in the components object. Each field describes what changes were made to the parsed input in order to deliver the final result. (See [full documentation](https://www.smarty.com/docs/cloud/international-street-api#changes), SDK support pending.) Example:

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


## 2.1.5 - 2019-03-06

FIXES:

- Fixed configuration reader wireup


## 2.1.4 - 2019-03-06 [YANKED]

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.


## 2.1.3 - 2018-09-05

CHANGES:

- Latest web translation code.
