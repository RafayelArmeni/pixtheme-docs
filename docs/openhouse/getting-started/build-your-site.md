# Build your site

Create each page with **Content › Website pages › Create**, choose the Openhouse template, then edit the text and photos in the page editor. The demo content is already in place, so every page looks finished from the start.

## Recommended pages

| Page | Template | Suggested address |
|---|---|---|
| Home | **Home** (or one of the other home designs) | `/` |
| Listings and property pages | **Property listings and property pages** | `/listings` |
| Agents and profiles | **Agents and agent profiles** | `/agents` |
| Neighborhoods and guides | **Neighborhoods and neighborhood guides** | `/neighborhoods` |
| Sell your home | **Sell your home** | `/sell` |
| About | **About** | `/about` |
| Contact | **Contact** | `/contact` |

## Connect the HubDB pages

The listings, agents and neighborhoods templates each make **two kinds of page from one page**: the list (for example all properties) and a page for every row (each property).

1. Create the page with the template, for example **Property listings and property pages**.
2. Open **Settings › Advanced › Dynamic pages** and choose your table as the **data source**, for example *Properties*.
3. In the editor, click the **Property Listings** module and choose your table under **Properties table**. Set **Property pages** to this page's address, for example `/listings`.
4. Click the **Property Details** module and choose your **Agents table**, so each property shows its agent.
5. Publish. Your list is at `/listings` and each property at `/listings/{page path}`.

Do the same for **Agents** (data source: your Agents table) and **Neighborhoods** (data source: your Neighborhoods table).

!!! note "Why the editor shows every module"

    The editor shows the list modules and the detail modules together, so you can edit both in one place. Visitors only see the list on `/listings`, and only the property modules on a property page.

## Point the other modules to your tables

These modules can also read your tables. Open each one and choose the table:

| Module | Setting |
|---|---|
| **Agent Cards** | **Source**: *My agents table (HubDB)*, then the table and **Agent profile pages** |
| **Neighborhood Tiles** | **Source**: *My neighborhoods table (HubDB)*, the table, **Neighborhood guide pages**, and optionally the **Properties table for the counts** |
| **Home Hero** search bar | **Listings page**: your listings page address |

The home pages show homes with the **Property Cards** module, where you type each home in. To show your HubDB homes instead, replace it with the **Property Listings** module, set **What to show** to *Featured properties only*, and choose your table and property pages. Tick **featured** on the homes you want there.

## Content Hub Starter

Without dynamic pages, build the same site with typed-in content:

* Use **Property Cards** instead of Property Listings to show homes.
* Create one page per property with the **Property listings and property pages** template and fill in **Property (when the page is not connected to HubDB)** in the Property Details module. Hide the Property Listings module on those pages.
* Set **Agent Cards** and **Neighborhood Tiles** to **Typed in below**.

## The other home designs

| Template | Best for |
|---|---|
| **Home** | Agencies with a team and many listings |
| **Home – single agent** | One agent's personal site, with a portrait hero and their own listings |
| **Home – luxury** | High-end homes, with a full-screen photo hero |
| **Home – commercial** | Offices and retail, with a contact form for leasing enquiries |
| **Home – new development** | One project, with gallery, unit types, availability table and register-interest form |

Next: [Header, footer and menus](header-and-footer.md).
