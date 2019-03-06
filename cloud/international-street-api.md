# Changelog - [International Street Address API](https://smartystreets.com/docs/cloud/international-street-api)

All notable changes to the International Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## 2.1.5 - 2019-03-06

FIXES:

- Fixed configuration reader wireup

## 2.1.4 - 2019-03-06 [YANKED]

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.

CHANGES:

- Overhauling module and deployment system. (No public-facing changes expected.)
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


## 2.1.3 - 2018-09-05

CHANGES:

- Latest web translation code.
