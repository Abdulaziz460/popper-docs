# Popper documentation (archive)

These are the docs that were hosted on `popper.js.org`, which has been
decommissioned. They are preserved here in plain Markdown so the Popper v1 and
v2 reference material stays available to people who have not migrated to
Floating UI yet.

Popper is the predecessor to Floating UI. **For new code, use the
[Floating UI docs](https://floating-ui.com/docs/getting-started) instead** —
nothing in this repository describes the current library.

> [!NOTE]
> This is a read-only archive. Popper is no longer maintained, and these
> documents are not updated — they record the library as it was documented when
> the site was retired.

## Finding a page from an old link

The folder layout mirrors the old site's URLs, so an old link maps directly onto
a file. `popper.js.org/docs/v2/modifiers/flip/` is
[`docs/v2/modifiers/flip.md`](./docs/v2/modifiers/flip.md); a URL ending at a
directory is that folder's `index.md`.

## Contents

- [`docs/v2/`](./docs/v2/index.md) — Popper 2 (`@popperjs/core`): constructors,
  lifecycle, modifiers, utils, tutorial, and the v1 → v2 migration guide
- [`docs/v1/`](./docs/v1/index.md) — Popper 1 (`popper.js`) API reference
- [`react-popper/v2/`](./react-popper/v2/index.md) — the `react-popper` wrapper:
  the `usePopper` hook, render props, portals, and typings

## What changed in the conversion

These files were MDX pages rendered by a Gatsby site. Converting them to plain
Markdown meant dropping the parts that only existed at build time:

- Frontmatter (`navigationLabel`, `order`, `redirect_from`) — replaced by a
  regular `# Heading` on each page
- Interactive demo components (`<OffsetDemo>`, `<FlipDemo>`, and the tutorial's
  `<ResultN>` embeds) — these needed a live React runtime. The surrounding
  prose and code samples that explain each behaviour are unchanged
- Ad placeholders, and the `__UNPKG_CDN_URL__` build variable, which is now
  written out as `https://unpkg.com/@popperjs/core@2`

Internal links were repointed at the corresponding `.md` files, since the old
site served every page at a directory URL. All code samples are preserved
verbatim.
