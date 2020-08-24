# [SmartyList CLI](https://smartystreets.com/docs/plugins/smartylist/cli)


## 8.4.1 - 2020-?

BUG FIXES:

- Ensured the `-version` flag correctly displays the version.


## 8.4.0 - 2020-0?

CHANGES:

- Deprecated `-licenses` flag from 8.3.0, in favor of `-license` (singular). This flag may be supplied multiple times to specify multiple values. Most users need not supply this flag.


## 8.3.0 - 2020-08-14

CHANGES:

- Added `-licenses` command line flag. This flag is useful when targeting specific capabilities of an API based on your subscription level. See the documentation for possible values. Most users need not supply this flag.


## 8.2.7 - 2020-01-15

CHANGES:

- Now compiled with Go 1.13
- Better handling of progress bar in error scenarios
- Corrected documentation URL in `DO-NOT-README.txt`: https://smartystreets.com/docs/plugins/smartylist/cli


## 8.2.6 - 2019-06-13

CHANGES:

- The record count displayed on the final processing report is now formatted with thousands separators (,).


## 8.2.5 - 2019-06-13

CHANGES:

- Using [latest SmartyStreets Go SDK](https://github.com/smartystreets/smartystreets-go-sdk/commit/615b3d80a5cbde61385c68bc55c8a217ce0ccb93) which has better support for disabling http2 (see version 8.2.4).

## 8.2.4 - 2019-06-11

BUG FIXES:

- Prevented the application from hanging in the case that a request/batch fails even after configured retries.

CHANGES:

- Many users reported errors which seem to be related to the http2 protocol (which go now supports by default). Until further notice this application will downgrade all requests to http 1.1.


## 8.2.3 - 2019-06-04

CHANGES:

- Using latest dependencies.


## 8.2.2 - 2019-05-01

CHANGES:

- The pre-processing analysis view no longer reports the size of the input file.
- The in-process progress bar has been replaced with a simpler reporting mechanism which shows `lookups completed / total lookups (completed %)`.


## 8.2.0 - 2019-04-30

CHANGES:

- Now compiled with Go 1.12 and go modules.
- Reworked packaging and publishing process.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 8.1.20 - 2019-02-15

CHANGES:

- The changelog document included with all downloads of the SmartyList CLI now just references this document
- The sample input file that is included with all downloads of the SmartyList CLI has column headers that are more aligned with [published documentation](https://smartystreets.com/docs/plugins/smartylist/cli#input).


## 8.1.19 - 2018-12-07

BUG FIXES:

- Corrected initial prompt, which was reporting '0' as the number of expected lookups to be used. This bug was introduced with version 8.1.18.


## 8.1.18 - 2018-12-06

IMPROVEMENTS:

- Changed ordering of file analysis such that large files with invalid headers are rejected much faster.


## 8.1.17 - 2018-09-26

IMPROVEMENTS:

- Estimated lookup count in analysis prompt now displayed using a comma as the thousands separator.
- Small formatting tweaks to progress bar display.
- Upgraded internal dependencies to latest versions.
- Dependencies managed using [go modules](https://github.com/golang/go/wiki/Modules) rather than [dep](https://github.com/golang/dep).
- Now compiled using [Go 1.11](https://blog.golang.org/go1.11).


## 8.1.16 - 2018-05-17

BUG FIXES:

- Updated csv test to use valid delimiter value (see https://golang.org/doc/go1.10#encoding/csv).


## 8.1.15 - 2018-05-17

NOTE: This version was never actually published because of a test failure during the build process. The failure is addressed by version 8.1.16.

IMPROVEMENTS:

- Usage of smart-quotes (and their ilk) as quotation characters in command line flags now results in a fatal error.
- Now compiled with Go 1.10.2


## 8.1.14 - 2018-03-28

IMPROVEMENTS:

- Code cleanup
- Now compiled with Go 1.9.4


## 8.1.13 - 2017-12-18

IMPROVEMENTS:

- Simplified internal build tasks (streamlined for go 1.9).
- Now compiled with Go 1.9


## 8.1.12 - 2017-12-18

IMPROVEMENTS:

- Updated internal dependencies.


## 8.1.11 - 2017-08-28

IMPROVEMENTS:

- Now using the [dep](https://github.com/golang/dep) tool for managing source code dependencies.


## 8.1.10 - 2017-08-15

IMPROVEMENTS:

- Upgraded internal and open-source dependencies.


## 8.1.9 - 2017-07-31

IMPROVEMENTS:

- Added new DPV footnotes supplied by US Street API and their definitions:

    "PB": "PO Box Street Address"
    "R7": "Phantom Address"


## 8.1.8 - 2017-05-11

IMPROVEMENTS:

- Corrected the handling of the UTF-8 byte-order mark (https://en.wikipedia.org/wiki/Byte_order_mark). Without this fix, lists that contained a UTF-8 byte order mark and whose first column was the 'street' field could not be analyzed or processed because the required 'street' field was not recognized.


## 8.1.7 - 2017-05-04

IMPROVEMENTS:

- Internal refactorings and improvements. May the 4th be with you...always.


## 8.1.6 - 2017-01-27

FEATURES:

- Summary text is now "No Match - PO Box Only" for records whose `metadata.zip_type` is "PO Box" (`P`).


## 8.1.5 - 2016-12-08

IMPROVEMENTS:

- Internal optimizations.


## 8.1.4 - 2016-11-30

IMPROVEMENTS:

- Internal optimizations.


## 8.1.3 - 2016-11-17

IMPROVEMENTS:

- We've installed more verbose HTTP request tracing in error scenarios. This is in response to several recent
reports from users of intermittent timeouts and stalls and have been very tricky to reproduce. These seem to
be related to the network connections with our API servers, not the SmartyList tool itself. If your list
fails, please send the log file associated with that processing attempt to help us diagnose the problem.


## 8.1.2 - 2016-11-11

BUG FIXES:

- Log file path can now be specified at the command line with the -log flag. We no longer display the -proxy and -base-url values in the list analysis if defaults are used.


## 8.1.1 - 2016-11-02

IMPROVEMENTS:

- Increased HTTP timeout and retry parameters.


## 8.1.0 - 2016-10-31

FEATURES:

- New command-line flag: -proxy (Allows lists to be processed via an organization's web proxy.)


## 8.0.4 - 2016-10-27

UPGRADE NOTES:

- Failure by the smartylist tool to ascertain the latest version is grounds for early termination of the
program and a non-zero exit code. So there.


## 8.0.3 - 2016-10-17

IMPROVEMENTS:

- Modified the output for addresses that completely fail verification that also have a "Unique" ZIP codes.


## 8.0.2 - 2016-10-10

IMPROVEMENTS:

- Using the latest version of the smartystreets-go-sdk: 5.0.1 (which correctly buffers the request body for retry)


## 8.0.1 - 2016-10-06

BUG FIXES:

- Prevent double url-encoding of auth-token



## 8.0.0 - 2016-10-04

FEATURES:

1. JSON configuration files: Support for JSON config files is being dropped. The 'config'
command line flag will be removed. (For those wishing to avoid the auth-id and auth-token
values showing up in process lists those flags may be populated with the names of environment
variables containing the actual auth values.)

2. Schema: Support for the the 'zipcode' schema is being dropped. The 'address' schema is now
the only supported mode of operation. The 'schema' command line flag will be removed.

3. Batches: Support for customizing the number of concurrent bathes is being dropped as the
smartylist tool now uses the maximum number of batches by default. The 'batches' command line
flag will be removed.

4. Hostname: Support for customizing the hostname is being dropped. The 'hostname' command line
flag will be removed. (The base-url flag has been the preferred method of pointing to alternate
endpoints and will continue to be supported.)

5. Verbosity: The verbose and debug flags have been replaced by a single new flag: 'silent'. If
set, no output or prompts will be presented. The 'verbose' and 'debug' command line flags will
be removed.


In this version of smartylist, all configuration and options will be provided via the following
command-line flags (this is the same listing provided by 'smartylist -help'):

  -auth-id
    	The auth-id value (or name of environment variable) to use for API requests.
  -auth-token
    	The auth-token value (or name of environment variable) to use for API requests.
  -base-url
    	The base URL to use for API requests.
    	Unless you are pointing to an onsite API installation or a proxy the default value is appropriate.
    	Default: [https://api.smartystreets.com]
  -input
    	The path to the input file with records to verify/lookup. (REQUIRED)
  -log
    	The path to the diagnostic log file.
    	Default: [log_<datetime>.txt]
  -output
    	The path to the output file to create.
    	Default: [<input-filename>-output.<input-extension>]
  -silent
    	Squelch all diagnostic output and process list without confirmation prompt if possible.
  -version
    	Show the version and exit.


## 7.0.0 - 2016-08-29

FEATURES:

- This version served as an intermediate version between 6.0.0 and 8.0.0. No new processing
behavior was released. The only change in this version was the addition of a series of
informational prompts warning the user of the changes listed below in version 8.0.0.

