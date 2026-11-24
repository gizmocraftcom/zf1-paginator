# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-paginator`, published as `gizmocraft/zendframework1-paginator`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-paginator` to `gizmocraft/zendframework1-paginator`. It now requires `gizmocraft/zendframework1-exception`, `-loader`, `-json`, `-cache`, `-controller`, `-db`, `-filter` and `-view` (each `^2.0.0`) and `-config` (`^3.0.0`).

### Other changes

- `is_integer()` (deprecated in PHP 8.6) replaced by `is_int()` in `Zend_Paginator` and `Zend_Paginator_Adapter_DbSelect`. No signature changes.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. The removed `getMockForAbstractClass()` calls use a real in-memory `Zend_Db_Adapter_Pdo_Sqlite`. The Oracle tests (skipped without Oracle) no longer error in `tearDown()` when `setUp()` was skipped.
- Removed an obsolete PHPStan ignore pattern.
- CI runs PHP 8.5 and 8.6.
