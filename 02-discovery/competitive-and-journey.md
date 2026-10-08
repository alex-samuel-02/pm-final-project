# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** An experienced delivery driver who completes dozens of stops a day and knows the route better than the software does.
- **Goal, what is this user ultimately trying to achieve?:** To move through every stop as fast as possible with the fewest taps, so the day ends on time.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Standing at a doorstep in the rain with a package in one hand, they have to tap through three screens just to mark a stop delivered, and "Start Route", used about 30 times a day, is now buried under features they've never touched. They've given up and text the dispatcher instead, which means the app no longer records the work it exists to track (BUG-2055, BUG-2079).
- **External tools, the outside platforms or tools the user is forced to use:** The research shows three workarounds this persona relies on. One is directly evidenced for this driver, and two come from other experienced drivers in the same data.

1. Texting the dispatcher instead of marking stops delivered (primary hack). Diego says this directly (UXR-01), and the bug log confirms the three-tap flow "drives off-platform workarounds" (BUG-2055).

2. A paper manifest kept in the cab. Five of seven focus-group drivers carry one "just in case the app dies" (UXR-12), so it's a backup the veteran keeps alongside the app.

3. Overriding route optimization from memory. Sam overrides it every day because the app ignores closures and loading docks (UXR-05, BUG-2068). This is the "knows the route better than the software" part of your persona.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1) The driver hands over the package at the doorstep and gets back to the van or keeps walking.
2) They open their messaging app (SMS or the dispatch WhatsApp group), not RouteLogic.
3) They type a short note like "14 Elm St done" and send it, often batching several stops into one message later.
4) They move to the next stop, skipping the in-app proof-of-delivery photo and status change entirely.
5) he dispatcher reads the message, possibly among dozens from other drivers, and has to work out which stop it refers to.
6) The dispatcher either updates the system manually, later, or doesn't, leaving the stop showing "in progress" (the stale-board problem in UXR-09).
- **Core frustration, the exact moment the process feels most “broken”:** The process feels most broken in the few seconds after the package leaves the driver's hand. The delivery is physically finished, but the app says it isn't. The driver is on a doorstep in the rain, still holding another package, and the app wants three screens of attention for a job that's already done.

That's the moment the driver decides it isn't worth it, pockets the app and texts the dispatcher instead.
- **The evidence, a specific quote or behavior from the research that proves this:** Diego's interview (UXR-01) captures both the moment and the behaviour in his own words:

"To mark a stop delivered I tap through three screens. In the rain, at a doorstep, with a package in one hand. I've started just texting my dispatcher instead."

This is the strongest piece of evidence because it contains everything in one place: the friction (three screens), the conditions (rain, doorstep, one hand) and the resulting behaviour (texting the dispatcher). It's also a direct quote from a three-year driver, so it carries the credibility of experience rather than a newcomer's learning curve.
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** routelogic-future-state-journey.html
