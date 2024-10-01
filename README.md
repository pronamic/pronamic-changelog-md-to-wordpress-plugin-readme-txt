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

## Exit code

| Exit code | Description |
| --------- | ----------- |
| `0`       | Succes.     |
| `1`       | Error.      |

## Links

- https://keepachangelog.com/
- https://everything.curl.dev/cmdline/exitcode.html
- https://github.com/Automattic/wordbless
