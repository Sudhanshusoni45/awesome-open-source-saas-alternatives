# Contributing

Thanks for helping build this collection. The list starts empty; add categories and SaaS products only when there is a project to list under them.

## Suggest a project

Open an issue using the **Suggest an alternative** form. Include the paid SaaS product it replaces, its category, the alternative's name, source code URL, license, and a short description.

Submissions are reviewed by the maintainer before they are added.

## Open a pull request

1. Edit [`data.json`](data.json). The top-level array contains one object per SaaS product. Add an alternative to an existing product, or create a product entry if needed.
2. Update the **Alternatives** section in [`README.md`](README.md) to match. Group entries under category headings, then SaaS product headings. Use a table with **Alternative**, **Description**, and **License** columns; link each alternative to its source code.
3. Check that the JSON is valid, links work, and no duplicate projects were added. Keep unrelated edits out of the pull request.

## Data format

Each SaaS product has these fields:

| Field | Format | Purpose |
| --- | --- | --- |
| `slug` | String | Unique lowercase identifier with hyphens between words. |
| `name` | String | Name of the SaaS product being replaced. |
| `category` | String | Category used to group the listing. |
| `description` | String | A short explanation of what the SaaS product does. |
| `alternatives` | Array | One or more open source alternatives. |

Each object in `alternatives` has these fields:

| Field | Format | Purpose |
| --- | --- | --- |
| `name` | String | Name of the open source project. |
| `repo` | String or `null` | GitHub repository in `owner/repository` format. Use `null` for projects hosted elsewhere. |
| `url` | String, optional | HTTPS source code URL, required when `repo` is `null`. |
| `description` | String | A factual, single-sentence description of up to 160 characters. |
| `license` | String | License identifier, verified against the project's license file. |

## Listing criteria

- The project has public source code and an open source license.
- It is a practical alternative to a paid or freemium SaaS product.
- The source repository is accessible and is not archived.
- Descriptions explain what the project does without promotional claims.
- Self-hosting and feature claims are checked against the project's documentation.
- A project appears only once under each SaaS product it replaces.
