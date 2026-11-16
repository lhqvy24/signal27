# SIGNAL/27 Launch Campaign

A concept launch campaign for **SIGNAL/27**, a fictional applied-AI day in Ho Chi Minh City (Sat 16 Jan 2027). The project covers the full path from social post to landing page to shareable attendee badge, built with AI tools end to end.

> Concept project by Vivian Le. SIGNAL/27 is not a real event.

**Live microsite:** https://lhqvy24.github.io/signal27/

**Design kit (Figma):** https://www.figma.com/design/CslTv4CYDE9qnLs9RuZFyM/Signal-27?node-id=6-128&t=XgoD6idUoOpj0Ht4-1

## The problem

Event pages usually list every session and leave visitors to work out what is relevant to them. With three rooms running at once, a visitor can only attend a third of the programme, so the question they need answered is "which sessions are for me?"

## Campaign idea

Tagline: **Less noise. More shipped AI.** A single yellow signal line runs through every asset: scattered noise that resolves into one clear pulse.

The campaign works as a loop:

1. **Social kit** announces the event and counts down to it.
2. Every asset links to the **microsite**.
3. The microsite turns the agenda into a personal schedule.
4. Visitors create an **"I'm going" badge** and post it, which brings new people back to step 1.

## Deliverables

### 1. Interactive microsite (this repository)

| Feature | What it does |
| --- | --- |
| Countdown | Live timer to doors opening |
| Plan my day | Visitor picks a role and topics; the site recommends one session per time slot |
| Full agenda | 14 sessions across Build, Ship and Grow tracks, filterable by track |
| Make my badge | Generates a 1080×1080 share card and caption from the visitor's name and role |

How it works:

- One self-contained `index.html` (HTML, CSS, vanilla JavaScript). No backend, no build step.
- Recommendations use a simple tag score: 2 points for each tag matching a chosen topic, 1 point for each tag matching the chosen role. The top-scoring session in each time slot is selected.
- The badge is drawn in the browser with the Canvas API.
- Choices are saved in the visitor's own browser only. No data is collected or sent.

### 2. Social launch kit (Figma)

- **Announcement kit:** Instagram post (1080×1350), LinkedIn banner (1584×396), speaker card (1080×1080)
- **Countdown series:** three Instagram stories (1080×1920) for 30 days, 7 days and the day before, each with a 6-second motion loop

## Visual system

| Token | Value |
| --- | --- |
| Cobalt background | `#1B2FD1` |
| Off-white text | `#F4F1E8` |
| Signal yellow accent | `#FFD23F` |
| Display font | Big Shoulders Display |
| Label font | JetBrains Mono |

## Tools and process

- **Claude** for AI-assisted coding of the microsite
- **Figma AI and Figma Motion** for the social kit and animated stories
- **GitHub Pages** for deployment

Process: define audience and funnel, write the brief and prompts, generate a first version, review it against the brief, refine through follow-up prompts and manual edits, then deploy.

## Next steps

- Add a registration flow so the badge is issued after sign-up
- Add Vietnamese language support
- Track which topics visitors choose, to inform programme planning

## Author

**Vivian Le** | [GitHub](https://github.com/lhqvy24)
