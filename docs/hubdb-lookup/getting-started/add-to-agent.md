# Add the tools to an agent

1. Open the agent in **Breeze › Agents** and click **Edit**.
2. In the agent's tools, add **List HubDB tables** and **Search HubDB table**. Both are listed under **HubDB Lookup**.
3. Save, then try the agent with a question about your data.

Add both tools. The agent uses **List HubDB tables** to find the right table and its exact column names, then **Search HubDB table** to get the rows.

## Tips for good answers

* **Name tables and columns clearly.** The agent picks tables by their names and labels. A table called `store_locations` with a column `open_saturday` is easy to find. A table called `table_3` with a column `col_b` isn't.
* **Use select columns for fixed choices.** Status, type, category and similar values work best as select or multi-select columns. The agent sees the allowed options and filters on them exactly.
* **Use number columns for numbers.** Prices, bedrooms and ratings stored as numbers can be compared (`price <= 500`) and sorted. Numbers stored as text can't.
* **Publish your tables.** The tools read the published version only.
* **Mention it in the agent's instructions** if a topic always lives in HubDB, for example: "Store hours and services are in the HubDB table Store locations."

## Use the tools in a workflow

Both tools are also workflow actions. Add **Search HubDB table** to a workflow, fill in the table and filters, and use the **Matching rows** output in later actions, such as an email or a property update.

Next: [how searching works](../guides/searching.md).
