# How searching works

Agents fill in the search for you. This page explains what they can ask for, which also helps when you use **Search HubDB table** in a workflow or check why an answer looks wrong.

## Search fields

| Field | What to enter | Example |
|---|---|---|
| **Table** | The table's name, label or id | `store_locations` |
| **Filters** | One condition per line: column, operator, value | `city = Austin` |
| **Columns to return** | Optional. Column names, separated by commas. Empty means all columns | `name, city, phone` |
| **Sort by** | Optional. A column name. Start with `-` for highest first | `-price` |
| **Maximum rows** | Optional. Default 10, maximum 50 | `3` |

Columns can be named by their name or their label, and capitals, spaces and underscores don't matter: `open_saturday`, `Open Saturday` and `open saturday` all work. Use `name` for the row's name.

## Filter operators

| Operator | Meaning | Example |
|---|---|---|
| `=` | Equals | `status = For sale` |
| `!=` | Doesn't equal | `status != Sold` |
| `>` `>=` `<` `<=` | Greater or smaller | `beds >= 3` |
| `contains` | Text contains, ignoring capitals | `name contains cottage` |
| `not contains` | Text doesn't contain | `city not contains San` |
| `starts with` | Text starts with | `name starts with Dallas` |
| `in` | Any of several values, for select and number columns | `type in House, Townhouse` |
| `not in` | None of several values | `status not in Sold, Under offer` |
| `is empty` | No value | `photo is empty` |
| `is not empty` | Has a value | `phone is not empty` |

All filters must match. For "this **or** that" on a text column, the agent runs one search per value.

## Values by column type

| Column type | How to write the value |
|---|---|
| Select, multi-select | The option's label or name: `For sale` or `for_sale`. On multi-select, `=` means the row has that option |
| Boolean (checkbox) | `yes` or `no` (`true`, `false`, `1` and `0` also work) |
| Number, currency | Plain numbers. Currency signs and commas are ignored: `$1,250,000` |
| Date, date and time | `YYYY-MM-DD`, for example `2026-11-15` |
| Text, rich text | Any text |

## What the agent gets back

Each matching row comes back as text: its name, its page path for dynamic pages, and the requested columns. Values are made readable:

* Select options show their label.
* Checkboxes show `yes` or `no`.
* Dates show as `YYYY-MM-DD`.
* Images show their URL.
* Rich text loses its HTML formatting, and long values are shortened to 300 characters.

When more rows match than were returned, the result says so, for example "Showing 10 of 24". The agent can then narrow the search or ask for more rows.

## Finding tables

**List HubDB tables** returns every published table with its name, id, number of rows and columns. The agent can pass a word to only list matching tables. If no table name matches, it gets all tables instead, so it can still choose.
