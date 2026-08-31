# obilourdes.com

Website for **Lourdes Work Corporation**. Marketing consulting, and digital
guides and tools.

Plain HTML and CSS. No framework, no build step, no dependencies. Edit a file,
commit, and GitHub Pages publishes it.

## Files

| File | What it is |
|---|---|
| `index.html` | Home page |
| `terms.html` | Terms of service |
| `privacy.html` | Privacy policy |
| `refunds.html` | Refunds and cancellations |
| `thanks.html` | Landing page after the contact form is submitted without JavaScript |
| `styles.css` | All styling, including the design tokens at the top |
| `fonts/` | Self-hosted Newsreader and Geist |
| `CNAME` | Tells GitHub Pages to serve this at obilourdes.com. Do not delete. |

## Editing

Open any `.html` file in a text editor. The copy is plain text between the
tags. To change colours, spacing or type sizes, edit the `:root` block at the
top of `styles.css`; every value used on the site is defined there once.

To preview locally before committing:

```bash
python3 -m http.server 4173 --directory .
```

Then open <http://localhost:4173>.

## Design rules this site follows

Kept here so future edits do not quietly break the look.

- **No pure white and no pure black.** Page is warm paper, text is warm
  near-black. Both are defined as tokens.
- **One accent colour** (deep muted green) used identically everywhere.
- **One corner radius** (3px) on every element.
- **Serif for headings only** (Newsreader), grotesque for everything else
  (Geist). Do not mix a second serif in.
- **No em-dashes anywhere in visible text.** Use a normal hyphen, a comma, or
  a second sentence.
- **Both light and dark themes** are defined. Any new colour needs a value in
  both, or it breaks for half of visitors.

## Compliance notes

Two reviewers read this site, so some content is not decorative.

**Stripe** requires the business name, a description of what is sold, a
customer service contact, and a refund and cancellation policy, all publicly
reachable without a password. Those live on the home page, in the footer of
every page, and on `refunds.html`.

**The contact form is the only customer service channel.** No email address
appears anywhere on the site, deliberately, to keep it away from scrapers.
Stripe accepts a contact form for this, but it means the form breaking is the
same as having no contact method at all. If you change the form, test that a
real message arrives before pushing. The access key is in `index.html`; it is
public by necessity, so restrict it to obilourdes.com in the Web3Forms
dashboard.

**The site carries no income claims, no earnings figures and no guaranteed
results, deliberately.** Stripe's restricted business list covers schemes
promising high reward for little effort, and marketing and course businesses
get declined for copy that reads that way. The "no guarantee of results"
sections on the home page and in the terms are there on purpose. Do not
replace them with performance claims.

**Google** requires the home page, privacy policy and terms URLs for OAuth app
verification, on a domain verified in Search Console.

If the business changes what it sells, update the descriptions here and the
description given to Stripe together. A mismatch between the two is a common
cause of account review.
