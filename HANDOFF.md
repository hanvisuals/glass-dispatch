# HANDOFF — Ideal Glass Studios Newsletter

## What this is
A custom-coded HTML email newsletter for **Ideal Glass Studios** ("The Glass Dispatch").
File: `index.html` (also serves as the web-hosted preview).

## Design
- Monochrome, chic: white sheet floating on light grey frame, black type, no color accent.
- Type: Bodoni Moda (display) / Archivo (body) / Space Mono (meta: dates, runtimes, labels).
  Outlook falls back to Georgia + Helvetica. Web fonts load via Google Fonts <link>.
- Mixed media: landscape PHOTOS + vertical (9:16) YouTube SHORTS shown as clickable
  thumbnails with mono runtime captions (email can't play video inline).
- Aesthetic direction: editorial, flash/grain, anti-corporate. No em dashes anywhere.

## Structure (sections, top to bottom)
Masthead → subscribe-catcher bar → hero photo → featured Short (vertical thumb + text,
"Subscribers first") → Upcoming events (mc:repeatable list) → Shorts row (2 vertical videos)
→ In the Studio (photo + text) → "Forward this issue" block → black CTA band (Book the space)
→ footer (social + merge tags).

## Built for list growth (priority = grow the email list, NOT drive traffic to YouTube)
- Subscribe-catcher for forwarded readers (needs real signup form URL).
- Forward-to-friend in two places (uses *|FORWARD|* in the Mailchimp version).
- Short framed as subscriber-first (retention).
- Event "RSVP + bring one" referral hook.

## Current state / TODO
1. **Deploy to GitHub Pages** to show managers: repo with `index.html` at root, add empty
   `.nojekyll`, enable Pages (Settings > Pages > main / root). Use trailing slash on the URL.
   (Past 404 issues came from missing index at root / no trailing slash.)
2. **Swap placeholder images**: currently picsum.photos. Replace with real Ideal Glass photos
   (landscape for photo slots, 9:16 for Shorts). Grayscale+contrast filter is CSS-only
   (works in browser + webmail, ignored by Outlook) — for guaranteed grain, export B/W assets.
3. **Real Short data**: replace `https://youtube.com/shorts/REPLACE_ME` links and the mono
   runtimes (0:52 etc.). Best move: export short looping GIFs of each Short as the thumbnails.
4. **Real links**: `SIGNUP_FORM_URL`, social URLs, and the `mailto:hello@idealglass.studio` CTA.

## Email platform decision (still open)
- **Mailchimp**: custom HTML needs the paid **Standard** plan; free tier is now 250 subs /
  500 emails/month / no automation. Poor fit for a growth play.
- **EmailOctopus (recommended)**: free = 2,500 subs / 10,000 emails/mo, "Code your own"
  editor accepts the full pasted HTML, custom fonts work only in that editor.
- **Brevo (alt)**: unlimited contacts but 300 emails/day cap; has HTML custom-code editor too.
- When a platform is chosen: the DESIGN is 100% portable, but swap the required merge tags
  (unsubscribe etc.) and drop the Mailchimp-only `mc:edit` / `mc:repeatable` attributes.

## Working preferences
Fast execution over long explanation. Specific + actionable, not generic. No em dashes.
Casual Turkish is fine in chat; client-facing copy stays in English.
