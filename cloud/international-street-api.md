# Changelog - [International Street Address API](https://www.smarty.com/docs/cloud/international-street-api)

All notable changes to the International Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
- These changes will be deployed throughout the day of Feb 9, 2026. 
- Changes to the Turkey (TUR) address components and format
  - DependentLocality will no longer be returned. Instead, it will return DoubleDependentLocality.
  - Locality will no longer be returned. Instead, it will return SubAdministrativeArea.
  - The format for the Address lines has been modified to use these new fields.
  - Possible customer impact:
    - If the customer is using only the Address lines returned in every result, then existing code will not be impacted. 
    - If the customer is building their own Address lines or using the individual components mentioned above, they will need to adjust their code to use the new fields.

## 3.8.12 - 2026-01-21
CHANGES:
- Internal maintenance. 

## 3.8.12 - 2026-01-21
CHANGES:
- Internal maintenance. 

## 3.8.10 - 2026-01-20
CHANGES:
- Added support for Bouvet Island (BVT), and Heard Island and McDonald Islands (HMD). 

## 3.8.9 - 2025-12-17
CHANGES:
- Normal code maintenance.

## 3.8.5 - 2025-11-09
CHANGES:
- Normal code maintenance.

## 3.8.4 - 2025-11-12
CHANGES:
- Fixed an issue with ISR (Israel) queries when the input is all Arabic and the results would return in Hebrew.

## 3.8.0 - 2025-11-11
CHANGES:
- Added geocode-classification feature flag.

## 3.7.5 - 2025-10-31
CHANGES:
- Fixed Kosovo ISO-3 code. It has been corrected to XKX.

## 3.7.4 - 2025-10-23
CHANGES:
- Improved address line formats for DNK, ITA, and FRA.


## 3.7.3 - 2025-10-06
CHANGES:
- Fixed Palau that was redirecting to USA. It has been corrected to PLW.
- Added more names for both Congo countries to better recognize their full names.


## 3.7.2 - 2025-09-26
CHANGES:
- Fixed FSM (Micronesia) which was being treated as a US territory.


## 3.7.1 - 2025-09-19
CHANGES:
- Normal code maintenance.


## 3.6.30 - 2025-09-03

CHANGES:
- Canada addresses with a sub building type of Ph or Th, will have this value used as a prefix to the sub building number.
  - Example:  Ph4-363 Sorauren Ave Toronto ON  M6R 3C1
- Updated data: 2025Q3.1-0


## 3.6.28 - 2025-08-08

CHANGES:
- Backed out the Canada fix made earlier today. It is not always appropriate to add the sub building type as a prefix. For example, PH is an appropriate prefix, but APT is not. We will create a more comprehensive fix later.

## 3.6.27 - 2025-08-08

CHANGES:
- Canada sub-building types will now be returned in the address lines.
- Enabled a new feature called `occupant_use` which provides the use type of the address, such as `residential` or `commercial`. This requires a specific plan.


## 3.6.26 - 2025-04-21

CHANGES:
- Internal maintenance.


## 3.6.24 - 2025-03-31

CHANGES:
- Fixed a formatting issue with CHE (Switzerland) addresses with building names.


## 3.6.23 - 2025-03-27

CHANGES:
- The `administrative_area_iso2` field will now always be uppercase to conform to standards.


## 3.6.20 - 2025-03-04

CHANGES:
- Internal maintenance.

## 3.6.18 - 2024-10-16

CHANGES:
- Fixed more address formatting issues for CAN sub-buildings


## 3.6.17 - 2024-10-11

CHANGES:
- Fixed some address formatting issues for CAN


## 3.6.16 - 2024-10-10

CHANGES:
- Release of October data.
- Added additional components for Canada
  - AdditionalContent
  - DeliveryInstallation
  - DeliveryInstallationType
  - DeliveryInstallationQualifierName
  - Route
  - RouteNumber
  - RouteType
- Use Enhanced Mode for queries of US addresses
- Fixed some casing issues


## 3.6.13 - 2024-09-09

CHANGES:
- Release of September data.


## 3.6.13 - 2024-09-03

CHANGES:
- Fixed address line formatting for sub-buildings in CAN. 
- Fixed formatting for KGZ.


## 3.6.10 - 2024-05-07

CHANGES:
- Added more options for valid country names. More specifically, any country name with the word "and" will also support an "&".  For example: As use can use: TRINIDAD AND TOBAGO or TRINIDAD & TOBAGO


## 3.6.7 - 2024-03-20

CHANGES:
- Fixed issue where Kosovo was not recognized as a supported country. 

## 3.6.6 - 2024-03-08

CHANGES:
- New data.


## 3.6.5 - 2024-02-23

CHANGES:
- Added Premise Type to AUS.


## 3.6.4 - 2024-02-20

CHANGES:
- Fixed sub-building formatting for FRA.


## 3.6.3 - 2024-01-29

CHANGES:
- Internal changes that will not affect results.


## 3.6.2 - 2024-01-10

CHANGES:
- Fixed an issue with TUR addresses where some address lines were missing.


## 3.6.1 - 2024-01-08

CHANGES:
- Added Dependent Locality to MEX formatted address lines.


## 3.6.0 - 2023-12-11

CHANGES:
- Code maintenance changes that should not affect results.


## 3.5.41 - 2023-11-27

CHANGES:
- Improved performance


## 3.5.39 - 2023-11-13

CHANGES:
- Fixed address formatting issues in ROU


## 3.5.35 - 2023-11-03

CHANGES:
- Internal changes that should not affect results.


## 3.5.32 - 2023-11-01

CHANGES:
- Fixed an issue where only the first of an ambiguous set of results would be returned.


## 3.5.30 - 2023-10-31

CHANGES:
- Removed ability to receive results in XML.
- Improved address lines for most countries. At times, it did not include sub-building.


## 3.5.28 - 2023-10-27

CHANGES:
- Supports using http method POST with no body. All parameters are still provided in the query string. This change was provide for integrations that require using POST to call external APIs.


## 3.5.25 - 2023-10-24

CHANGES:
- Significantly increased Delivery Point precision results. 


## 3.5.24 - 2023-10-16

CHANGES:
- Fixed issue where input_id would sometimes now be returned or would be an incorrect value. 


## 3.5.21 - 2023-10-11

CHANGES:
- Internal changes that will not affect results. 


## 3.5.13, 3.5.14 - 2023-10-04

CHANGES:
- Internal changes that will not affect results. 


## 3.5.10 - 2023-09-05

CHANGES:
- Removed the ability to receive results in XML based on the accept header. 


## 3.5.8 - 2023-08-30

CHANGES:
- Internal code changes that should not affect general results.


## 3.5.7 - 2023-08-22

CHANGES:
- Implemented format change in DEU for address lines. Move Sub Building after Premise.
- Fixed JPN formatting issues for native and latin.
- If no language is specified in the request we will determine it from the input character set. For best results, specify the language if consistent transliteration is needed.


## 3.5.5 - 2023-08-15

CHANGES:
- Fixed a sub building formatting issue for GBR.
- Where both an address and PO Box are returned (dual address), both will now be returned in the address lines. 


## 3.5.4 - 2023-08-10

CHANGES:
- Fixed a formatting issue for CAN PO Boxes where a linefeed was not being issued.


## 3.5.3 - 2023-08-10

IMPROVEMENTS:
- Improved handling and retention of building and apartment information for addresses.
- Improvements to the output address formats to better align with local postal expectations.
- Field-specific changes are now returned for transliterated addresses.
- Improved consistency in street abbreviations.

CHANGES:
- Standardization of administrative_area field (removal of administrative_area_short and administrative_area_long fields)
- MEX administrative_area will now utilize the ISO-3 state code.
- Field-specific changes no longer apply to full address lines (as they are more useful on individual fields).
- New component field (level_number) - for applicable countries


## 3.3.35 - 2023-05-08

CHANGES:

- Fixed an issue where it could cause the server to restart.
- No longer return sub city type in address lines for NLD.


## 3.3.34 - 2023-04-28

CHANGES:

- Internal changes that do not affect results.


## 3.3.33 - 2023-04-20

CHANGES:

- An internal fix that will not affect results.


## 3.3.32 - 2023-04-19

CHANGES:

- An internal fix that will not affect results.


## 3.3.31 - 2023-04-19

CHANGES:

- No longer return sub city type in address lines for CHE and SGP.
- Prefix ALA postal codes with AX


## 3.3.30 - 2023-04-03

CHANGES:

- Fixed an issue that resulted in inconsistent results being returned.


## 3.3.29 - 2023-03-30

CHANGES:

- Performance improvements


## 3.3.27 - 2023-03-21

CHANGES:

- Fixed issue for JPN where Premise numbers would not match the output language.


## 3.3.26 - 2023-03-10

CHANGES:

- Fixed an issue where some PO Box results would incorrectly have a precision of Thoroughfare. It is now DeliveryPoint.
- Fixed an issue with Postal code analysis changes for CAN and GBR.
- Improved input handling so we will return results when previously no results would be returned.
- Eliminated Company and Organization from address lines.
- Fixed formatting of sub building data in GBR.
- Added dependent thoroughfare in the address lines for GBR.
- Fixed an issue where status would be ambiguous when a single result would be returned.


## 3.3.23 - 2023-01-27

CHANGES:

- Improved BEL results by adding sub and super administrative area data.
- Released new quarterly data and improved search engine.


## 3.3.19 - 2022-11-10

CHANGES:

- Implemented new data to improve results.
- Fixed precision for PO Box results - is now Locality.
- Handle abbreviated thoroughfare types in POL.


## 3.3.16 - 2022-10-27

CHANGES:

- Fixed an issue with the health check that could make it unhealthy unexpectedly.
- Added NOR to the Germanic Street Suffix handling.
- Added an Administrative Area table for GBR so it will always return one.


## 3.3.14 - 2022-10-25

CHANGES:

- Backed out the feature in 3.3.12 as it created a health check failure after a few hours and caused an outage.


## 3.3.12 - 2022-10-24

CHANGES:

- Implemented a feature to improve results across the board.


## 3.3.11 - 2022-10-05

CHANGES:

- Compiled against Go v1.19.
- Internal changes that should not affect the user experience.


## 3.3.9 - 2022-10-04

CHANGES:

- Added PRT as a super administrative area country. 
- Updated address formatting for various countries.
- Updated postal code data for countries with a single or no postal code.


## 3.3.7 - 2022-09-28

CHANGES:

- Added new fields in result (when applicable): administrative_area_short and administrative_area_long
- Added a list of countries that always use administrative_area_short for the value of administrative_area.
  [AUS BRA BRB CAN CHE CXR CCK GIB ITA MEX]


## 3.3.6 - 2022-09-22

CHANGES:

- Fixed Plot/Premise issue for THA. We now prepend PLOT when to the premise number when available.
- Add DNK to the list of countries for Germanic street suffix handling where some suffixes are appended to the street with no space.
- Added fields to the output: level_type, level_number when available.
- Standardized address line formatting for various countries.
- Use the new Level fields in the AUS address lines.


## 3.3.5 - 2022-09-19

CHANGES:

- Return expanded CAN pre-directionals. (e.g. it was S, now is South)
- Improved GBR results by not falling back to street centroid results.
- Improved GBR results by not including the input premise number when none was requested.
- Add building name to the results where applicable.
- Improved LUX results by pre-processing the requested Postal Code.
- Improved overall performance.


## 3.3.2 - 2022-09-07

CHANGES:

- Fixed an issue for GBR addresses that could cause inconsistent results.


## 3.3.1 - 2022-09-06

CHANGES:

- Updated logic for countries that use Super Administrative Area. Removed SVN from the S.A.A. country list.
- Fixed a miscalculation of the changes field for Locality and Admin area.
- Improved CAN results for freeform queries.


## 3.3.0 - 2022-08-23

CHANGES:

- Updated the data to improve results.
- Fixed issue where sub buildings may be returned that are not associated with the result.
- Will only attempt to transliterate for native countries. Updated native country list.
- Improved GBR results.


## 3.2.15 - 2022-08-18

CHANGES:

- Organization data will now be used in the search.
- Improved search results in GBR and JPN.
- Restored postal code prefix for LVA.


## 3.2.12 - 2022-08-17

CHANGES:

- Updated the max precision for various countries.
- Updated list of countries that have super administration areas.
- Fixed the changes field for NLD postal codes.
- Fixed the changes field for some sub building scenarios.
- Fixed sub building deficiencies for some GBR addresses.
- Fixed precision for CAN addresses where no thoroughfare was matched.
- Eliminate duplicate candidates.


## 3.2.11 - 2022-08-01

CHANGES:

- Fixed issue where some postal codes would have the two letter country code prepended. Specifically SWE, LVA, LTU.
- Fixed AUS unit placement in results. It is now returned as a prefix to the premise number separated by a slash.


## 3.2.10 - 2022-07-28

CHANGES:

- Fixed high latency issues.
- Fixed inconsistent casing issues.


## 3.2.5 - 2022-07-18

CHANGES:

- Fixed address_format for PO Box results. It contained fields not used to build the address fields.
- Improved results in when components are used in the lookup.
- Fixed an issue with the changes section in the premise field. Sometimes it would say Verified when it should have been Identified.


## 3.2.1 - 2022-07-05

CHANGES:

- Fixed issue where postal codes could be incorrect.


## 3.1.16 - 2022-06-28

CHANGES:

- Fixed NLD postal code issue where the suffix was not being included.


## 3.1.15 - 2022-06-20

CHANGES:

- Added AUT to a list of countries affected by the street suffix concatenation fix in 3.1.5.
- Fixed bug that would not recognize changes to the ThoroughfareType field.
- Improved search results in all countries.


## 3.1.10 - 2022-06-14

CHANGES:

- Fixed issue that would occasionally return inconsistent results.


## 3.1.8 - 2022-06-08

CHANGES:

- Fixed bug that would not remove diacritics and ligatures when language is set to latin.
- Added SWE to a list of countries affected by the street suffix concatenation fix in 3.1.5.
- Fixed issue where transliteration would not occur for freeform requests.


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
