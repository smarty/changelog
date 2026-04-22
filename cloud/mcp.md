# Changelog - Smarty MCP

All notable changes to the Smarty MCP Server will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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