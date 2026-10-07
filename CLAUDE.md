# Sheryl-Slides

A collection of standalone HTML presentations, published with GitHub Pages from
`main` at the repository root.

## Adding a presentation — required steps

Publishing a deck is **two** changes, not one. A deck that is committed but
missing from the README is invisible to anyone reading the repo.

1. Add the deck itself:
   - a single self-contained `<name>.html` at the repository root, or
   - a directory `<name>/` if it needs companion files.
   - Images and other assets go in a sibling `<name>-assets/` directory.
2. **Add a row to the Presentations table in `README.md`.** Never skip this.

### Row format

```markdown
| `<file-or-dir>` | <Title — Subtitle> | [Open](https://sheryl-shiyi.github.io/Sheryl-Slides/<path>) |
```

- **File** column: the filename or directory in backticks, exactly as committed.
- **Topic** column: the deck's own title, and its subtitle when there is one.
  Write what the talk is about — not a restatement of the filename.
- **Public Link** column: always the literal text `Open`, pointing at the
  Pages URL. For a directory deck the URL must include the entry HTML file
  (for example `red-hat-maas/red-hat-maas.html`), except where an `index.html`
  makes the bare directory work.
- Append new rows at the bottom of the table.

### Before committing

Check that every root-level `.html` and every published directory has a row in
the table, and that each Pages URL resolves once Pages has rebuilt.

## Conventions

- Decks are zero-dependency: inline CSS and JS, no build step, no npm.
- Filenames are kebab-case.
- Decks may be public. Before committing one that came out of customer work,
  confirm what has to be genericised — customer names, product names,
  internal hostnames, cluster URLs and namespace names.
