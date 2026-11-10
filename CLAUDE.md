# Popcorn Files website: project notes for Claude

Read this before making changes. It records what the founders decided while building the site, so new sessions don't undo past decisions.

## What Popcorn Files is
A small new studio that builds AI automation for marketing, branding, web and video agencies (roughly 5–30 people) in Bengaluru, Mumbai and Delhi NCR.

Core offer: **Enquiry-to-Client Autopilot**. New enquiries are saved to the CRM, a reply is drafted for a human to approve, follow-ups get reminders, and new clients are onboarded automatically. **A person always approves anything a client sees.**

Engagement path: quick chat (30 min) → workflow check (1–2 weeks) → build and test / pilot (3–6 weeks) → go live, with an optional monthly care plan.

## Site structure
One file: `index.html`. Pages are views switched by the URL hash:

| Hash | Page |
|---|---|
| `#home` (or none) | Home |
| `#services` | Services |
| `#how-it-works` | How it works |
| `#about` | About |
| `#mag` | Popcorn Mag (blog + The Weekly Crunch) |
| `#guide-automate-first` | Sample guide article |
| `#contact` | Contact form |

Menu order: Home · Services · How it works · About · Popcorn Mag · Let's talk. There's a separate phone menu (`#mmenu`). Update both when adding pages, plus the `names` map in the router script.

## Brand decisions (keep these)
- **Font:** Plus Jakarta Sans only. The founders rejected serif italics, handwriting fonts and quirky display fonts as hard to read or "AI-looking".
- **Colours:** cream paper background `#FFF9EE`, ink `#16130F`. Accents: red `#FF4B33`, blue `#2D5BFF`, yellow `#FFC83D`, pink, mint. **Prefer pastel tints** (`--pink-soft`, `--mint-soft`, `--yellow-soft`, `--blue-soft`, `--red-soft`) for large areas. Bright colours only for buttons, small highlights and headline words. **Light mode only, no dark mode.**
- **Style:** clean and professional but creative. Soft shadows, large rounded corners. No hard black "sticker" shadows, no dotted backgrounds, no doodles.
- **Icons:** simple line SVG icons. **Never use emojis as icons.**
- **Numbering:** numbered steps only on the How it works journey. Don't number other sections.
- **Mascot: Kernel**, an original cute popcorn bucket (red/cream stripes, big shiny eyes, blush, mitten hands). Drawn in JS (`build()` in the mascot script) and placed with `<div class="mascot" data-m="...">`. Options are `head`, `wave`, `folder`. Never give him more than two hands. Animations: blink, bob, eyes follow the cursor, popcorn pops and a click burst in the home hero. The founders love Kernel. Keep him.
- **Copy:** plain, simple English. Story-driven, not jargon. Mention "AI" sparingly.

## Honesty rules (from the business plan)
- No invented clients, testimonials, results or numbers.
- Example names (Meera, Riya, Arjun, Neha, Hartwell Foods) are fictional and labelled "Example" or "Sample".
- Don't name real founders or team size (the founders asked for this). Team is shown as roles with Kernel avatars.
- Weekly Crunch posts are samples. Replace them with real news; never publish made-up news about real products.

## Known to-dos before launch
- Contact form is not connected (it shows a "preview" message). Connect it to Formspree, Web3Forms, Netlify Forms or similar.
- Replace sample Weekly Crunch items with real ones.
- Add real work, demo screenshots or video to Services and "Selected work".
- Confirm: "We'll reply within two working days", "New guides every two weeks", 30-minute quick chat, and the "Why Popcorn?" story on About (written as a placeholder).
- Check add-ons (WhatsApp/Instagram, proposals, reports, call notes) and creative AI tools are things the team can deliver now.
- Fonts load from Google Fonts. Everything else is self-contained.
