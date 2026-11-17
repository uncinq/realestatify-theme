# realestatify-theme

## Install

Edit `config/_default/module.yaml` to install the `realestatify-theme` module.

### V2

This module carries no styling, so it works with either design module. Declare it **first**, before the section modules, the core theme and the styling module: it overrides fields of hugolify-admin, and its mounts have to shadow theirs.

```yml
imports:
  - path: github.com/uncinq/realestatify-theme/v2

  # Section modules
  - path: github.com/hugolify/hugolify-theme-realestates/v2

  # Core theme
  - path: github.com/hugolify/hugolify-theme/v2

  # Styling, one of the two
  - path: github.com/hugolify/hugolify-theme-design-system # CSS + design tokens
  # - path: github.com/hugolify/hugolify-theme-bootstrap   # SASS + Bootstrap 5
```

### V1

```yml
imports:
  - path: github.com/uncinq/realestatify-theme
  - path: github.com/hugolify/hugolify-theme
```

## Structured data

The theme adds `RealEstateAgent`, a local business, to the generic schema.org types of hugolify-theme, through `layouts/_partials/func/GetSchemaTypesTheme.html`. Hugolify admin offers it for the organization, under *Config › Structured data*, and for each place. A site that defines its own hook replaces it, see [Structured data](https://www.hugolify.io/docs/customization/structured-data/#types).

## Releasing

Tags are `v`-prefixed (`v2.0.0`): a `/v2` module path is only resolvable from a `v2.x.y` semver tag.

```bash
npx release-it
```

## Documentation

- [Hugolify documentation](https://www.hugolify.io/docs/)
- [Migration from v1 to v2](https://www.hugolify.io/docs/getting-started/migration/)

## Licensing

Hugolify is free for personal or commercial projects (MIT license)
