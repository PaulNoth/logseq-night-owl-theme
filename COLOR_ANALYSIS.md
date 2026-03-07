# Color Analysis: Dark vs Light Theme

## 1. CSS Variables — Common to Both Themes (different values)

These CSS variables are explicitly defined in **both** `_theme_dark.scss` and `_theme_light.scss`.

| Variable | Dark | Light |
|---|---|---|
| `--ct-highlight-color` | `#7e57c2` | `#d3e8f8` |
| `--ct-tertiary-color` | `#1d3b53` | `#F6F6F6` |
| `--ct-primary-text-color` | `#d6deeb` | `#403f53` |
| `--ls-selection-background-color` | `#1d3b53` | `#E0E0E0` |
| `--ls-primary-background-color` | `#011627` | `#FBFBFB` |
| `--ls-primary-text-color` | `var(--ct-primary-text-color)` | `#403f53` |
| `--ls-title-text-color` | `#d2dee7` | `#403f53` |
| `--ls-link-text-color` | `#82AAFF` | `#4876d6` |
| `--ls-guideline-color` | `#122d42` | `#d9d9d9` |
| `--ls-table-tr-even-background-color` | `#010b14` | `#F6F6F6` |
| `--ls-block-properties-background-color` | `#0b2942` | `#F6F6F6` |
| `--ls-code-bg-color` | `#01111d` | `#F6F6F6` |
| `--ls-code-text-color` | `#d6deeb` | `#403f53` |

---

## 2. CSS Variables — Dark Theme Only

These variables are defined **only in `_theme_dark.scss`** and have no counterpart in the light theme.

| Variable | Value |
|---|---|
| `--ls-link-ref-text-color` | `#d6deeb` |
| `--ls-block-bullet-color` | `#d6deeb` |
| `--ls-block-bullet-border-color` | `#4b6479` |
| `--ls-scrollbar-foreground-color` | `#084d8180` |
| `--ls-scrollbar-background-color` | `#010b14` |
| `--ls-scrollbar-thumb-hover-color` | `#084d8180` |
| `--ls-page-blockquote-border-color` | `#5f7e97` |
| `--ls-page-blockquote-bg-color` | `#01111d` |
| `--ls-page-blockquote-color` | `var(--ct-primary-text-color)` |

---

## 3. CSS Variables — Light Theme Only

These variables are defined **only in `_theme_light.scss`** and have no counterpart in the dark theme.

| Variable | Value |
|---|---|
| `--ct-primary-color` | `#F0F0F0` |
| `--ct-primary-hover-color` | `#d3e8f8` |
| `--ct-secondary-color` | `#2AA298` |
| `--ct-icon-color` | `#403f53` |
| `--ct-warning-color` | `#de3d3b` |
| `--ct-success-color` | `#08916a` |
| `--ls-secondary-background-color` | `#F0F0F0` |
| `--ls-tertiary-background-color` | `#F6F6F6` |
| `--ls-secondary-text-color` | `#93A1A1` |
| `--ls-border-color` | `#d9d9d9` |
| `--ls-page-checkbox-border-color` | `#2AA298` |

---

## 4. CSS Rule Selectors — Common to Both Themes

These selectors appear in both theme files (with theme-appropriate colors).

| Selector | Notes |
|---|---|
| `#main-content-container` | font-size, font-weight, letter-spacing |
| `.page-properties` | background, `.page-property-key` color |
| `.blocks-container` | padding |
| `.color-level` | background |
| `a.page-ref, a.external-link` | color, border-bottom |
| `a.page-ref:hover, a.external-link:hover` | border-bottom (+ color in dark) |
| `a.external-link:before` | icon content (identical in both) |
| `.page-reference:hover` | background transparent (identical) |
| `#main-content-container .ui__button, .ui__modal-panel .ui__button` | background, color, border |
| `.absolute-modal[data-modal-name="page-search"]` | background |
| `.cp__all_pages .cp__all_pages_table th` | border-bottom |
| `.cp__all_pages .search-wrap .form-input` | border |
| `.cp__all_pages .search-wrap .ui__button` | background transparent, color |
| `.cp__themes-installed>.it.is-active` | active state color/bg |
| `#main-content input.form-checkbox:checked` | background |
| `code, .CodeMirror` | background, color |
| `pre` | background, border |
| `.extensions__code-lang` | background |
| `.CodeMirror-linenumber` | color |
| `.CodeMirror-activeline-background` | background |
| `.ls-block:focus-within` | background |
| `.tag` | background, color, border |
| `h1, h2, h3, h4, h5, h6` | color |
| `h1.title` | color |
| `.ls-block .bullet` | background |
| `.ls-block .bullet-closed` | background |
| `:not(pre) > code` | background, color, padding, border-radius, border |
| `.priority` | color |
| `.timestamp` | color |
| `::selection` | background, color |

---

## 5. CSS Rule Selectors — Dark Theme Only

| Selector |
|---|
| `.cp__sidebar-left-layout` |
| `.cp__plugins-item-lists .cp__plugins-item-card` |
| `.cp__plugins-page .tabs .ui__button.active>span` |
| `.menu-link:hover, button.menu:focus, button.pull:hover, #sidebar-nav-wrapper .dropdown-wrapper a:hover` |
| `.logseq-focus-toolbar, .cp__header { a.button.active, a.button:hover }` |
| `.block-highlight, .content .selected` |
| `.search-results-wrap a:hover` |
| `text-area` |

---

## 6. CSS Rule Selectors — Light Theme Only

| Selector |
|---|
| `#search-button, #left-menu` |
| `.left-sidebar-inner a.item, .left-sidebar-inner .nav-content-item .bd ul a, .left-sidebar-inner .header a` |
| `.cp__header a` |
| `.cp__header a:hover` |
| `.ui__modal-panel` |
| `.tippy-tooltip` |
| `.tippy-wrapper` |
| `.cp__plugins-item-card, .ui__button` |
| `.graph-filters` |
| `.cp__right-sidebar` |
| `.cp__right-sidebar-topbar` |
| `.sidebar-item-list .sidebar-item` |
| `.form-checkbox` |
| `.cp__sidebar-help-btn` |
| `.cp__palette-main .chosen` |
| `.cp__plugins-page .ui__button, .cp__settings-inner>aside ul>li.active, blockquote` |
| `.cp__settings-inner>aside ul>li>a` |
| `.keyboard-shortcut>code` |
| `.cp__themes-installed>.it` |
| `.cp__settings-app-updater .update-state` |
| `blockquote` |
| `.external-link` |
| `.external-link:hover` |
| `.marker-switch` |
| `.page-ref` |
| `.page-ref:hover` |

---

## 7. Comparison with `_colors.scss` (Base Definitions)

`_colors.scss` sets defaults for **both** themes. The theme files then selectively override these.

### 7a. Variables overridden by the dark theme

| Variable | Base (`_colors.scss`) | Dark Override | Note |
|---|---|---|---|
| `--ct-highlight-color` | `#7e57c2` | `#7e57c2` | **Redundant** — same value |
| `--ct-tertiary-color` | `#F6F6F6` | `#1d3b53` | Different |
| `--ct-primary-text-color` | `#403f53` | `#d6deeb` | Different |
| `--ls-selection-background-color` | `#E0E0E0` | `#1d3b53` | Different |
| `--ls-primary-background-color` | `#FBFBFB` | `#011627` | Different |
| `--ls-primary-text-color` | `#403f53` | `var(--ct-primary-text-color)` | Different (references overridden var) |
| `--ls-title-text-color` | `var(--ct-primary-text-color)` | `#d2dee7` | Different |
| `--ls-link-text-color` | `var(--ct-primary-text-color)` | `#82AAFF` | Different |
| `--ls-guideline-color` | `#262A39` | `#122d42` | Different |
| `--ls-table-tr-even-background-color` | `var(--ct-tertiary-color)` | `#010b14` | Different |
| `--ls-page-blockquote-border-color` | `var(--ct-secondary-color)` → `#5f7e97` | `#5f7e97` | **Redundant** — resolves to same value |
| `--ls-page-blockquote-bg-color` | `#FBFBFB` | `#01111d` | Different |

> Variables new in dark theme (not in base): `--ls-block-properties-background-color`, `--ls-block-bullet-color`, `--ls-block-bullet-border-color`, `--ls-scrollbar-*`, `--ls-page-blockquote-color`, `--ls-code-bg-color`, `--ls-code-text-color`, `--ls-link-ref-text-color`.

### 7b. Variables overridden by the light theme

| Variable | Base (`_colors.scss`) | Light Override | Note |
|---|---|---|---|
| `--ct-primary-color` | `#011627` | `#F0F0F0` | Different |
| `--ct-primary-hover-color` | `#010d18` | `#d3e8f8` | Different |
| `--ct-secondary-color` | `#5f7e97` | `#2AA298` | Different |
| `--ct-tertiary-color` | `#F6F6F6` | `#F6F6F6` | **Redundant** — same value |
| `--ct-primary-text-color` | `#403f53` | `#403f53` | **Redundant** — same value |
| `--ct-icon-color` | `#d6deeb` | `#403f53` | Different |
| `--ct-warning-color` | `#EF5350` | `#de3d3b` | Different |
| `--ct-success-color` | `#9CCC65` | `#08916a` | Different |
| `--ct-highlight-color` | `#7e57c2` | `#d3e8f8` | Different |
| `--ls-primary-background-color` | `#FBFBFB` | `#FBFBFB` | **Redundant** — same value |
| `--ls-secondary-background-color` | `var(--ct-primary-color)` | `#F0F0F0` | Effectively same (light `--ct-primary-color` is `#F0F0F0`) |
| `--ls-tertiary-background-color` | `var(--ct-tertiary-color)` | `#F6F6F6` | **Redundant** — resolves to same value |
| `--ls-primary-text-color` | `#403f53` | `#403f53` | **Redundant** — same value |
| `--ls-secondary-text-color` | `#89a4bb` | `#93A1A1` | Different |
| `--ls-title-text-color` | `var(--ct-primary-text-color)` | `#403f53` | Effectively same (light `--ct-primary-text-color` is `#403f53`) |
| `--ls-link-text-color` | `var(--ct-primary-text-color)` | `#4876d6` | Different |
| `--ls-guideline-color` | `#262A39` | `#d9d9d9` | Different |
| `--ls-border-color` | `#5f7e97` | `#d9d9d9` | Different |
| `--ls-selection-background-color` | `#E0E0E0` | `#E0E0E0` | **Redundant** — same value |
| `--ls-table-tr-even-background-color` | `var(--ct-tertiary-color)` | `#F6F6F6` | **Redundant** — resolves to same value |
| `--ls-page-checkbox-border-color` | `#5f7e97` | `#2AA298` | Different |

> Variables new in light theme (not in base): `--ls-block-properties-background-color`, `--ls-code-bg-color`, `--ls-code-text-color`.

### 7c. Base variables NOT overridden by either theme

These `_colors.scss` variables are inherited as-is by both themes:

| Variable | Base Value |
|---|---|
| `--ct-warning-color-text` | `var(--ct-primary-color)` |
| `--ct-success-color-text` | `var(--ct-primary-color)` |
| `--ct-highlight-color-text` | `#ffffff` |
| `--ls-quaternary-background-color` | `var(--ct-primary-hover-color)` |
| `--ls-page-properties-background-color` | `var(--ct-tertiary-color)` |
| `--ls-page-checkbox-color` | `#ffffff` |
| `--night-owl-header-text-color` | `#403f53` |
| `--night-owl-sidebar-text-color` | `#89a4bb` |
| `--night-owl-sidebar-text-color-hover` | `#d2dee7` |
| `--ls-menu-hover-color` | `var(--ct-tertiary-color)` |
| `--ls-block-highlight-color` | `var(--ct-tertiary-color)` |
| `--ls-icon-color` | `var(--ct-icon-color)` |
| `--ls-search-icon-color` | `var(--ct-icon-color)` |
| `--color-level-1` through `--color-level-6` | various |

---

## Summary of Redundant Overrides

These overrides can be safely removed without any visual change:

| Theme | Variable | Reason |
|---|---|---|
| Dark | `--ct-highlight-color: #7e57c2` | Identical to base |
| Dark | `--ls-page-blockquote-border-color: #5f7e97` | Same as base `--ct-secondary-color` which dark doesn't override |
| Light | `--ct-tertiary-color: #F6F6F6` | Identical to base |
| Light | `--ct-primary-text-color: #403f53` | Identical to base |
| Light | `--ls-primary-background-color: #FBFBFB` | Identical to base |
| Light | `--ls-tertiary-background-color: #F6F6F6` | Resolves to same as base |
| Light | `--ls-primary-text-color: #403f53` | Identical to base |
| Light | `--ls-secondary-background-color: #F0F0F0` | Same as light's `--ct-primary-color` which base already references |
| Light | `--ls-selection-background-color: #E0E0E0` | Identical to base |
| Light | `--ls-table-tr-even-background-color: #F6F6F6` | Resolves to same as base (via `--ct-tertiary-color`) |
| Light | `--ls-title-text-color: #403f53` | Resolves to same (light's `--ct-primary-text-color` = `#403f53`) |
