# Changelog

## 0.3.2
- Fixed a typo with stale resource config (#13)
- Make HTTPS the default upstream registry transport (#12)

## 0.3.1
- Fixed issue with config.json file not being found and issue where upstreamPort
  wasn't being honored ( #10 )
- Fixes an issue with Lactate cache expiry options leading to excessive CPU
  usage ( #11 )

## 0.3.0
- Large cleanup and refactor for new feature implementations.
- Now have the ability to serve stale resources from the cache while they cannot
  be refreshed from the upstream registry. (`--permit_stale_resources`)
- Support a list of blacklisted packages using semver ranges via a JSON
  configuration file. See an example configuration in the `examples/` folder.
  Enabled with `--package_blacklist <path to config file>`
- Added example server configuration in `examples/`
- Fix a bug where non 200 upstream registry responses were written to disk.
- Other minor bug fixes.

## 0.2.3
- Fix packages with multiple versions not being routed to the appropriate
  handler.

## 0.2.2
- Support version parsing when the package identifies itself with multiple
semvers.

## 0.2.1

- Ensure dots are parsed in the package name via HTTP routes.
