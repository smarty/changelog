# Changelog - [US Autocomplete API (V2)](https://www.smarty.com/docs/cloud/us-autocomplete-api)

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
All notable changes to the US Autocomplete API will be documented in this file.

## Important Note:
`US Autocomplete Basic` has been deprecated.
This API is accessed with the following URL: `us-autocomplete.api.smarty.com/suggest`
We suggest you contact Smarty support for assistance in migrating to `US Autocomplete V2`.

`US Autocomplete Pro` has been updated to `US Autocomplete V2`.
That API is accessed with the following URL: `us-autocomplete-pro.api.smarty.com/lookup`
We suggest you contact Smarty support for assistance in migrating to `US Autocomplete V2`.

## 1.0.33 - 2026-07-08
- To be deployed throughout the day.
- New data: `2026.07.P` (based on 2026.07.B with new stuff below)
- `urbanization` support during search for Puerto Rico addresses.
- `urbanizaiton` is returned in the result in "v2" mode.
- New enhanced filter in v2 mode: `undeliverable-base-address` to filter out undeliverable `AAN1` base addresses.

## 1.0.30 - 2026-06-26
- Fixed an issue where smarty_key would not be returned on results containing an alternate city. 

## 1.0.29 - 2026-06-18
- Internal changes that will not affect the customer experience. 

## 1.0.28 - 2026-06-05
- Prevent inputted commas from obscuring matches 
- Allow fully spelled-out ordinals (first through tenth) to match their numeric equivalents, and vice versa
- Allow primaries with a hyphen to be typed without one, and vice versa
- Prevent PO Box results from being returned when search term does not start with PO Box (in all of its forms) 
- Improve performance by automatically removing preferences that conflict with the filters.

## 1.0.27 - 2026-05-28
- Performance enhancements

## 1.0.26 - 2026-05-27
- Performance enhancements
- Reduce noisy results that do not appear to fit the input
- Fix a bug that could cause a panic

## 1.0.23 - 2026-05-19
- Internal maintenance

## 1.0.22 - 2026-05-07
- Deploying the new US Autocomplete V2, the next generation of US Autocomplete.
- This will be a gradual deploy from May 7 through May 11.
- V2 is compatible with US Autocomplete Pro calls so no code needs to be modified.
- New V2 features will be available starting May 12.
