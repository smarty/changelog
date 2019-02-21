# Changelog - [US Street Address API](https://smartystreets.com/docs/cloud/us-street-api)

All notable changes to the US Street Address API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## Unreleased

Changes:

- Overhauling module and deployment system. (No public-facing changes expected.)
- Freeform inputs containing underscores (instead of spaces) will be handled correctly.


## 3.0.22 - 2018-11-29

IMPROVEMENTS:

- Latest internal dependencies


## 3.0.21 - 2018-11-29

BUG FIXES:

- Fixed county output in scenario categorized by a plus 4 code that crosses over a state line into a county with a FIPS code that matches the FIPS code of an unrelated county in the default state. Previously, the output contained county info pertaining to the unrelated county from the default state rather than the correct county in the adjoining state.
