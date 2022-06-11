# Software Versioning

Software versioning is the process of assigning either unique version names or unique version numbers to unique states of computer software.

- [en.wikipedia.org/wiki/Software_versioning](https://en.wikipedia.org/wiki/Software_versioning){:target="_blank"}

## [Conventional Commits 1.0.0](https://www.conventionalcommits.org){:target="_blank"}

The conventional commits specification. This convention dovetails with SemVer(Semantic Versioning), by describing the features, fixes, and breaking changes made in commit messages.

The most important prefixes you should have in mind are:

- `fix:` which represents bug fixes, and correlates to a SemVer(Semantic Versioning) patch.
- `feat:` which represents a new feature, and correlates to a SemVer minor.
- `feat!:`, or `fix!:`, `refactor!:`, etc., which represent a breaking change (indicated by the `!`) and will result in a SemVer major.

## [Semantic Versioning 2.0.0](https://semver.org/){:target="_blank"}

Given a version number MAJOR.MINOR.PATCH, increment the:

1. MAJOR version when you make incompatible API changes,
2. MINOR version when you add functionality in a backwards compatible manner, and
3. PATCH version when you make backwards compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

## [Calendar Versioning](https://calver.org/){:target="_blank"}

CalVer is a versioning convention based on your project's release calendar, instead of arbitrary numbers.

- YYYY - Full year - 2006, 2016, 2106
- YY - Short year - 6, 16, 106
- 0Y - Zero-padded year - 06, 16, 106
- MM - Short month - 1, 2 ... 11, 12
- 0M - Zero-padded month - 01, 02 ... 11, 12
- WW - Short week (since start of year) - 1, 2, 33, 52
- 0W - Zero-padded week - 01, 02, 33, 52
- DD - Short day - 1, 2 ... 30, 31
- 0D - Zero-padded day - 01, 02 ... 30, 31

Case studies

- Ubuntu - YY.0M
- Unity - YYYY.MINOR.MICRO
- pip - YY.MINOR.MICRO
- PyCharm - YYYY.MINOR.MICRO
- OpenSCAD - YYYY.0M
- fusefs-ntfs - YYYY.MM.DD_MICRO
- certifi - YYYY.MM.DD
- boltons - YY.MINOR.MICRO
