# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** The manager who bought the platform for its admin and reporting, and who has to justify renewing it.
- **Goal, what is this user ultimately trying to achieve?:** Have one reliable record of delivery operations that their team actually uses, so the reports reflect what really happened.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Their drivers won't adopt the app, so the reporting they paid for rests on data nobody is entering. Real coordination happens on WhatsApp, texts and paper, and completed stops still show "in progress." One regional manager has flagged the renewal as at risk because of poor driver adoption. An enterprise ops manager is evaluating a simpler competitor that only does routing (UXR-04, UXR-10). New drivers can't be onboarded the same day because the menus are too nested (UXR-08). For this person, the product costs money and effort without delivering what they bought it for.
- **External tools, the outside platforms or tools the user is forced to use:** THE TOOLS THEY RELY ON INSTEAD

- Dispatch WhatsApp group: replaces live dispatch and reassignments in the app (UXR-02)
- Drivers texting dispatchers: replaces driver status updates in the app (UXR-01, UXR-02)
- Paper manifests (5 of 7 drivers): replaces the in-app stop list (UXR-12)
- Morning route screenshots: replaces offline route caching (UXR-06)
- Hands-on, multi-day onboarding: replaces self-serve onboarding in the app (UXR-08, BUG-2090)
- A routing-only competitor: replaces the platform itself (UXR-10)
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1. Stop trusting the dashboard.
Completed stops show as "in progress" for 20-60 minutes, so the manager can't treat the dashboard as live. [Documented: BUG-2072, UXR-09]

2. Get the real picture from dispatch's side channels.
To know what's actually happening, they have to rely on the WhatsApp group and driver texts, because that's where coordination now lives. [Channels documented; the manager relying on them is inferred]

3. Patch the records by hand before reporting.
They check app data against messages and paper manifests, then fix or explain the gaps before reports go up the chain. [Inferred: follows if reports are needed and the app data is wrong]

4. Onboard new drivers in person, over more than a day.
The nested menus make same-day onboarding impossible, and the tutorial can't be reopened, so experienced staff have to shadow and re-teach. [Constraint documented: UXR-08, BUG-2090; shadowing inferred]

5. Escalate or look for a way out.
They flag the renewal as at risk (regional manager) or trial a simpler routing-only competitor (enterprise ops manager). [Documented: UXR-04, UXR-10]
- **Core frustration, the exact moment the process feels most “broken”:** - They pay twice: the company pays for a platform and also pays in staff time to run WhatsApp, texts and paper beside it. The platform becomes an extra system to feed rather than the one place the work is recorded.
- The same work gets recorded three times: one delivery can exist as a tap in the app, a text to dispatch and a tick on paper, and these may disagree. Someone has to decide which is true.
- The data can't be audited: information in WhatsApp threads and on personal phones has no structure and no history, and it isn't owned by the company. Nothing lands where reporting can use it.
- The reporting advantage disappears: the Executive Summary says the workarounds cancel out "the reporting value that justified the purchase." Reports built on incomplete data are either wrong or need manual correction.
- Onboarding doesn't scale: every new driver takes experienced staff time, which is the kind of admin cost the product should remove.
- The problem feeds itself: less data in the app makes the dashboard less trustworthy. That pushes more coordination to WhatsApp, which leaves even less data in the app.
- **The evidence, a specific quote or behavior from the research that proves this:** 1. Drivers bypass the app because core actions take too long (BUG-2055, BUG-2079). That is the burden the Problem Hook describes.
2. The manager's data breaks down. Stale statuses and missing entries make reports unreliable.
3. The manager can't prove return on investment. The one thing they bought, reporting, no longer works, and that shows up at renewal. This is the regional manager's at-risk renewal (UXR-04).
4. The workaround proves they don't need the full platform. If the team already coordinates on WhatsApp and paper and only needs routes, a routing-only tool looks like a good fit. This is the enterprise account's competitor evaluation (UXR-10).

Key point: The competitor doesn't need better reporting than ours. It only needs to be simple enough that drivers use it, because our reporting is already producing nothing useful.
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** ops-manager-future-state.html
