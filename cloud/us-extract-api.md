# Changelog - [US Extract API](https://www.smarty.com/docs/cloud/us-extract-api)

All notable changes to the US Extract API will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 3.14.7 2022-08-24

CHANGES:

- Fixed an issue for local customers where some local instances of us-street would not work. Error: EOF


## 3.14.6 2022-08-22

CHANGES:

- Removed some messages printed on the console.


## 3.14.4 2022-08-18

CHANGES:

- Go v1.18.4
- Fixed an issue with hyphens in the primary number.
- Any communication errors to US Street will be reported to the client.


## 3.13.0 2022-06-10

CHANGES:

- Allow patch to config.json upon startup using -config


## 3.12.2 2022-05-23

CHANGES:

- Compiled using Go v1.18.x.
- Update internal logging of parsing failures.

## 3.12.1 2022-05-20

CHANGES:

- Latest dependencies.
- Update internal logging of upstream validation failures.

## 3.12.0 2022-05-11

CHANGES:

- When the upstream validation service returns a rate limited response (HTTP 429), it will be passed on in the client response.
- For local installations:
  - The executable binary is now statically compiled and no longer depends on `libc` or `libpcre` dynamic modules.
  - If upstream validation fails, a `[WARN]` message is logged by the application.
  - Added command line option descriptions under `-help`.
  - Added command line option `-license` for when a single `auth-id` has multiple us address licenses.

BUG FIXES:
 
- For local installations:
  - Fix where `-auth-id` and `-auth-token` options on the command line could have been ignored.
	

## 3.11.15 2022-04-07

CHANGES:

- Code refactor. Nothing was changed that would modify the user experience.


## 3.11.14 2022-03-24

CHANGES:

- Fix issue with candidate processing that could cause a server panic.
- Internal code refactor to improve reliability and stability.


## 3.11.10 2022-03-09

CHANGES:

- Go v1.17.8
- Ensuring all arguments are fully reset on each HTTP invocation to prevent cross-talk between requests.

## 3.11.3 2022-03-02

CHANGES:

- Internal packaging to ensure binaries for local installation are available.

## 3.11.0 2022-03-02

CHANGES:

- Latest dependencies.
- Go v1.17.7
- Completely overhauled internal structure.

## 3.8.3 2021-04-01

CHANGES:

- Latest dependencies.
- Better diagnostic logging of upstream errors.
- Overhauled build packaging.

## 3.7.0 2020-09-30

CHANGES:

- Compiled using Go v1.15.x.
- Full support for the [`license` query string parameter](https://www.smarty.com/docs/cloud/licensing).


## 3.5.1 - 2020-08-25

CHANGES:

- Incorporate latest version of the Smarty Go SDK (v1.6.2) which adds support for calling a local instance of the US Street API hosted behind a non-blank path in its address.


## 3.5.0 - 2020-06-30

CHANGES:

- Internal upgrades to messaging infrastructure.


## 3.4.4 - 2020-06-12

CHANGES:

- Upgrade to latest dependencies
- Updated packaging instructions for on-premise builds.
- Compiled using Go v1.14.x.


## 3.4.1 - 2020-05-05

CHANGES:

- Internal behavior surrounding subscription management.


## 3.4.0 - 2020-04-13

CHANGES:

- Updated packaging instructions for on-premise builds.


## 3.3.1 - 2020-03-16

CHANGES:

- Latest internal dependencies.

## 3.3.1 - 2019-12-20

CHANGES:

- Internal refactorings and simplifications.
- Emitting additional data points for internal business intelligence.
- Local Installations Only:
	- It is now required that clients send requests with `Content-Type` of `text/plain; charset=utf-8`. Failure to do so may result in `HTTP 400 Bad Request`.
	- The server no longer limits the size of the request body or provides CORS response headers. If desired, this is now the responsibility of the organization hosting the local installation.


## 3.3.0 - 2019-09-06

CHANGES:

- Additional configuration values for cloud version to make downstream URL dynamic.
- Latest dependencies.

## 3.2.4 - 2019-08-16

CHANGES:

- Reworking build/publish boilerplate.


## 3.2.3 - 2019-08-16 [YANKED]

CHANGES:

- Reworking build/publish boilerplate.


## 3.2.2 - 2019-08-16

CHANGES:

- Compiling using Go v1.12.9 to address various potential CVEs found in standard library for HTTP/2.

## 3.1.13 - 2019-04-18

- Rolled back changes introduced in 3.1.12 once issue was identified.


## 3.1.12 - 2019-04-18

- Includes additional http tracing to help debug an issue in production. (https://status.smarty.com/incidents/6052sfzh0xhh)


## 3.1.11 - 2019-04-04

CHANGES:

- Now compiled with Go 1.12 and Go modules.
- The service now runs in a docker image and has been fully migrated to geo-distributed kubernetes clusters.

NOTES:

- While this is a minor version release, there are no additional behaviors or features in this release.


## 3.0.5 - 2019-03-26

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.4 - 2019-03-25

CHANGES:
- Internal refactoring relative to message routing.


## 3.0.3 - 2019-03-08

IMPROVEMENTS:
- Internal refactoring.

## 3.0.2 - 2019-03-06

IMPROVEMENTS:

- Overhauling module and deployment system. (No public-facing changes expected.)
- Updated internal dependencies.
- Compiled using Go v1.12.


## 3.0.1 - 2018-07-03

CHANGES:

- Final cleanup related to 3.0.0 release. Mostly just removed unneeded packaging declarations.


## 3.0.0 - 2018-07-03

CHANGES:

- Separated all authentication and authorization checkpoints to separate process, greatly slimming down wireup and configuration.
