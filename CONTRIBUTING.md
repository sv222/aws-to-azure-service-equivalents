# Contributing

Thank you for helping keep this comparison accurate and current. This guide explains how the table is organized and what to check before you propose a change.

## Table format

The README has one H2 section per category. Each section holds a single table with four columns:

```
| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
```

## Row rules

- Use one service per row. Do not combine several services in one cell.
- Use official, current product names from AWS or Microsoft documentation.
- Write the description as one sentence that ends with a period.
- If a product was retired or renamed, state the change and its date in the description, for example "Retired on December 31, 2022."
- Add a row only when you can verify both sides against official AWS or Microsoft documentation.
- Do not add links that you have not checked.
- Keep the Category cell identical to the section heading.

## Proposing a change

- Open an issue to report an error, retire a row, or suggest a service you are unsure about.
- Open a pull request for a change you can document. Link the official sources in the pull request description.
- Keep pull requests small. Each one should address one concern, such as a single renamed product or a single new category row. Split unrelated edits into separate pull requests.

## Commit messages

Use Conventional Commits for one-line subjects, at 72 characters or fewer. Common types for this repository are:

- `docs:` for table content changes, such as `docs: rename Azure Data Factory row to current name`
- `fix:` for corrections to an existing row
- `ci:` for changes to workflows under `.github/`

## Link checks

The Link check workflow runs on pushes to `main`, on pull requests, and weekly. If a link fails only because the site blocks automated requests or requires sign-in, add a pattern for it to `.lycheeignore`, with a comment above it that explains why.

## License

By contributing, you agree that your contributions are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
