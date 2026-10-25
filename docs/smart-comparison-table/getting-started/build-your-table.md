# Build your table

A new Smart Comparison Table starts with a finished example: three pricing plans with section headings, icons and tooltips. Change the example instead of starting from an empty table.

## 1. Heading and text

Under **Heading and text**, set the **Eyebrow** (small label), **Heading** and **Intro text**. Leave any of them empty to hide it.

* **Heading level:** use **H2** in most cases. Use **H1** only if the table is the main heading of the page.
* **Alignment:** left or center.

## 2. Columns

Each column is a plan or a product. Under **Columns (plans or products)** you can add 2 to 6 columns and drag them to change the order.

| Field | What it does |
|---|---|
| **Name** | Plan or product name, for example *Professional* |
| **Short description** | One line under the name |
| **Price** and **Price period** | For example `$49` and `/month`. Leave the price empty for product comparisons |
| **Badge** | Small label above the name, for example *Most popular* |
| **Highlight this column** | Adds a border and background in your brand color. Use it for one column |
| **Logo** | Optional logo above the name, shown 32 px high |
| **Button** | Text, link and style (filled or outline). Leave the text empty to hide the button |

## 3. Rows

Under **Rows**, each row is either a **Feature row** or a **Section heading**. Section headings group the rows below them, for example *Core features* or *Support*.

For a feature row, fill in:

* **Label:** the feature name, for example *Storage*.
* **Tooltip:** optional extra explanation. Visitors see it when they hover, tab to or tap the small **i** button.
* **Values:** one value per column, in the same order as your columns, separated by `|`.

### Writing values

| You type | Visitors see |
|---|---|
| `yes` | Check icon (*Included*) |
| `no` | Cross icon (*Not included*) |
| `partial` | Half-filled icon (*Partly included*) |
| `-` | A dash (*Not applicable*) |
| Any other text, like `10 GB` or `24/7` | The text |

Example for a table with three columns:

```
yes | yes | no
3 users | 10 users | Unlimited
Email | Email and chat | Dedicated manager
```

!!! warning "Type `-` for an empty cell"
    Don't leave a value blank in the middle of a row, like `yes | | no`. HubSpot removes empty values, so the values after it would move one column to the left. Type `yes | - | no` instead.

Matching is not case sensitive, so `Yes` and `YES` work too. `✓`, `y` and `true` also show a check, and `✗`, `x` and `false` show a cross.

## 4. Publish

Preview the page on desktop and on a phone, then publish. Next, see the [table options](../customize/table-options.md) and [style settings](../customize/style.md).
