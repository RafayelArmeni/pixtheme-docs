# Set up your listings (HubDB)

Openhouse keeps your properties, agents and neighborhoods in three **HubDB tables**. HubDB is a spreadsheet-like database built into HubSpot (**Content › HubDB**). Each row becomes a card on your listings page and, on Content Hub Professional, its own page.

A HubSpot theme can't create tables in your account, so you create them once, with our templates. It takes about 15 minutes.

| Table | Used for |
|---|---|
| **Properties** | Listings page, property pages, featured homes, similar homes |
| **Agents** | Agents page, agent profile pages, the agent box on each property |
| **Neighborhoods** | Neighborhoods page, area guides, home counts per area |

You only need the Properties table to start. Agents and Neighborhoods are optional: without them, type agents and areas into the Agent Cards and Neighborhood Tiles modules instead.

## Download the templates

Each CSV has the demo content (12 homes, 4 agents, 4 neighborhoods) so you can see everything working, then replace it with your own.

* [openhouse-properties.csv](../assets/downloads/openhouse-properties.csv)
* [openhouse-agents.csv](../assets/downloads/openhouse-agents.csv)
* [openhouse-neighborhoods.csv](../assets/downloads/openhouse-neighborhoods.csv)

The demo photos are hosted by Pixtheme for your preview. Replace them with your own photos before you go live.

## Create a table from a CSV

Repeat these steps for each table. Start with **Properties**.

1. Go to **Content › HubDB** and click **Create table**.
2. Enter a **Table label** (for example *Properties*) and a **Table name** (for example `properties`). You can't change the name after publishing.
3. In the new table, click **Actions › Import**, upload the CSV and click **Next**.
4. On the **Map columns** page:
    * Map **name** to **Name** and **page_path** to **Page path**.
    * For every other CSV column, click **Add column** and give it **the same name** as the CSV column, with the type from the tables below.
5. Finish the import and check the rows.
6. Click **Actions › Manage settings**, turn on **Enable creation of dynamic pages using row data**, and save.
7. Click **Publish**.

!!! warning "Use the exact column names"

    The theme finds your data by column name, so use the names exactly as they appear in the CSV (`price`, `main_image`, `open_house`…). Labels can be anything you like.

### Properties columns

| Column | Type | What it does |
|---|---|---|
| `status` | Select | Options: **For sale**, **For rent**, **Sold**, **Under offer**, **Coming soon**. Drives the badge and the Buy/Rent filter |
| `property_type` | Select | Options such as **House**, **Apartment**, **Townhouse**, **Land**, **Office**, **Retail**. You can add your own types |
| `price` | Number | Shown with your currency settings. Leave empty to show "Price on request" |
| `price_suffix` | Text | For example `/month` for rentals |
| `beds`, `baths`, `parking`, `year_built` | Number | Key facts. Empty values are hidden |
| `area` | Number | Floor area |
| `area_unit` | Text | Optional. Overrides the area unit from theme settings for this home |
| `address`, `city` | Text | Shown under the title and searched by the location filter |
| `neighborhood` | Text | Must match the **name** of a row in your Neighborhoods table, for example `Noe Valley` |
| `location` | Location | Map pin on the property page (see below) |
| `summary` | Text | One or two sentences for cards and search engines |
| `description` | Rich text | The full description on the property page |
| `features` | Text | Separate features with commas: `Garden, Fireplace, Garage` |
| `main_image` | Image | The card photo and first gallery photo |
| `photo_2` … `photo_6` | Image | More gallery photos |
| `floor_plan` | Image | Floor plan image |
| `video_url` | URL | YouTube or Vimeo video tour |
| `badge` | Text | Extra badge, for example `New` or `Open house Sat 11–2` |
| `open_house` | Text | Open house date and time, shown in a box on the property page |
| `featured` | Boolean | Featured homes show first and in "Featured properties" sections |
| `agent` | Text | The **page path** of the agent in your Agents table, for example `daniel-reyes` |

### Agents columns

| Column | Type | What it does |
|---|---|---|
| `role` | Text | For example `Senior agent, Noe Valley` |
| `photo` | Image | Portrait photo, about 5:6 |
| `phone`, `email` | Text | Call and email buttons |
| `bio` | Rich text | Profile page text |
| `languages`, `areas` | Text | Shown on the profile page |
| `meeting_link` | URL | Your HubSpot meetings link. Powers the **Book a viewing** button on property pages |
| `sort_order` | Number | Lower numbers show first |

### Neighborhoods columns

| Column | Type | What it does |
|---|---|---|
| `image` | Image | Tile and guide photo, portrait works best |
| `summary` | Text | Short intro |
| `description` | Rich text | The full area guide |
| `location` | Location | Map on the area guide |
| `highlights` | Text | Separate highlights with commas |
| `sort_order` | Number | Lower numbers show first |

## Map pins

The `location` column isn't in the CSV files. After the import, add a column named `location` of type **Location**, click a cell and search for the address. The map shows on the property page and area guide once a location is set.

## After the import

Open the table and check:

* **status** and **property_type** show options (not empty cells).
* **featured** is ticked for the homes you want to highlight.
* Images show thumbnails.

If a column came in empty, fill it in directly in the table. Then click **Publish**.

## Adding and editing properties

Edit the Properties table like a spreadsheet: click **Add row**, fill in the cells, then **Publish**. New rows appear on your listings page and get their own page automatically. The row's **Page path** is added to your listings page's address, for example `/listings/classic-porch-home-noe-valley`. Use lowercase words and dashes.

!!! tip "Use the HubSpot CLI instead"

    Developers can create each table with columns, options and demo rows in one command, using our table definitions: [properties](../assets/downloads/openhouse-properties.json), [agents](../assets/downloads/openhouse-agents.json), [neighborhoods](../assets/downloads/openhouse-neighborhoods.json).

    ```
    hs hubdb create --path openhouse-properties.json
    ```

## Limits

* Filters and sorting run in the visitor's browser on up to 500 properties. That's plenty for most agencies.
* Next: [Build your site](build-your-site.md).
