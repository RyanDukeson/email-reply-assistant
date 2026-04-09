# Email Reply Assistant
### Built by Ryan Dukeson

An AI-powered email reply tool built for reception staff at **Glen Innes Pool & Leisure Centre (The Y / YMCA North, Auckland NZ)**.

Staff paste an incoming customer email, select a topic, and instantly receive three ready-to-send reply options — grounded in the centre's actual terms & conditions, facility info, and class timetables. No typing from scratch, no guessing at policies.

**Live demo:** https://rgdreplyassistant.netlify.app/

---

## Why I built this

As a receptionist, a significant part of the job involves replying to emails about memberships, cancellations, suspensions, swim school, pool hire, and general enquiries. These replies need to be accurate (referencing real T&Cs), consistent, and sent quickly during busy shifts.

I built this tool to solve that problem — reducing the time it takes to draft a reply from several minutes to a few seconds, while keeping responses accurate and on-brand.

---

## Features

- **Per-user staff profiles** — each team member signs in at the start of their shift with their own profile, preferences, and communication style
- **AI-generated reply options** — three tones generated per email: warm & friendly, professional, and brief & direct
- **Grounded in real T&Cs** — replies are based on actual YMCA North terms and conditions, facility hours, pricing, and the Summer 2026 group exercise timetable
- **Kia ora greeting** — culturally appropriate NZ greeting used in friendly replies
- **Labelled blanks** — if information isn't available in the knowledge base, the AI flags it clearly with `[ BLANK - add: ... ]` rather than making something up
- **Receptionist tip** — each generation includes a heads-up for the staff member about anything worth double-checking before sending
- **Topic quick-select** — tag the email type (Cancellation, Suspension, Class enquiry, Pool hire, etc.) to help the AI focus
- **Style learning** — the app tracks which reply style each staff member tends to pick, and adjusts future suggestions accordingly
- **Per-user settings** — light/dark theme toggle and accent colour preference, saved per profile
- **Edit before sending** — inline editing on any reply before copying
- **Reset / start over** — one click to clear and start fresh
- **Correct email routing** — reception vs swim school emails used appropriately based on query type

---

## Tech

- Vanilla HTML, CSS, JavaScript — single file, no build tools or dependencies
- [Anthropic Claude API](https://www.anthropic.com/) (`claude-sonnet-4-20250514`) for reply generation
- `localStorage` for persisting staff profiles and style preferences between sessions
- Hosted on [Netlify](https://netlify.com)

---

## How it works

1. Staff select their profile on the login screen at the start of their shift
2. They paste an incoming customer email into the text area
3. Optionally tag the topic using the quick-select bar
4. Click **Generate reply options**
5. Three replies are returned, grounded in the T&Cs knowledge base
6. Staff pick the best one, edit if needed, and copy to send
7. The pick is recorded to the staff member's profile to refine future suggestions

---

## Knowledge base

The AI prompt includes:
- Full YMCA North membership T&Cs (cancellation, suspension, payments, age requirements)
- Glen Innes facility info and operating hours
- Public holiday hours
- Adult Learn to Swim pricing and term dates
- Tri-Squad session times and pricing
- Pool hire rates
- Swim school / courses cancellation policy
- Summer 2026 group exercise timetable

---

## Roadmap / planned features

- [ ] Import anonymised email history to further refine reply style per staff member
- [ ] Full email signature block with contact details
- [ ] PIN-protected access for staff privacy
- [ ] Email inbox integration (Gmail/Outlook API) — Phase 2
- [ ] Smarter content-based learning from edited replies

---

## Version history

| Version | Notes |
|---------|-------|
| v1.0 | Initial release — profile screen, reply generation, style learning, topic tags, per-user settings |

---

*Built for The Y Glen Innes Pool & Leisure Centre, Auckland NZ.*
