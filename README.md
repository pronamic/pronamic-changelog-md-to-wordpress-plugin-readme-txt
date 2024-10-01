# Pronamic `CHANGELOG.md` to WordPress plugin `readme.txt`

Automates syncing of changelog entries from `CHANGELOG.md` to WordPress plugin `readme.txt`.

## Table of contents

- [Usage](#usage)
- [Exit code](#exit-code)
- [Links](#links)

## Usage

To keep this library simple, two markers are needed in `CHANGELOG.md` and `readme.txt`.

```
<!-- Start changelog -->
```

```
<!-- End changelog -->
```

### WordPress plugin `readme.txt`

https://wordpress.org/plugins/readme.txt

```
=== Plugin Name ===
Contributors: (this should be a list of wordpress.org userid's)
Donate link: https://example.com/
Tags: tag1, tag2
Requires at least: 4.7
Tested up to: 5.4
Stable tag: 4.3
Requires PHP: 7.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Here is a short description of the plugin.  This should be no more than 150 characters.  No markup here.

== Description ==

This is the long description.  No limit, and you can use Markdown (as well as in the following sections).

== Changelog ==

⬇️
<!-- Start changelog -->

= 1.0 =
* A change since the previous version.
* Another change.

= 0.5 =
* List versions from most recent at top to oldest at bottom.

<!-- End changelog -->
⬆️
```

### Composer script

```json
	"scripts": {
		"changelog": "Pronamic\\ChangelogMdToWordPressPluginReadmeTxt\\Synchronizer::run"
	}
```

```json
	"scripts": {
		"changelog": "vendor/bin/pronamic-changelog-md-to-wordpress-plugin-readme-txt"
	}
```

## Exit code

| Exit code | Description |
| --------- | ----------- |
| `0`       | Succes.     |
| `1`       | Error.      |

## Links

- https://keepachangelog.com/
- https://developer.wordpress.org/plugins/wordpress-org/how-your-readme-txt-works/
- https://everything.curl.dev/cmdline/exitcode.html
- https://github.com/Automattic/wordbless
