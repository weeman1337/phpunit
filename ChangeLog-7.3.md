# Changes in PHPUnit 7.3

All notable changes of the PHPUnit 7.3 release series are documented in this file using the [Keep a CHANGELOG](http://keepachangelog.com/) principles.

## [7.3.0] - 2018-08-03

### Added

* Implemented [#3147](https://github.com/sebastianbergmann/phpunit/pull/3147): Support for running tests first that failed in a previous run
  * Implemented `cacheResult` configuration directive and `--cache-result` CLI option to control test result cache required for "run defects first" functionality (disabled by default)
  * Implemented `cacheResultFile` configuration directive and `--cache-result-file` CLI option to configure test result cache file (default: `.phpunit.result.cache`)
  * Implemented `stopOnDefect` configuration directive and `--stop-on-defect` CLI option for aborting test suite execution upon first defective test
  * Implemented `executionOrder` configuration directive and `--order-by` CLI option for sorting the test suite before execution
  * The `--order-by=random` CLI option should now be used instead of `--random-order`
  * The `--order-by=depends` CLI option should now be used instead of `--resolve-dependencies`
  * The `--order-by=reverse` CLI option should now be used instead of `--reverse-order`
* Implemented [#3161](https://github.com/sebastianbergmann/phpunit/pull/3161): Support for indexed arrays in `PHPUnit\Framework\Constraint\ArraySubset`
* Implemented [#3194](https://github.com/sebastianbergmann/phpunit/issues/3194): `@covers class` (and `@uses class`) should include traits used by class
* Implemented [#3196](https://github.com/sebastianbergmann/phpunit/issues/3196): Support for replacing placeholders in `@testdox` text with data provider values
* Implemented [#3198](https://github.com/sebastianbergmann/phpunit/pull/3198): Provide source location for useless tests

### Fixed

* Fixed [#3154](https://github.com/sebastianbergmann/phpunit/issues/3154): Global constants as default parameter values are not handled correctly in namespace

[7.3.0]: https://github.com/sebastianbergmann/phpunit/compare/7.2...7.3.0

