# Nobody Online — Build 0.1

A functional first-stage prototype for a research-creation thesis about perceived social presence in simulated multiplayer environments.

## Start locally

Because NPC data is loaded with `fetch`, open the project through a local web server (not by double-clicking `index.html`).

```bash
cd nobody-online-build01
python -m http.server 8000
```

Visit http://localhost:8000 . You can also deploy the project root to GitHub Pages.

## Implemented

- Responsive dark fantasy strategy-game UI, with world map and 9 clickable settlements including the player
- Resource economy, 3 building upgrades, action points and power progression
- 30 simulated NPC profiles, ranking list, three joinable alliances
- Periodic seeded NPC chat and power events (every 9 seconds)
- Player chat entry (display only, no NPC reply engine)
- Local session persistence, reset and JSON event-log export

## Not yet implemented

- Meaningful NPC responses to player messages, competitive resource nodes, alliance invitations, NPC state machines, timed research conditions, questionnaires, reveal/debrief flow, backend research data collection
- Visual AIGC assets (currently CSS and text symbols are placeholders)

## Research / ethics

This is an internal demonstration and development prototype. The UI explicitly identifies its population as simulated. It is **not** approved for undisclosed-deception participant research. Obtain the required institutional research-ethics clearance or determination before any such formal study. Do not present synthetic activity logs as real participant data.

## Test steps

1. Open World, click a simulated castle and inspect the profile.
2. Gather wood once. Verify the action count falls and wood increases.
3. Open Territory and upgrade the castle; verify resource deduction and power increase.
4. Open Rankings and check the player's new power.
5. Join an alliance; verify one-time reward and no repeat reward on switching.
6. Wait 9 seconds; verify chat or power activity and event log.
7. Export the log, then reset the session.

## Known limitations

- NPC schedule uses a 9-second timer and will pause or throttle when the browser tab is backgrounded.
- The random generator is seeded for NPC event selection but wall-clock timing and session IDs vary.
- Action points do not regenerate in this version.
- Browser storage can be cleared by private browsing or site-data deletion.
