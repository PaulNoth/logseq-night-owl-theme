# CSS Unification Recommendations

## Verdict: Partial, targeted unification

Do not attempt full unification. The themes are intentionally different — that's their purpose. A full merge into shared selectors + variable-only overrides would be a large, risky refactor with limited practical benefit.

Instead, fix the three categories of real problems found.

---

## 1. Fix structural inconsistencies (bugs, not style choices)

These are cases where the same selector does something genuinely different between themes — likely unintentional.

| Selector | Dark | Light | Fix |
|---|---|---|---|
| `.cp__themes-installed>.it.is-active` | `color: var(--ct-primary-color)` | `background-color: #d3e8f8; border: none` | Align to the same properties in both |
| `a.page-ref:hover, a.external-link:hover` | `border-bottom` + `color` | `border-bottom` only | Add `color` to light's hover rule |
| `.extensions__code-lang` | `background-color` only | `background-color` + `color` | Add `color` to dark |

---

## 2. Replace raw hex with variables for consistency

Dark theme correctly uses CSS variables in some places where light hardcodes raw hex for the same values, and vice versa. Align them to use variables consistently.

| Selector | Dark | Light | Recommendation |
|---|---|---|---|
| `.cp__all_pages .cp__all_pages_table th` | `var(--ls-guideline-color)` | `#d9d9d9` | Light should use `var(--ls-guideline-color)` |
| `.cp__all_pages .search-wrap .form-input` | `var(--ls-guideline-color)` | `#d9d9d9` | Light should use `var(--ls-guideline-color)` |
| `code, .CodeMirror` | raw hex `#01111d` | `var(--ls-block-properties-background-color)` | Dark should use `var(--ls-block-properties-background-color)` |
| `pre` | raw hex `#01111d` | `var(--ls-block-properties-background-color)` | Dark should use `var(--ls-block-properties-background-color)` |

---

## 3. Audit light-only selectors for dark coverage

26 selectors exist only in the light theme. Some are almost certainly missing dark overrides — gaps rather than intentional omissions. Review each against the dark theme visually.

Priority candidates:

| Selector | Why it likely needs a dark override |
|---|---|
| `.tippy-tooltip` | Tooltip background/border will use light defaults |
| `.tippy-wrapper` | Same as above |
| `.ui__modal-panel` | Modal panel background unset in dark |
| `.cp__right-sidebar` | Sidebar background unset in dark |
| `.cp__right-sidebar-topbar` | Topbar background and border unset in dark |
| `blockquote` | Border color and text color unset in dark |
| `.marker-switch` | Background and color unset in dark |
| `.external-link` / `.external-link:hover` | Hover color behavior diverges |

---

## What NOT to do

- **Don't merge shared selectors into a third file.** The color differences in 1b selectors are intentional and the current split-file structure is clear and maintainable.
- **Don't replace all raw hex with new CSS variables.** The variable system is already defined in `_colors.scss`. Adding variables for every individual color value would over-engineer the codebase.
- **Don't touch the 9 identical selectors (case 1a).** They are already correct and consistent.

---

## Summary

The architecture is sound. The `_colors.scss` → `_theme_dark.scss` / `_theme_light.scss` split is a clean pattern. The work needed is fixing ~5–8 specific inconsistencies and auditing missing dark overrides — not a structural rewrite.
