# Install the app

1. Open the install link: [hubdb-lookup.hubdb-lookup-worker.workers.dev/install](https://hubdb-lookup.hubdb-lookup-worker.workers.dev/install).
2. Log in to HubSpot if asked, and choose the account you want to connect.
3. Review the access the app asks for and approve it.
4. You'll see **"HubDB Lookup is connected"**. You can close the tab.

The app is now in **Settings › Integrations › Connected apps**.

## What the app can access

| Access | Why |
|---|---|
| Read HubDB tables (`hubdb.tables.read`) | To list your tables and their columns |
| Read HubDB rows (`hubdb.rows.read`) | To search the rows of a table |

That's all. The app can't edit HubDB or read contacts, companies, deals or any other HubSpot data.

## Uninstall

Go to **Settings › Integrations › Connected apps**, open **HubDB Lookup** and choose **Actions › Uninstall**. The tools stop working right away, and agents that use them will show an error until you remove the tools. The app's stored access for your account is deleted within a day.

Next: [add the tools to an agent](add-to-agent.md).
