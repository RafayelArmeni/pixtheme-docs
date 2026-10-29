# Forms and leads

Openhouse uses your own **HubSpot forms**, so every inquiry, valuation request and contact message creates or updates a contact in your CRM. You choose the form in each module.

## Where the forms are

| Page | Module | Suggested form |
|---|---|---|
| Property pages | **Property Details** › Inquiry form | Property inquiry: first name, email, phone, message |
| Sell your home | **Form Section** | Home valuation: name, email, phone, address, postal code, home type |
| Contact | **Contact Section** | Contact: name, email, phone, "I'm looking to…", message |
| Single agent and commercial homes | **Form Section** | Contact (the same form works) |
| New development home | **Form Section** | Register interest: name, email, phone |

Create the forms in **Marketing › Forms**, then click the module in the page editor and choose the form. The theme styles every form to match your colors and fonts.

## Know which property each lead asked about

HubSpot already records the page of every form submission on the contact's timeline. To also save the property on the contact record, so you can use it in lists, workflows and notifications, add a hidden field:

1. Go to **Settings › Properties** and create a contact property: label **Property of interest**, internal name `property_of_interest`, field type **Single-line text**.
2. Open your property inquiry form, add **Property of interest**, and make it a **hidden field**.
3. In the **Property Details** module, check that **Hidden field for the property** says `property_of_interest`. It's already filled in.

The theme fills the hidden field with the property's name and address, for example *Classic porch home – 1458 Sanchez Street, Noe Valley, San Francisco*.

!!! tip "Lead notifications"

    Create a workflow that sends the property's agent an email when a contact submits the inquiry form, including the **Property of interest** value.

## Book a viewing

Each agent can have a **meeting_link** in the Agents table, for example a HubSpot meetings link. Property pages then show a **Book a viewing** button that opens the agent's calendar. If the agent has no link, the button uses the **Viewing link when the agent has no meeting link** setting.

## More contact properties (optional)

The demo forms also use **Looking to** (buy, sell, rent or invest) and **Home type** (dropdowns). Create them the same way if you want them in your forms and reports.
