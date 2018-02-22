# TDS-Codemod

TDS Codemod scripts. This repository contains a transform file to be used with [jscodeshift][facebook-jscodeshift] to facilitate in the upgrade from the [TDS][tds-github] v1.y.z mono-package to split packages by refactoring import statements programatically.

## Usage for projects running TDS v0.34.z or earlier

It is not recommended upgrade to split packages from these versions due to the removal of global CSS. Before using this codemod, it is recommended to upgrade to TDS 1.0.z by following the [TDS v1.0.0 migration guide][migration].

## Usage for projects running TDS v1.y.z

### Requirements

* Node 8 or greater
* The latest version of Yarn
* The latest version of npm

1. Clone this repository locally
2. Install jscodeshift CLI: `yarn global add jscodeshift` or `npm i -g jscodeshift`
3. Transform your project files by running the following command:

```sh
jscodeshift ~/path/to/your/project/ui/src/**/*.jsx -t ~/path/to/tds-codemod/src/transform.js
```

[facebook-jscodeshift]: https://github.com/facebook/jscodeshift
[tds-github]: https://github.com/telusdigital/tds
[migration]: https://github.com/telusdigital/tds/releases/tag/v1.0.0