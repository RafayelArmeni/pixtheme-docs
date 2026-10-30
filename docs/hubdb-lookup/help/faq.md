# FAQ and troubleshooting

??? question "The agent says it can't find the information."

    Check that the data is in a **published** HubDB table. Draft tables and unpublished changes aren't visible. Clear table and column names help the agent pick the right table, and a line in the agent's instructions helps too, for example "Product prices are in the HubDB table Products".

??? question "Install fails with \"your account lacks access to the required scopes [hubdb.rows.read, hubdb.tables.read]\"."

    The HubSpot account doesn't have HubDB, or your user can't grant access to it. HubDB comes with **Content Hub Professional or Enterprise** (or CMS Hub Professional or Enterprise). Check that **Content › HubDB** opens in the account. If it does, ask a Super Admin to install the app, or to give your user HubDB and app install permissions.

??? question "Install fails with \"the app developer has not signed the acceptable use policy\"."

    This was a setup step on our side and is fixed. If you still see it, email [support@pixtheme.com](mailto:support@pixtheme.com).

??? question "The agent shows \"HubDB Lookup is not connected to this HubSpot account\"."

    The app isn't installed in this account, or it was uninstalled. [Install the app](../getting-started/install.md) again.

??? question "The agent fails with \"The agent configuration references actions that no longer exist\"."

    The app was uninstalled and reinstalled, so the agent still points to the old tools. Open the agent, remove the HubDB Lookup tools, add them again and save.

??? question "A filter on a select column finds nothing."

    Use one of the column's options, by label or name. The agent sees the options in **List HubDB tables**. A value that isn't an option matches nothing.

??? question "Sorting by price puts the rows in the wrong order."

    The column is probably a text column. Text sorts alphabetically, so "900" comes after "1,250,000". Change the column to a number column.

??? question "Can the app change my HubDB tables?"

    No. It only has read access to HubDB tables and rows.

??? question "Can the app see my contacts or deals?"

    No. It has no access to CRM data or any other part of HubSpot.

??? question "How many rows can a search return?"

    Up to 50 per search, 10 by default. Very long results are shortened, and the result says how many rows matched in total.

??? question "Does it work with tables used for dynamic pages?"

    Yes. Rows also show their page path, so the agent can point to the page.
