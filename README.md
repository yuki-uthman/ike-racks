# Ike Racks

A single static page showing **how many 2C and RD8 racks MRH Investment sold,
month by month** (Jan – 15 Oct 2026), per rack type and height. Same look as
[ike-po](https://github.com/yuki-uthman/ike-po). No secret, no cron, no build step.

## What is counted

- Composite racks only (Single Side, Double Side, End Rack) in 2C Black/White and
  RD8 Gray/White. Loose parts, shelves, clips, nets and price borders are not racks.
- Also shown: the **Lui Kaana Haru** wood vegetable racks (Small 4 Layer, Medium 5 Layers), and the **Vegetable Rack 4 Square Baskets** and the **Trolley Stand 5 Layer** (Black, White; a Zoho item with no colour is taken as black); one piece = one rack, Zoho paid + Odoo confirmed sales.
- Each bay is one rack: a set sold as "x5" counts as 5.
- Racks of different heights are separate rows and are never added together
  (2C 1800/2000mm, RD8 1550/1950mm).
- Zoho: paid invoices (status Closed, balance 0), 1 Jan – 26 Aug 2026, by invoice date.
  Odoo: confirmed sales from 27 Aug 2026 with suspected duplicates held out.
- Left out until confirmed: round-shelf end racks, add-on bays. One row,
  Zoho "2C Mart Rack End White 5ft", has no clear height and is shown on its own.

## Data

The numbers are a **snapshot embedded in `index.html`** (`var DATA`). They do not
refresh by themselves. Source workbook: `odoo/rack_sales_by_month.xlsx`. A **Graphs | Table** switch sits at the top (`#table` opens the table directly). Each rack has its own vertical bar graph, one bar per month with the
number on top (each graph is scaled to its own highest month).

## One-time setup

GitHub Pages: Settings → Pages → Deploy from a branch → `main`, `/ (root)`.
Page: `https://yuki-uthman.github.io/ike-racks/`.

## Visibility

Free GitHub Pages needs a public repository, so the page is reachable by anyone
with the URL. It shows rack types and counts only: no customer names, prices or amounts.
