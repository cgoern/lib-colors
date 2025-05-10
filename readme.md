![ink logo](./ink.svg)

Color tooling and core colors library.

[![npm publish](https://github.com/cgoern/lib-colors/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/cgoern/lib-colors/actions/workflows/npm-publish.yml)
![npm (scoped)](https://img.shields.io/npm/v/@cgoern/lib-colors)

## Usage

Run `npm i @cgoern/lib-colors` in your project directory.

Use and (optionally) configure the Sass module:

```scss
@use '@cgoern/lib-colors' with (
  $namespace: 'acme',
  $useDarkMode: false,
  $useDisplayP3: false
);
```

Use the predefined modules:

```scss
@use '@cgoern/lib-colors/core';
@use '@cgoern/lib-colors/gray';

:root {
  @include core.palette;
  @include gray.palette;
}
```

### Use the built-in mixins

Declare multiple colors:

```scss
$myPalette: (
  'brand': rgb(242 59 34),
  'accent': rgb(52 195 117),
);

:root {
  @include lib-colors.colors($myPalette);
}
```

Declare a single color:

```scss
:root {
  // RGB color
  @include lib-colors.color('brand', rgb(242 59 34));

  // Display P3 color
  @include lib-colors.color('brand', rgb(242 59 34), true);
}
```
