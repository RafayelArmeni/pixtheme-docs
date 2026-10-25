# FAQ and troubleshooting

??? question "Values show up in the wrong column."

    A value in the middle of the row is empty, like `yes | | no`. HubSpot removes empty values, so the rest move left. Type `-` for an empty cell: `yes | - | no`.

??? question "A row shows a dash at the end."

    The row has fewer values than there are columns. Add a value for every column, in column order.

??? question "The word 'yes' shows instead of a check icon."

    Check the spelling. `yes`, `y`, `true` and `✓` show a check. Text like `yes!` or `yes, with limits` shows as text.

??? question "The sticky bar sits under my site header."

    Set **Table options › Sticky header offset** to your header's height in pixels. Leave it at 0 to detect the header automatically.

??? question "I don't see the sticky bar on my phone."

    The bar is for desktop. On phones the table scrolls sideways with the feature names fixed, or shows cards.

??? question "The 'Show differences only' switch hides nothing."

    Every row has at least one different value, so there's nothing to hide. The switch only hides rows where all columns have the same value.

??? question "The table colors don't match my brand."

    Set **Style › Brand color**, or choose another preset. Custom colors in the Style tab override the preset.

??? question "Can I use several tables on one page?"

    Yes. Each table has its own settings.

??? question "Which pages does the module work on?"

    Website pages and landing pages.
