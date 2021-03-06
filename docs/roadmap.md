# Current Project Roadmap (Mid 2020 - Mid 2021)

The below items are general topics which may or may not include current GitHub issues.

# v5.x:

## Deployment:
* Deployment Tasks: configurable, deferrable deployment for exports, ccs, ssh/sftp, apache, nginx, exchange etc
* Better general support for non-IIS scenarios
* Deploy certs to vault (Hashicorp Vault etc)
* Fetch latest from vault (deploy to bindings)
* Default password on PFX etc, optional custom per managed cert. Needs data protection.
* support for IIS wildcard bindings (*.example.com) - only when cert has matching wildcard?
* Need to warn user when their deployment will target no bindings
* CCS/Web farm - Simplest/best way to achieve coordinated (or proxied) challenge responses?

## Remote server support
* Possible to offer support for managing certificates on non-windows servers.

## Reporting
* Variety of reports/scans to determine current status of sites/services to determine which are currently managed and which are not. Diagnostics scans.

## Domain options
* Needs performance improvements for many bindings scenario
* Possibly sort checked items to the top, or scroll to first and sort in reverse domain order

## DNS Validation
* Provide custom CNAME redirection service (probably based on a hosted acme-dns solution)
* Additional DNS API support (community provided)

## Upgrading
* Add release notes to update UI
* Prompt user to remove the old scheduled task
* Introduce db schema version for easier migration detection

## Accessibility
* Check and fix current accessibility for core functions

## Stored Credentials
* Make credential encryption scope optional (CurrentUser vs LocalMachine), provide migration between options.
* Provide export/import option

## Improve config checks
* Possibly use letsdebug.net API for extended diagnostics

## Docs/Portal/API
* Website improvements
* Documentation updates
* Separate dashboard app from main website
* Move API to AWS/Azure functions

## Misc
* Localization text updates
* EFS not implemented yet
* Allow http validation to wait a delay before completing validation (web farm volume sync)
* Option to cancel config check mid tests
* Capture config check verbose logs so full details can be viewed
* Failed validations can be re-tried later? would need to store validation status info
* check localhost bindings to 127.0.0.1 and not an IP e.g. netsh http show iplisten, netsh http delete, iplisten ipaddress=195.43.64.112 
* Credential export option (backup credentials). Should email the primary contact when it occurs. Should we email the primary contact when their details are changed in the app? Could be a pref controlled in the dashboard.
* Full config backup/restore - needs to be protected if it contains credentials. Option for cloud sync/backup (files can be v. large).
* Windows Admin Center extension?
* Proxy support

# Investigate
* Cross platform UI options for desktop app (mac os & linux support)
* Centralised management options
* Storage in Hashicorp Vault, Azure etc and retrieval (one instance can renew and store a cert for other instances to consume)
