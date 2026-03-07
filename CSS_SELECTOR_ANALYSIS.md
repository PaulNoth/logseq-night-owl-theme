# CSS Selector Comparison: Dark vs Light Theme

**Legend:**
- **1a** — Selector exists in both themes, uses the **same CSS variables / identical values**
- **1b** — Selector exists in both themes, uses **different values or variables**
- **2a** — Selector exists in **dark theme only**
- **2b** — Selector exists in **light theme only**

---

## Case 1a — Same selector, same values / variables

These are structurally and visually identical between the two themes.

| Selector | Properties |
|---|---|
| `#main-content-container` | `font-size: 1em; font-weight: 400; letter-spacing: .002em` |
| `#main-content-container .editor-wrapper textarea,`<br>`#main-content-container .block-content-wrapper .inline` | *(empty placeholder)* |
| `.page-properties` | `background-color: var(--ls-block-properties-background-color)` |
| `.page-properties .page-property-key` | `color: var(--ct-primary-text-color)` |
| `.blocks-container` | `padding: 10px` |
| `a.external-link:before` | `font-family: tabler-icons!important; content: '\ea99'` |
| `.page-reference:hover` | `background-color: transparent` |
| `.absolute-modal[data-modal-name="page-search"]` | `background-color: var(--ls-primary-background-color)` |
| `#main-content input.form-checkbox:checked` | `background-color: var(--ls-page-checkbox-border-color)` |

---

## Case 1b — Same selector, different values or variables

Selector exists in both themes but with different colors, variables, or even different CSS properties.

| Selector | Dark | Light | Difference |
|---|---|---|---|
| `::selection` | `background-color: #1d3b53`<br>`color: #d6deeb` | `background-color: #E0E0E0`<br>`color: #403f53` | Different raw hex values |
| `a.page-ref, a.external-link` | `color: #d6deeb`<br>`border-bottom: 1px dashed #122d42` | `color: #4876d6`<br>`border-bottom: 1px dashed #d9d9d9` | Different raw hex values |
| `a.page-ref:hover, a.external-link:hover` | `border-bottom: 1px dashed #82AAFF`<br>`color: #82AAFF` | `border-bottom: 1px dashed #4876d6` | Dark adds `color` property; different border values |
| `.color-level` | `background: none` | `background-color: transparent`<br>+ nested `.content { padding: 5px 0 }`<br>+ nested `.blocks-container { background-color: var(...); padding: 10px }` | Light has additional nested rules; dark defines `.color-level .blocks-container` as a separate rule |
| `#main-content-container .ui__button,`<br>`.ui__modal-panel .ui__button` | `background-color: #7e57c2`<br>`color: #ffffff`<br>`border: none` | `background-color: #2AA298`<br>`color: #F0F0F0`<br>`border: none` | Different raw hex values |
| `.cp__all_pages .cp__all_pages_table th` | `border-bottom: 1px solid var(--ls-guideline-color)` | `border-bottom: 1px solid #d9d9d9` | Dark uses CSS variable; light uses raw hex |
| `.cp__all_pages .search-wrap .form-input` | `border: none`<br>`border-bottom: 1px solid var(--ls-guideline-color)`<br>`border-radius: 0` | `border: none`<br>`border-bottom: 1px solid #d9d9d9`<br>`border-radius: 0` | Dark uses CSS variable; light uses raw hex |
| `.cp__all_pages .search-wrap .ui__button` | `background: transparent !important`<br>`color: #d6deeb` | `background: transparent !important`<br>`color: #403f53` | Different text color |
| `.cp__themes-installed>.it.is-active` | `color: var(--ct-primary-color)` | `background-color: #d3e8f8`<br>`border: none` | Entirely different properties: dark sets text color, light sets background |
| `code, .CodeMirror` | `background-color: #01111d`<br>`color: #d6deeb` | `background-color: var(--ls-block-properties-background-color)`<br>`color: #403f53` | Dark uses raw hex for bg; light uses CSS variable; different color values |
| `pre` | `background-color: #01111d`<br>`border: 1px solid #122d42` | `background-color: var(--ls-block-properties-background-color)`<br>`border: 1px solid #d9d9d9` | Dark uses raw hex; light uses CSS variable for bg |
| `.extensions__code-lang` | `background-color: var(--ls-block-properties-background-color)` | `background-color: #F0F0F0`<br>`color: #403f53` | Light adds `color` property; dark uses CSS variable, light uses raw hex |
| `.CodeMirror-linenumber` | `color: #4b6479` | `color: #90A7B2` | Different raw hex values |
| `.CodeMirror-activeline-background` | `background: #010d18` | `background: #F0F0F0` | Different raw hex values |
| `.ls-block:focus-within` | `background-color: #010d18` | `background-color: #F0F0F0` | Different raw hex values |
| `.tag` | `background-color: var(--ls-block-properties-background-color)`<br>`color: #c792ea`<br>`border: 1px solid #122d42` | `background-color: #F0F0F0`<br>`color: #994cc3`<br>`border: 1px solid #d9d9d9` | Dark uses CSS variable for bg; light uses raw hex throughout; different color values |
| `h1, h2, h3, h4, h5, h6` | `color: #82AAFF` | `color: #4876d6` | Different raw hex values |
| `h1.title` | `color: #d2dee7` | `font-weight: 500; text-decoration: none`<br>`color: #403f53` *(defined twice in light)* | Light adds layout properties; different color values |
| `.ls-block .bullet` | `background-color: #d6deeb` | `background-color: #403f53` | Different raw hex values |
| `.ls-block .bullet-closed` | `background-color: #5f7e97` | `background-color: #93A1A1` | Different raw hex values |
| `:not(pre) > code` | `background-color: var(--ls-block-properties-background-color)`<br>`color: #c5e478`<br>`padding: 2px 6px`<br>`border-radius: 3px`<br>`border: 1px solid #122d42` | `background-color: #F0F0F0`<br>`color: #994cc3`<br>`padding: 2px 6px`<br>`border-radius: 3px`<br>`border: 1px solid #d9d9d9` | Dark uses CSS variable for bg; different color values; same padding/radius |
| `.priority` | `color: #c792ea` | `color: #de3d3b` | Different raw hex values |
| `.timestamp` | `color: #7fdbca` | `color: #0c969b` | Different raw hex values |

---

## Case 2a — Dark theme only

These selectors have **no equivalent** in the light theme.

| Selector | Properties |
|---|---|
| `.cp__sidebar-left-layout` | `background-color: var(--ct-primary-color)` |
| `.cp__plugins-item-lists .cp__plugins-item-card` | `background-color: transparent`<br>`border: 1px solid var(--ct-primary-color)` |
| `.cp__plugins-page .tabs .ui__button.active>span` | `color: var(--ct-primary-color)` |
| `.menu-link:hover, button.menu:focus, button.pull:hover,`<br>`#sidebar-nav-wrapper .dropdown-wrapper a:hover` | `color: var(--ct-primary-color)` |
| `.left-sidebar-inner .nav-content-item>.header:hover` | `background-color: #010d18`<br>`color: #d2dee7` |
| `.logseq-focus-toolbar, .cp__header`<br>`{ a.button.active, a.button:hover }` | `color: var(--ct-primary-color)` |
| `.block-highlight, .content .selected` | `background-color: var(--ls-block-properties-background-color)`<br>`border: none` |
| `.search-results-wrap a:hover` | `color: #82AAFF`<br>`background-color: #010d18` |
| `text-area` | `color: var(--ct-primary-text-color)` |
| `.cp__all_pages .ti-search` | `color: var(--ls-link-text-color)` |

---

## Case 2b — Light theme only

These selectors have **no equivalent** in the dark theme.

| Selector | Properties |
|---|---|
| `#search-button, #left-menu` | `color: #403f53` |
| `.left-sidebar-inner a.item,`<br>`.left-sidebar-inner .nav-content-item .bd ul a,`<br>`.left-sidebar-inner .header a` | `color: #403f53` |
| `.cp__header a` | `color: #403f53` |
| `.cp__header a:hover` | `color: #4876d6` |
| `.ui__modal-panel` | `background-color: #FBFBFB` |
| `.tippy-tooltip` | `background-color: #F0F0F0`<br>`border: 1px solid #d9d9d9` |
| `.tippy-wrapper` | `background-color: #FBFBFB` |
| `.cp__plugins-item-card, .ui__button` | `background-color: #F0F0F0` |
| `.graph-filters` | `background-color: #F0F0F0` |
| `.cp__right-sidebar` | `background-color: #F0F0F0` |
| `.cp__right-sidebar-topbar` | `background-color: #F0F0F0`<br>`border-bottom: 1px solid #d9d9d9` |
| `.sidebar-item-list .sidebar-item` | `background-color: #FBFBFB`<br>`margin-left: 4px` |
| `.sidebar-item-list .sidebar-item .blocks-container` | `background-color: #FBFBFB` |
| `.form-checkbox` | `border: 1px solid var(--ls-page-checkbox-border-color)`<br>`border-radius: 2px` |
| `.cp__sidebar-help-btn` | `background-color: #F0F0F0`<br>`color: #2AA298`<br>`border: 1px solid #2AA298` |
| `.cp__palette-main .chosen` | `background-color: #d3e8f8` |
| `.cp__plugins-page .ui__button,`<br>`.cp__settings-inner>aside ul>li.active,`<br>`blockquote` | `background-color: var(--ls-block-properties-background-color) !important` |
| `.cp__settings-inner>aside ul>li>a` | `background: none` |
| `.keyboard-shortcut>code` | `color: #403f53` |
| `.cp__themes-installed>.it` | `background: none` |
| `.cp__settings-app-updater .update-state` | `background-color: var(--ls-block-properties-background-color)`<br>`color: #403f53` |
| `blockquote` | `border-left: 3px solid #2AA298`<br>`color: #403f53` |
| `.external-link` | `color: #4876d6` |
| `.external-link:hover` | `color: #2AA298` |
| `.marker-switch` | `background-color: #2AA298`<br>`color: #F0F0F0` |
| `.page-ref` | `color: #4876d6` |
| `.page-ref:hover` | `color: #2AA298`<br>`background-color: transparent` |

---

## Summary

| Category | Count |
|---|---|
| **1a** Same selector, same values | 9 |
| **1b** Same selector, different values | 23 |
| **2a** Dark theme only | 10 |
| **2b** Light theme only | 26 |

### Notable inconsistencies

- **`.cp__themes-installed>.it.is-active`** — completely different CSS properties: dark sets `color`, light sets `background-color` + `border`. Functionally divergent.
- **`.extensions__code-lang`** — dark has only `background-color` (via variable), light also adds `color`. Missing `color` in dark.
- **`a.page-ref:hover, a.external-link:hover`** — dark includes `color` on hover, light only changes `border-bottom`. Asymmetric hover behavior.
- **`code, .CodeMirror` / `pre`** — dark hardcodes colors as raw hex, light uses `var(--ls-block-properties-background-color)`. Inconsistent variable usage.
- **`.cp__all_pages th` / `.search-wrap .form-input`** — dark uses `var(--ls-guideline-color)`, light uses raw `#d9d9d9`. Should use variables consistently.
- **Light-only sidebar/panel selectors** — `.ui__modal-panel`, `.cp__right-sidebar`, `.tippy-tooltip`, etc. are not overridden in the dark theme, relying on defaults from `_colors.scss` or Logseq base styles. Dark theme may need explicit overrides for these.
