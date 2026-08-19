# Changelog - Smarty MCP

All notable changes to the Smarty MCP Server will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 1.9.0 - 2026-08-05

### CHANGED
- The server now operates statelessly: no server-side sessions or initialization handshake are required between requests.
- `server/discover` is exempt from authentication, alongside the legacy handshake methods.
- Upgraded `modelcontextprotocol/go-sdk` to v1.7.0.

## 1.8.1 - 2026-07-15

### FIXED
- Upstream Smarty API calls are now bounded by a 50-second timeout (including SDK retry sleeps), so a slow upstream call no longer holds a pooled client indefinitely.
- Invalid connection pool retry configuration is rejected at startup with an error instead of panicking; `POOL_RETRIES=0` is now accepted.

## 1.8.0 - 2026-07-13

### FIXED
- Enrichment "Not Modified" (304) responses now conform to the tool output schema and are correctly distinguished from results that changed to empty.

### CHANGED
- Updated Go toolchain to 1.26.5 and `smartystreets-go-sdk` to v1.39.0.

## 1.7.0 - 2026-06-20

### ADDED
- Business name search for `US_Business_Summary_Components`: look up business data by `business_name` plus city/state/ZIP.

### CHANGED
- Updated Go toolchain to 1.26.4 and dependencies.

## 1.6.1 - 2026-05-14

### FIXED
- Publish release artifacts to the production data GCS bucket.

## 1.6.0 - 2026-05-13

### ADDED
- `US_Address` and `US_Address_Bulk` now accept parsed address component fields in addition to freeform input.

## 1.5.0 - 2026-05-11

### ADDED
- Support for Consul service URLs.

### CHANGED
- Updated Go toolchain to 1.26.3.

## 1.4.0 - 2026-05-05

### ADDED
- `max_candidates` parameter for `US_Address` (return up to 10 candidates for partial or ambiguous input).

## 1.3.0 - 2026-05-04

### ADDED
- `match_strategy` parameter for `US_Address` and `US_Address_Bulk` (`strict`, `invalid`, or `enhanced`).

## 1.2.1 - 2026-04-17

### ADDED
- Automated release pipeline.

## 1.2.0 - 2026-04-17

### ADDED
- New business data tools: `US_Business_Summary_Smartykey`, `US_Business_Summary_Components`, and `US_Business_Detail`.

## 1.1.1 - 2026-04-14

### FIXED
- Prevent mid-request session termination.

## 1.1.0 - 2026-04-10

### ADDED
- Basic authentication middleware.

### CHANGED
- Migrated shutdown orchestration to `github.com/smarty/dominoes`.
- Added built-in panic recovery
- Updated Go toolchain and dependencies.

## 1.0.1 - 2026-04-01

### FIXED
- Track in-flight GET/SSE requests to prevent premature session expiration.

## 1.0.0 - 2026-03-31

### ADDED
- Initial release of Smarty MCP Server