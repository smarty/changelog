# Changelog - [International Street Address API](https://smartystreets.com/docs/cloud/international-street-api)

All notable changes to the International Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## UNRELEASED

- n/a


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

- New object nested within the `analysis` object, entitled `changes` which mirrors the structure of the address fields provided at the top-level object and in the components object. Each field describes what changes were made to the parsed input in order to deliver the final result. (See [full documentation](https://smartystreets.com/docs/cloud/international-street-api#changes), SDK support pending.) Example:

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
