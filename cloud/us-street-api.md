# Changelog - [US Street Address API](https://www.smarty.com/docs/cloud/us-street-api)

All notable changes to the US Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 5.12.0 - 2025-05-27
We are beginning our phased rollout of us-street-api 5.12.0. This process is scheduled to be completed by 2025-05-28 00:00:00 UTC.

### CHANGES
- This deploy is in preparation for the beta release of Component Analysis.
- This deploy will not affect results.

## 5.11.8 - 2025-05-23
We are beginning our phased rollout of us-street-api 5.11.8 and its associated us-street-data 1.1:2025.05.D. This process is scheduled to be completed by 2025-05-24 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- This includes a data release of version 1.1:2025.05.D
- For the local download of us-street-api with the enhanced data addon, you can now use county_source=geographic to request geographic county information.

## 5.11.7 - 2025-05-19
We are beginning our phased rollout of us-street-api 5.11.7. This process is scheduled to be completed by 2025-05-21 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved matching on addresses with ordinal and fraction components
- Improved enhanced_match field result with ignored input

## 5.11.5 - 2025-05-15
Changes:
- Improved matching with addresses that include invalid secondaries
- Improved matching with partial match results

## 5.11.2 - 2025-05-08
We are beginning our phased rollout of us-street-api 5.11.2. This process is scheduled to be completed by 2025-05-10 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

Changes:
- Improved matching where the street name matches the city name.
- Improved matching in cases where Saint is abbreviated as ST in city names and street names

## 5.11.1 - 2025-04-30
We are beginning our phased rollout of us-street-api 5.11.1. This process is scheduled to be completed by 2025-05-03 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

Changes:
- Internal data restructuring

## 5.11.0 - 2025-04-24
We are beginning our phased rollout of us-street-api 5.11.0. This process is scheduled to be completed by 2025-04-26 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### CHANGES
- Added a new enhanced_match value, address-link-conversion, this is to show the address components were changed based on authoritative data to a linked address.

### FIXED
- Improved matching when lastline components are out of order, especially when zipcode appears before the city/state.
- Improved matching with hyphens.

## 5.10.8 - 2025-03-27
We are beginning our phased rollout of us-street-api 5.10.8. This process is scheduled to be completed by 2025-03-29 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Latest internal dependencies.

## 5.10.7 - 2025-03-24
We are beginning our phased rollout of us-street-api 5.10.7. This process is scheduled to be completed by 2025-03-26 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved handling of secondary floor addresses.

## 5.10.4 - 2025-03-14

### FIXED
- Improved geographic county accuracy in enhanced mode.

## 5.10.3 - 2025-03-13
We are beginning our phased rollout of us-street-api 5.10.3. This process is scheduled to be completed by 2025-03-16 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved handling on various common spelling corrections
- Improved common abbreviations with periods
- Improved delivery line 2 information that removes information that is used as part of the matching process
- 'enhanced-match: missing-secondary' will only appear on addresses that require a secondary in order to be a deliverable address
- Various other minor changes to improve matching across the board

## 5.10.0 - 2025-03-03
We are beginning our phased rollout of us-street-api 5.10.0. This process is scheduled to be completed by 2025-03-05 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- DPVFootnotes are now always in alphabetical order
- Updated addresses with invalid secondaries now have the same DPV barcode as their root addresses
- Updated unique ZIP codes to return the correct dpv_match_code from Y when it should be D

## 5.9.34 - 2025-02-18
We are beginning our phased rollout of us-street-api 5.9.34. This process is scheduled to be completed by 2025-02-21 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved DPV Footnote accuracy
- Improved matching for addresses with “COU” in the street name

## 5.9.33 - 2025-01-30
We are beginning our phased rollout of us-street-api 5.9.33. This process is scheduled to be completed by 2025-02-01 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved matching with various kinds of hyphen addresses in enhanced mode.
- Added county_source to strict/invalid modes.
- Fixed county_source for xml inputs.
- Fixed returning urbanization information for PR addresses when using enhanced mode.

## 5.9.32 - 2025-01-28
We are beginning our phased rollout of us-street-api 5.9.32. This process is scheduled to be completed by 2025-01-30 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.
This deploy also has a corresponding us-street-data change to 2025.01.K.

### FIXED
- No longer report rooftop geocodes for invalid post office boxes.
- Various other minor differences and improvements.

## 5.9.31 - 2025-01-22
We are beginning our phased rollout of us-street-api 5.9.31. This process is scheduled to be completed by 2025-01-24 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.
This deploy also has a corresponding us-street-data change to 2025.01.E.

### FIXED
- Better matching for certain types of address variations, including crossing->xing, County Roads, and North East addresses
- Better partial matching for addresses that do not have a primary number
- Various other minor differences and improvements

## 5.9.28 - 2024-12-18
We are beginning our phased rollout of us-street-api 5.9.28. This process is scheduled to be completed by 2024-12-20 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.
This deploy also has a corresponding us-street-data change to 2024.12.G.

### FIXED
- Improved matching on partial addresses and PO boxes.
- Improved matching with certain types of misspellings.

## 5.9.26 - 2024-11-20
We are beginning our phased rollout of us-street-api 5.9.26. This process is scheduled to be completed by 2024-11-23 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Fixed a rare issue where secondary designators were duplicated
- Improved match functionality for inputs with an invalid primary number in enhanced mode.

## 5.9.25 - 2024-11-04
We are beginning our phased rollout of us-street-api 5.9.25. This process is scheduled to be completed by 2024-11-07 00:00:00 UTC. Some customers may notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Fixed an issue where parts of delivery instructions in delivery_line_2 were being erroneously omitted.
- Fixed a rare issue where an incorrect street suffix would be assigned to the returned address.
- Improved detection for PMBs when input doesn't indicate there is a PMB.

## 5.9.24 - 2024-10-24
We are beginning our phased rollout of us-street-api 5.9.24. This process is scheduled to be completed by 2024-10-27 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved PMB handling in delievery_line_1.
- Improved dpv_footnotes relating to PMBs (RR and R1).
- Introduced a new input parameter: county-source=geographic.
  - This will return county information based on the physical location of the address as opposed to the postal county information.

## 5.9.22 - 2024-09-26
We are beginning our phased rollout of us-street-api 5.9.22. This process is scheduled to be completed by 2024-09-29 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Decreased latency for some inputs containing extra/invalid street and street2 information.
- Improved capability to validate input that has poor formatting.

## 5.9.19 - 2024-09-17
We are beginning our phased rollout of us-street-api 5.9.19. This process is scheduled to be completed by 2024-09-20 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Fixed a minor issue involving addresses that include boxes (PO, RR, HC, etc.).

## 5.9.18 - 2024-09-16
We are beginning our phased rollout of us-street-api 5.9.18. This process is scheduled to be completed by 2024-09-19 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved handling of extra secondary components.
- Fixed some mismatches between the components of an address and the delivery_line_1 field.
- Improved handling duplicated secondary info.
- Improved handling of addresses with NE directionals.
- Improved handling of unique zip code addresses that include boxes (PO, RR, HC, etc.).

## 5.9.17 - 2024-08-19
We are beginning our phased rollout of us-street-api 5.9.17. This process is scheduled to be completed by 2024-08-22 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved unique zip code handling for X# address matches.

## 5.9.16 - 2024-08-14
We are beginning our phased rollout of us-street-api 5.9.16. This process is scheduled to be completed by 2024-08-16 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved match functionality for street name in enhanced mode

## 5.9.15 - 2024-07-31
We are beginning our phased rollout of us-street-api 5.9.15. This process is scheduled to be completed by 2024-08-02 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Fixed a rare issue where the secondary number or street suffix was missing from the components fields.

## 5.9.13 - 2024-07-22
We are beginning our phased rollout of us-street-api 5.9.13. This process is scheduled to be completed by 2024-07-24 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved match functionality for inputs with fractions.

## 5.9.12 - 2024-07-10
We are beginning our phased rollout of us-street-api 5.9.12. This process is scheduled to be completed by 2024-07-13 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved matching techniques for addresses within unique ZIP codes.

## 5.9.8 - 2024-06-18

### ADDED
- Return valid components from freeform input containing an invalid primary number in enhanced mode.

## 5.9.7 - 2024-06-13

### FIXED
- Updated Connecticut FIPS compatibility option

## 5.9.6 - 2024-06-12

### FIXED
- Fixed inconsistent USPS county data for Connecticut to reflect the new county data.

## 5.9.5 - 2024-06-11
We are beginning our phased rollout of us-street-api 5.9.5. This process is scheduled to be completed by 2024-06-14 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED
- Improved match functionality for inputs with duplicate values.
- Fixed an issue where missing-secondary and unknown-secondary were missing from the enhanced_match results.
- Improved handling of invalid secondary results.

## 5.9.4 - 2024-05-02
We are beginning our phased rollout of us-street-api 5.9.4. This process is scheduled to be completed by 2024-05-05 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Improved accuracy for the enhanced match field in regards to "missing-secondary" and "unknown-secondary".
- Fixed an issue where the enhanced match field was "none" but a SmartyKey™ was being returned anyways.
- Improved accuracy for A#, B#, and M# footnotes.
- Improved ability to understand certain Spanish inputs.
- Fixed a rare scenario where an inaccurate SmartyKey™ was being returned for an address with a valid secondary.

## 5.9.3 - 2024-04-15
We are beginning our phased rollout of us-street-api 5.9.3. This process is scheduled to be completed by 2024-04-18 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Improved matching capabililty for enhanced match.
- Removed duplicate delivery_line_2.
- Fixed a rare scenario where the SmartyKey™ for a root address was being assigned to a secondary address.
- Fixed an issue where enhanced_match field would fail to label unknown secondaries.
- Stop removing apostrophes from Addressee field.
- Fixed an issue where duplicate PMB's would fail to validate.
- Fixed an issue where the enhanced_match field was incorrect for some unique zipcodes.
- Fixed an issue where enhanced_match field said "none" but an address was matched.

## 5.9.1 - 2024-03-13
We are beginning our phased rollout of us-street-api 5.9.1. This process is scheduled to be completed by 2024-03-16 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### CHANGED

- Utilizing new AI or machine learning algorithms to improve the results for enhanced match.

## 5.8.4 - 2024-03-07
We are beginning our phased rollout of us-street-api 5.8.4. This process is scheduled to be completed by 2024-03-12 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Fixed an issue where there was a contradiction between enhanced_match and DPVFootnotes.
- Improved ability to find SmartyKey™ when secondary is invalid.
- Improved ability to find results that use the street2 field.
- Fixed an issue where duplicate PMB values would be returned.
- Fixed the inconsistency between strict, invalid, and enhanced mode for the A# and B# footnotes.
- Improved matching on PO boxes with dual input.

## 5.8.2 - 2024-02-28
We are beginning our phased rollout of us-street-api 5.8.2. This process is scheduled to be completed by 2024-03-02 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Fixed an issue where inputting a PO box in street2 would yield an incorrect SmartyKey™.
- Fixed a rare issue where non-postals would yield an incorrect SmartyKey™.
- Fixed a rare issue where results were given an incorrect SmartyKey™
- Fixed an issue where an incorrect SmartyKey™ was being returned when multiple results were being returned.
- Fixed an issue where incorrect footnotes were being returned when multiple results were being returned.
- Improved the ordering footnotes are returned in.
- Improved the accuracy of the enhanced_match field.

## 5.7.38 - 2024-02-05

### DEPRECATED

- Officially removed support for JSONP.

## 5.7.37 - 2024-01-25
We are beginning our phased rollout of us-street-api 5.7.37. This process is scheduled to be completed by 2024-01-27 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Fixed an issue where some malformed PO boxes would cause empty results to return.

## 5.7.35 - 2024-01-25
We are beginning our phased rollout of us-street-api 5.7.35. This process is scheduled to be completed by 2024-01-27 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Improved PO box validation.
- Improved handling of results when input city is ambiguous.
- Fixed a rare case where empty results were being returned when a hyphen was in the input primary.

## 5.7.31 - 2024-1-3
We are beginning our phased rollout of us-street-api 5.7.31. This process is scheduled to be completed by 2024-01-04 00:00:00 UTC.

### FIXED

- Improved internal input validation. 

## 5.7.30 - 2023-12-20
We are beginning our phased rollout of us-street-api 5.7.30. This process is scheduled to be completed by 2023-12-22 00:00:00 UTC.

### FIXED

- Improved internal geocode processes.
- More accurate rooftop geocodes.
- Better address results for non-postal addresses.

#### 2023.12.G - Add-on Data 

On-Premise builds will require updated data which will be available after the cloud roll out is completed.

- Removed some invalid non-postal addresses.
- Updated and enhanced geocode precision.

## 5.7.29 - 2023-12-14
We are beginning our phased rollout of us-street-api 5.7.29. This process is scheduled to be completed by 2023-12-19 00:00:00 UTC. Some customers might notice slightly inconsistent results between subsequent calls for the same inputs. This is expected behavior.

### FIXED

- Fixed an issue with duplicated output.
- Improved handling of secondary values.
- Improved footnote accuracy.
- Improved performance for enhanced mode.
- Fixed incorrect address being returned in some cases.
- Improved PO Box validation.

## 5.7.27 - 2023-12-06

### FIXED

- Improved accuracy and matching capability for the city field.

## 5.7.24 - 2023-12-01

### FIXED

- Fixed a rare issue where erroneous results were being returned.

## 5.7.23 - 2023-11-8

### FIXED

- Fixed an issue where an improperly used dash would return no results
- Fixed a rare issue with extra spaces in some secondaries
- Fixed inconsistent results when the street field is empty but street2 contains valid data

### DEPRECATED

- JSONP is officially deprecated.  Support will be removed for JSONP starting on January 31, 2024.

## 5.7.19 - 2023-10-31
- Added Project US@ formatting option, for more information on Project US@ see https://www.smarty.com/articles/project-usa-address-standardization

## 5.7.16 - 2023-10-11
- Improved PMB handling

## 5.7.15 - 2023-10-02
- Improved SmartyKey accuracy

## 5.7.12 - 2023-09-25
- Fixed a rare issue where an incorrect empty result was being returned.

## 5.7.11 - 2023-09-19
- Fixed an issue where an odd secondary combination would cause results to not return correctly.

## 5.7.10 - 2023-09-13
- Fixed an internal issue that will not affect address results.

## 5.7.8 - 2023-08-18
- Fixed two rare validation input cases.

## 5.7.7 - 2023-08-15
  - Fixed issue where a specific 10 digit input pattern in street/street2 could return an error.

## 5.7.6 - 2023-08-10
Enhanced Match Improvements:
  - Fixed multiple false positive issues.
  - Fixed issue where input in street2 field occasionally returned odd results.
  - Fixed issue where M.L.K was not being recognized as a valid street.
  - Fixed issue where a duplicate PMB value was being copied into the primary number as well as PMB number field.
  - Fixed issue where some odd secondaries were being corrected erroneously.
  - Improved handling of some addresses with odd secondaries.
  - Improved capability to differentiate between street suffixes and street names.

## 5.7.2 - 2023-08-02
  - Includes a fix for when "via" or "plaza" was not being recognized.
  - Internal code optimizations.

## 5.7.1 - 2023-07-19
CHANGES:
  - Implemented USPS Cycle "O", the most notable change affects dpv_footnotes.
  - Of particular note, the meaning of the "CC" and "N1" dpv_footnotes are being revised.
  - For more information see https://www.smarty.com/docs/usps-cycle-o and https://www.smarty.com/docs/cloud/us-street-api#analysis

KNOWN ISSUES:
  - USPS has confirmed an issue in the July Cycle "O" release where some street names beginning with words such as "via" or "plaza" may not be found unless you leave those words out.
  - A fix will be available in the August data release.

## 5.6.1 - 2023-06-30
- Internal code optimizations.

## 5.6.0 - 2023-06-29
- Made smarty_key available for enhanced matching (cloud version).  

## 5.5.10 - 2023-06-23
- Fixed a minor JSONP issue where an extra header was being checked for JSONP.

## 5.5.9 - 2023-06-22
- Fixed some cases where PMB was not being returned correctly.
- Fixed issue where enhanced_match would sometimes display "none" instead of "postal-match".
- Fixed issue where Unique Zip Codes were not behaving as expected and in some cases an incorrect match was being made.

## 5.5.7 - 2023-05-05

- Fixed JSONP


## 5.5.6 - 2023-05-04

- Fixed HTTP 404 issues that would occur when a trailing slash was used at the end of the route in the URL such as https://us-street.api.smartystreets.com/street-address/?...
- Fixed HTTP 406 issues that would occur if all values in the Accept header were not supported. It will now default to return JSON in that case.
- Fixed an issue when making an API call in a web browser where it would return XML instead of JSON. 


## 5.5.1 - 2023-05-01

On-Premise customers should see documentation updates (https://www.smarty.com/docs/local/us-street-api#manage) as there are changes in the way the program is launched.

- Restructured source code to improve performance.
- Enhanced error messages which are returned as JSON with additional information.
- Geocodes are now rounded to the 6th decimal place instead of being truncated to the 6th.
- Fixed an issue where no results would be found if street2 was populated but street was not.


## 5.4.1 - 2023-04-14 - 2023-04-17

NOTE: This version will be released over the dates above.

On-Premise builds will require updated data which will be available after the cloud roll out is completed.

CHANGES:
- Enhanced accuracy and availability of geocodes.
- Improved secondary matches in enhanced mode.
- Internal code changes to prepare for upcoming features.

BUG FIXES:
- Fixed enhanced_match flag issue with strict and invalid mode when submitting batches.

## 5.3.6 - 2023-03-21

- Small internal changes regarding plans and subscriptions to interpret appropriate features of a customer request.
- Compiled using Go v1.19.7.

## 5.3.4 - 2022-01-26

CHANGES:
- Added CPR to CMR to support new data changes.
- Improved search capabilities for some alternate cities.

BUG FIXES:
- Resolved issue with outputs when secondaries were submitted in the 'street2' field.
- Resolved issues with specific key-words being dropped.

## 5.3.3 - 2022-12-08

CHANGES:

- Internal restructuring, no external changes.


## 5.3.2 - 2022-12-03

BUG FIXES:

- Fixed minor issue where a specific string combination would cause the request to fail.

## 5.3.1 - 2022-12-01

CHANGES:

Enhanced Mode Improvements:
- Significant improvements to footnotes analysis.
- Minor enhancement for misspelled street names.
- Minor improvement to match rates for addresses with similar street names.

## 5.3.0 - 2022-10-26

CHANGES:

Enhanced Mode Improvements:
- Improved match rates.
- Field enhanced_match is now consistently populated in the returned results.
- Field enhanced_match contains "ignored-input" parameter when input is not used to obtain a match.
- HC and HCR address matching has been improved.
- dpv_footnotes and footnotes are more consistent.
- Significant improvements to invalid secondaries.
- Improved matches for valid secondaries.


## 5.2.1 - 2022-09-28

## 5.2.2 - 2022-10-04

CHANGES:

- Compiled against Go v1.19.1
- Improved invalid secondary detection with hyphens in enhanced mode


## 5.2.1 - 2022-09-28

CHANGES:

- Fixed issue with invalid secondaries combining incorrectly across addresses in enhanced mode.
- Improved invalid secondary detection in enhanced mode.


## 5.2.0 - 2022-08-31

CHANGES:

- Improved speed and accuracy in enhanced mode.
- Improved primary number handling in enhanced mode.


## 5.1.1 - 2022-07-19

CHANGES:

- Compiled against Go v1.18.4.
- Upgrade to latest dependencies.
- Enhance geocode precision in very rare correction cases (cloud version).
- Internal update to DNS handling (cloud version).


## 5.0.31 - 2022-06-09

CHANGES:

- Compiled against Go v1.18.3.
- Increased load speed for local version.
- Improved street2 field recognition in enhanced mode.
- Improved secondary handling in enhanced mode.
- Improved match rates in enhanced mode.
- Improved spelling corrections in enhanced mode.


## 5.0.28 - 2022-05-04

CHANGES:
- Internal restructuring.
- Invalid secondary handling improvements for enhanced mode.

## 5.0.27 - 2022-03-23

CHANGES:

- Compiled against Go v1.17.8.
- Upgrade to latest dependencies.
- Internal restructuring, no external changes.

## 5.0.25 - 2022-02-22

CHANGES:

Enhanced Mode:
- Improved accuracy of analysis flags.
- Improved accuracy for addresses containing hyphens.
- Improved accuracy for ambiguous addresses.
- Improved accuracy for addresses containing Highways and "Heights".
- Improved accuracy when invalid zip codes are detected as input.
- Improved invalid secondary handling.

## 5.0.22 - 2021-12-6

CHANGES:

- Increased match accuracy for invalid zip codes in enhanced mode.
- Increased match accuracy for batched addresses in enhanced mode.

BUG FIXES:

- Fixed issue with invalid secondaries producing incorrect results.

## 5.0.21 - 2021-10-27

CHANGES:

- DPVMatchCode is no longer cleared in enhanced mode.
- Increased match accuracy for enhanced mode.
- Updated "enhanced" data format for local version; a new download of the "enhanced" data is required.

BUG FIXES:

- Fixed an instance where a secondary component field could be duplicated in the result under enhanced mode with non-postal data.

## 5.0.20 - 2021-08-31

CHANGES:

- Updated component input results to be more consistent with freeform input results in enhanced mode.
- Expanded multiple candidate support in enhanced mode.

BUG FIXES:

- Fixed instances where a secondary component field could be duplicated in the result under enhanced mode.

## 5.0.16 - 2021-08-12

BUG FIXES:

- Resolved issue where some queries would not return consistent results.

## 5.0.14 - 2021-08-11

BUG FIXES:

- Fix empty response for specific mangled address pattern.

## 5.0.12 - 2021-08-03

CHANGES:

- Changes to enhanced mode to eliminate some false positive results.
- Several internal changes that do not affect the user experience.  
- Provided enhanced mode for local installations (does not affect cloud environment). 

## 5.0.7 - 2021-07-14

BUG FIXES:

- In enhanced mode, a DPV match code might not have been returned in some circumstances when the match was a valid USPS address.

## 5.0.6 - 2021-07-13

In this major version release, new features are exposed via new `match` options (see [documentation](https://www.smarty.com/docs/cloud/us-street-api#input-fields)). The input/output contracts for existing features are preserved.

CHANGES:

- Release enhanced match mode and non-postal address features for cloud environments.

## 4.8.7 - 2021-05-14

BUG FIXES:

- Fixed segfault for certain startup error messages on local install.

## 4.8.6 - 2021-04-26

CHANGES:

- Updated internal metric instrumentation.

## 4.8.3 - 2021-03-05

BUG FIXES:

- Fixed issue with RDI data not being returned correctly in some cases.

## 4.8.2 - 2021-03-03

BUG FIXES:

- Fixed logging issue during spelling correction.

## 4.8.0 - 2021-02-17

CHANGES:

- Added output field: dpv_no_stat. This is a specialized field that should only be used by those who understand what it means.

## 4.7.3 - 2021-02-02

BUG FIXES:

- Fixed an issue with the on-premise binary. This did not affect cloud functionality.

## 4.7.2 - 2021-01-27

CHANGES:

- Corrected local install to not try to load unexpected data files.
- Internal restructure to better support reporting process speed to supports SLAs in hosted, cloud environment.

## 4.6.0 - 2020-11-23

CHANGES:

- Upgraded address processing engine to latest version.

- The `active` field in the `analysis` structure of the result candidate will
now always return "Y" to indicate active. In previous releases we were too
aggressive about showing a potential address as not active which could,
depending upon client processing logic, result in a perfectly valid and active
address from being utilized.


## 4.5.4 - 2020-10-29

CHANGES:

- Internal restructuring, no external changes.


## 4.5.3 - 2020-10-26

CHANGES:

- Latest dependencies.
- More attempts to geocode an address.


## 4.5.2 - 2020-10-16

CHANGES:

- Using earlier version of shared library which doesn't segfault on malformed input.
- Improved initialization speed with concurrency.


## 4.5.1 - 2020-10-15

CHANGES:

- Increased diagnostic message verbosity on failure.
- New diagnostic message regarding required number file descriptors.


## 4.5.0 - 2020-10-14

CHANGES:

- Internal structural changes.
- Removed dynamic geocoding corrections in favor of daily rotation.
- Wireup more tolerant of optional files.

## 4.4.1 - 2020-09-30

CHANGES:

- Compiled using Go v1.15.x.
- Internal structural changes.


## 4.4.0 - 2020-09-09

CHANGES:

- New `coordinate_license` field in response to give attribution as well as indicate any restrictions that may exist relative to the geocode coordinate being returned.


## 4.3.13 - 2020-08-21

CHANGES:

- Internal structural changes


## 4.3.5 - 2020-08-11

CHANGES:

- Set upper limit on number of workers for machines with high numbers of CPU cores.


## 4.3.2 - 2020-08-03

CHANGES:

- Better internal error checking surrounding geocoding.


## 4.3.1 - 2020-08-03

CHANGES:

- Internal handling of feature flags.


## 4.3.0 - 2020-07-31

CHANGES:

- Upgrade to latest dependencies
- Small internal improvements in preparation for soon-to-be-released features.


## 4.2.4 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.


## 4.2.3 - 2020-06-10

CHANGES:

- Compiled against Go v1.14.4.
- Adjusted internal metrics reporting frequency.

## 4.2.2 - 2020-05-28

CHANGES:

- Compiled against Go v1.14.3.
- Includes the new usps/ams libraries.

## 4.2.1 - 2020-05-05

CHANGES:

- Internal behavior surrounding subscription management.


## 4.2.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 4.1.1 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.1.0 - 2020-03-24

CHANGES:

- Internal packaging and dependency management.


## 4.0.30 - 2020-03-17

BUG FIXES:

- Corrected concurrent access bug that caused intermittent geocode inaccuracies.


## 4.0.29 - 2020-03-16

CHANGES:

- Latest internal dependencies.


## 4.0.28 - 2020-03-13

CHANGES:

- Replace common misspellings in street input field

## 4.0.27 - 2019-12-20

CHANGES:

- Internal refactoring 


## 4.0.26 - 2019-12-19

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.


## 4.0.21 - 2019-10-22

CHANGES:

- Latest version of internal dependencies.


## 4.0.20 - 2019-10-17

CHANGES:

- Refined certain log messages and updated to latest internal dependencies.


## 4.0.19 - 2019-09-18

CHANGES:

- Better handling of freeform inputs with stray punctuation.


## 4.0.18 - 2019-09-06

CHANGES:

- Internal refactoring.


## 4.0.17 - 2019-09-06

CHANGES:

- Latest version of internal, upstream dependencies.


## 4.0.16 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.


## 4.0.15 - 2019-08-02

CHANGES:

- Latest internal dependencies.


## 4.0.14 - 2019-07-26

CHANGES:

- Slight change to internal boilerplate code used in development and testing.


## 4.0.12 - 2019-07-26

CHANGES:

- Latest internal dependencies.


## 4.0.11 - 2019-07-26 [YANKED: cloud installation]

BUG FIXES:

- Reinstated top-level /lib folder into the local installation package (required reworking much of the source code boilerplate).

CHANGES:

- Internal refactoring.
 

## 4.0.10 - 2019-07-12 [YANKED: local installation]

BUG FIXES:

- Corrected mishandling of lookups that contain no street information, introduced in the 4.0.0 release.


## 4.0.7 - 2019-07-09 [YANKED: local installation]

BUG FIXES:

- With the 4.0.0 release a concurrency-related bug was introduced in a hash calculation which caused the application to panic and shut down. (See incident details: https://status.smarty.com/incidents/dk5ghfl03vjf) This release fixes that issue.


## 4.0.0 - 2019-07-01 [YANKED]

This release, while a major version release represents a merging of internal code repositories and does not introduce any changes to the input/output contracts [as currently documented](https://www.smarty.com/docs/cloud/us-street-api).

CHANGES:

- Local installations can now make use of up to 64 cores (previously the max was 8).
- Local installations should log slow status check durations less frequently (when applicable).
- Local installations no longer limit the size of request payloads. 
- Clients of local installations must now submit a `Content-Type` header with `application/json; charset=utf-8` for `JSON` payloads. Failure to do so will result in `HTTP 400 Malformed Request`.
    - One option would be to put the local installation behind your own proxy that performs an override in the case of certain common content types submitted by tools such as cURL (`x-www-formurlencoded` to `application/json; charset=utf-8`).

## 3.3.2 - 2019-06-24

- Updated internal dependencies. Incrementing the minor version number in this case was a mistake.


## 3.2.22 - 2019-04-30

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.27 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.26 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.25 - 2019-03-08

CHANGES:
- Internal refactoring.


## 3.0.24 - 2019-03-06

IMPROVEMENTS:

- Updated internal dependencies.
- Compiled using Go v1.12.

CHANGES:

- Overhauling module and deployment system. (No public-facing changes expected.)


## 3.0.23 - 2019-02-22

IMPROVEMENTS:

- Freeform inputs containing underscores (instead of spaces) will be sanitized and handled correctly.
- Updated all internal dependencies to latest versions.

BUG FIXES:

- Wireup race condition fixed in inner verification engine.


## 3.0.22 - 2018-11-29

IMPROVEMENTS:

- Latest internal dependencies


## 3.0.21 - 2018-11-29

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
