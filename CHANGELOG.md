# CHANGELOG

## Version 3.0.0

### Breaking Changes

#### Fixed locale names

The `zh-cn` and `zh-hk` were named incorrectly. They have been properly renamed as `zh-CN` and `zh-HK`.

#### Dropped

Dropped `pagy_serialized`, `pagy_apply_init_tag` and `PagyInit` javascript namespace. They were too basic to be useful as support for javascript powered custom component.

#### Renamed nav helper methods and files

The javascript-powered helpers (`pagy*_responsive_nav`, `pagy*_compact_nav` and `items_selector`) have been renamed in order to be simpler and more descriptive of their arguments, features and requirements. They have been improved internally, but you need only to search and replace because their usage has not been changed.

#### Bootstrap Extra

| v2.0+                                          | v3.0+                            |
|:-----------------------------------------------|:---------------------------------|
| `pagy_bootstrap_responsive_nav` `:breakpoints` | `pagy_bootstrap_nav_js` `:steps` |
| `pagy_bootstrap_compact_nav`                   | `pagy_bootstrap_combo_nav_js`    |

#### Bulma Extra

| v2.0+                                      | v3.0+                        |
|:-------------------------------------------|:-----------------------------|
| `pagy_bulma_responsive_nav` `:breakpoints` | `pagy_bulma_nav_js` `:steps` |
| `pagy_bulma_compact_nav`                   | `pagy_bulma_combo_nav_js`    |

#### Foundation Extra

| v2.0+                                           | v3.0+                             |
|:------------------------------------------------|:----------------------------------|
| `pagy_foundation_responsive_nav` `:breakpoints` | `pagy_foundation_nav_js` `:steps` |
| `pagy_foundation_compact_nav`                   | `pagy_foundation_combo_nav_js`    |

#### Materialize Extra

| v2.0+                                            | v3.0+                              |
|:-------------------------------------------------|:-----------------------------------|
| `pagy_materialize_responsive_nav` `:breakpoints` | `pagy_materialize_nav_js` `:steps` |
| `pagy_materialize_compact_nav`                   | `pagy_materialize_combo_nav_js`    |

#### Plain > Navs Extra

| v2.0+                                      | v3.0+                        |
|:-------------------------------------------|:-----------------------------|
| `pagy_plain_nav` (`pagy_nav` alias)        | - removed -                  |
| `pagy_plain_responsive_nav` `:breakpoints` | `pagy_nav_js` `:steps`       |
| `pagy_plain_compact_nav`                   | `pagy_combo_nav_js`          |
| `require "pagy/extras/plain"`              | `require "pagy/extras/navs"` |

#### Semantic Extra

| v2.0+                                         | v3.0+                           |
|:----------------------------------------------|:--------------------------------|
| `pagy_semantic_responsive_nav` `:breakpoints` | `pagy_semantic_nav_js` `:steps` |
| `pagy_semantic_compact_nav`                   | `pagy_semantic_combo_nav_js`    |

#### Renamed Pagy::VARS

`Pagy::Vars[:breakpoints]` has been renamed as `Pagy::VARS[:steps]`

#### Renamed items_selector

`items_selector` has been renamed as `items_selector_js`

#### Renamed classes and params in helpers

**Notice**: You can skip the following sections if you did not override any nav helper.

#### CSS nav classes

The `nav` CSS classes follow the same renaming rules of the helper methods:

| v2.0+                             | v3.0+                           |
|:----------------------------------|:--------------------------------|
| `pagy-bootstrap-responsive-nav`   | `pagy-bootstrap-nav-js`         |
| `pagy-bootstrap-compact-nav`      | `pagy-bootstrap-combo-nav-js`   |
| `pagy-bulma-responsive-nav`       | `pagy-bulma-nav-js`             |
| `pagy-bulma-compact-nav`          | `pagy-bulma-combo-nav-js`       |
| `pagy-foundation-responsive-nav`  | `pagy-foundation-nav-js`        |
| `pagy-foundation-compact-nav`     | `pagy-foundation-combo-nav-js`  |
| `pagy-materialize-responsive-nav` | `pagy-materialize-nav-js`       |
| `pagy-materialize-compact-nav`    | `pagy-materialize-combo-nav-js` |
| `pagy-plain-responsive-nav`       | `pagy-nav-js`                   |
| `pagy-plain-compact-nav`          | `pagy-combo-nav-js`             |
| `pagy-semantic-responsive-nav`    | `pagy-semantic-nav-js`          |
| `pagy-semantic-compact-nav`       | `pagy-semantic-combo-nav-js`    |

#### CSS JSON tag classes

Renamed first param passed to the `pagy_json_tag`:

| v2.0+         | v3.0+             |
|:--------------|:------------------|
| `:responsive` | `:nav`            |
| `:compact`    | `:combo_nav`      |
| `:items`      | `:items_selector` |

#### Javascript funcions

| v2.0+             | v3.0+                 |
|:------------------|:----------------------|
| `Pagy.responsive` | `Pagy.nav`            |
| `Pagy.compact`    | `Pagy.combo_nav`      |
| `Pagy.items`      | `Pagy.items_selector` |

---

For older versions, check the [LEGACY CHANGELOG](https://github.com/ddnexus/pagy/blob/master/LEGACY_CHANGELOG.md).
