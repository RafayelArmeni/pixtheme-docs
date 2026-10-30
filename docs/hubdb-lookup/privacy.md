# Privacy policy

**HubDB Lookup app** · Effective October 30, 2026

This policy explains what the HubDB Lookup app for HubSpot ("the app") accesses, stores and shares. The app is made by Pixtheme ("we"). Questions: [support@pixtheme.com](mailto:support@pixtheme.com).

## Summary

* The app only **reads** HubDB tables and rows. It can't change them and can't see any other HubSpot data.
* It doesn't keep copies of your table data. Rows are read when a tool runs and passed straight back to HubSpot.
* It stores one thing per account: the access keys HubSpot issues when you install it.
* We don't sell data, share it for advertising or use it to train AI models.

## What the app accesses

When you install the app, you grant it two HubSpot permissions:

* `hubdb.tables.read`: read the names, ids and columns of your HubDB tables.
* `hubdb.rows.read`: read the rows of your HubDB tables.

The app reads this data only when one of its tools runs, which happens when a Breeze agent or a workflow in your account uses it. It reads only the published version of your tables.

## What HubSpot sends to the app

Each time a tool runs, HubSpot sends the app:

* your HubSpot account id
* the tool's inputs, such as the table name, the filters, the columns, the sort order and the number of rows
* the id of the record the agent or workflow is working on, if any (for example a contact id). The app doesn't use it and doesn't read that record.

## What the app stores

| Data | Where | How long |
|---|---|---|
| OAuth access and refresh tokens for your account, and the install date | Cloudflare Workers KV | Until you uninstall the app. Deleted within one day after you uninstall. |
| Operational logs: account id, tool inputs listed above, number of rows returned, errors | Cloudflare Workers Logs | 7 days |

The logs don't contain your table rows. They can contain the text of filters, for example `city = Austin`, because filters are tool inputs. We use logs only to keep the app working and to fix problems.

HubDB table data that a tool returns isn't stored by the app. HubSpot keeps the results in your account as part of the agent's or workflow's history, under HubSpot's own policies.

## Service providers

* **Cloudflare, Inc.** hosts the app and stores the tokens and logs. See [Cloudflare's privacy policy](https://www.cloudflare.com/privacypolicy/).
* **HubSpot, Inc.** runs your account, the agents and the workflows. See [HubSpot's privacy policy](https://legal.hubspot.com/privacy-policy).

We don't share data with anyone else, except where the law requires it.

## Security

* Every request from HubSpot is checked against HubSpot's signature before the app does anything.
* Tokens are stored per account, sent only to HubSpot over HTTPS, and never shown in logs.
* Access to the hosting account is limited to Pixtheme.

## Your choices

* **Uninstall** the app at any time in HubSpot under **Settings › Integrations › Connected apps**. Access stops right away, and the stored tokens are deleted within one day.
* **Ask** us what we hold about your account, or ask us to delete it, at [support@pixtheme.com](mailto:support@pixtheme.com). We answer within 30 days.

## Children

The app is for businesses using HubSpot and isn't meant for children.

## Changes

If this policy changes, we update this page and the date at the top. Significant changes are also listed in the [changelog](help/changelog.md).
