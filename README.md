# Conley General Contractors, Inc. — spec site

Unsolicited demo site built to show Jeffrey Conley what a real web presence for his business could look like, ahead of a cold call. Built with its own visual system rather than the shared sibling template — a "job spec sheet / blueprint" theme (dimension lines, chamfered-corner numbering, architectural title-block info panels) to match a framing/concrete/tile general contractor specifically.

## Real logo

Kyle pasted the business's actual Facebook logo inline (a two-line wordmark: bold gray "CONLEY" over a smaller red "GENERAL CONTRACTORS INC."). No matching image file turned up in `~/Downloads` or `~/Desktop`, and there's no tool that can save inline-pasted image bytes directly to disk, so the exact file couldn't be recovered.

Instead, the site recreates the wordmark as real HTML/CSS text (`.wordmark` in the header/footer) using the **real brand colors** sampled from the pasted image — gray `#58595b` and red `#e2231a` — paired with Big Shoulders Display / Barlow Condensed to approximate the logo's bold industrial feel. This is **not** a pixel copy of the actual custom cut-corner lettering in the real logo (that's a custom font/vector we don't have), just a same-color, same-structure typographic stand-in. If Jeffrey can send the real logo file (from print materials, truck signage, or his own Facebook admin panel), swap it in directly.

## Facts used, and where they came from

- **Business name**: Conley General Contractors, Inc.
- **Owner**: Jeffrey Conley — per BBB
- **Phone**: (740) 961-2104 — per BBB
- **Address**: 1917 Shela Blvd, Portsmouth, OH 45662 — per BBB
- **Founded**: business started November 22, 2021 — per BBB
- **BBB**: A+ rating, accredited since 10/16/2023; 0 reviews listed
- **Services**: residential & commercial framing, electrical, concrete, tile, bathroom & kitchen remodeling, and general home improvements — BBB's own service description, used verbatim as the site's 6 service rows
- **No real website found**: only presence is the BBB profile and the Facebook page (facebook.com/p/Conley-General-Contractors-Inc-100075441270683). A domain called `conleycontractors.com` turned up in search results under a "Project Gallery" title, but it doesn't resolve (DNS lookup fails) — not confirmed to belong to this business at all, so it isn't used as a talking point on the call.
- **No email found** — contact section only lists phone, Facebook, and the BBB-listed address.
- **Service area**: site says "Portsmouth and the surrounding Scioto County area" — inferred from the business's location, not directly confirmed by Jeffrey; worth confirming on the call.

## Open questions for the call

1. Can he send the actual logo file (not just what's on Facebook) so the recreated wordmark can be swapped for the real one?
2. Real service area — just Portsmouth, or wider Scioto County / neighboring counties?
3. Whether he wants a business email set up (none found anywhere) for the contact form to send to.
4. Confirm the 0-reviews BBB listing isn't hiding a Google/Facebook review presence worth featuring.

## Stack

Static HTML/CSS/JS, no build step. Google Fonts: Big Shoulders Display (headings/wordmark) + Barlow Condensed (labels/nav/kickers) + Work Sans (body) — a deliberately different pairing from the Space Grotesk/Inter used on most sibling sites, to match this build's own visual system. Contact form posts to Formspree with a `YOUR_FORM_ID` placeholder — needs a real form ID before it'll send.

Local preview: `python3 -m http.server 8967` (also wired into `.claude/launch.json` as `conley-general-contractors`).

## Next steps to actually launch this for the client

1. Get the real logo file from Jeffrey and swap it in for the recreated text wordmark.
2. Buy a domain (~$12–15/yr) if Jeffrey doesn't already own one.
3. Swap the Formspree placeholder for a real form ID.
4. Confirm service area and whether he wants an email address set up.
5. Deploy (GitHub Pages is what the rest of the pipeline uses).
