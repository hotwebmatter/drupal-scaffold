---
title: Coding standards
tags:
  - coding standards
  - php
  - scss
  - sass
  - js
  - javascript
---
# Coding standards

This project comes with linting tools to check the syntax of custom code against
established coding standards/recommendations. Linters are available for the
following languages:

* JavaScript (ES6)
* PHP
* SASS

## JavaScript (ES6)

The validator for custom JavaScript is [ESLint][]. This project uses the
`/web/core/.eslintrc.json` file to validated custom JavaScript. The [ESLint][]
file provided by [Drupal][] core follows the
[Drupal coding standards for JavaScript][].

## PHP

The validator for custom PHP is [PHPCS][]. This project uses the `drupal/coder`
package to validate custom PHP files against the
[Drupal coding standards for PHP][].

## SASS

The validator for custom SASS is [stylelint][]. This project uses the
[SASS Guidelines][] with _some_ modifications:

**Rule:** `max-nesting-depth`
* Recommend setting is `1` but then, what is the point of SASS

**Rule:** `selector-no-qualifying-type`
* Qualifying a selector by type is allowed.

**Rule** `selector-max-compound-selectors`
* Maximum allowed compound selectors is increased from 3 to 4.

**Rule** `order/properties-alphabetical-order`
* Alphabetical order of properties is not enforced.

To temporarily disable the linter for certain code blocks you can use the syntax
below. More information can be found in the linter[docs][].

`
/* stylelint-disable selector-no-id, declaration-no-important  */
#id {
  color: pink !important;
}
/* stylelint-enable */
`

[Drupal]: https://drupal.org
[Drupal coding standards for JavaScript]: https://www.drupal.org/docs/develop/standards/javascript/javascript-coding-standards
[Drupal coding standards for PHP]: https://www.drupal.org/docs/develop/standards/coding-standards
[ESLint]: https://eslint.org
[PHPCS]: https://github.com/squizlabs/PHP_CodeSniffer
[stylelint]: https://github.com/stylelint/stylelint
[SASS Guidelines]: https://sass-guidelin.es
[docs]: https://github.com/stylelint/stylelint/blob/master/docs/user-guide/configuration.md#turning-rules-off-from-within-your-css
