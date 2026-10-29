# FAQ and troubleshooting

??? question "My listings page says to choose a table"

    Click the **Property Listings** module and choose your table under **Properties table**. The message only shows in the editor.

??? question "Property pages show a 404"

    Check that the page's **Settings › Advanced › Dynamic pages** data source is your Properties table, that **Enable creation of dynamic pages** is on in the table settings, and that the table is **published**.

??? question "The Buy/Rent filter or status badges look wrong"

    Check the `status` column is a **Select** column with the options For sale, For rent, Sold, Under offer and Coming soon, and that every row has a status.

??? question "The map doesn't show"

    Add a `location` column of type **Location** to your table and set a location for each row. See [Map pins](../getting-started/hubdb.md#map-pins).

??? question "Properties don't show their agent"

    Choose your Agents table in the **Property Details** module, and make sure the property's `agent` column has the agent's **page path** (for example `daniel-reyes`), not their name.

??? question "Prices show the wrong currency"

    Set **Currency**, **Currency position** and **Thousands separator** in **Theme settings › Property listings**.

??? question "Can I import listings from my MLS?"

    Openhouse doesn't include an MLS or IDX feed. You can import a CSV into HubDB at any time, or [contact us](support.md) about a custom sync.

??? question "Do I need Content Hub Professional?"

    Only for automatic property, agent and neighborhood pages from HubDB. On Starter, use the typed-in modules. See [Content Hub Starter](../getting-started/build-your-site.md#content-hub-starter).
