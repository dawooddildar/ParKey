# ParKey

Live parking-slot app for malls, hospitals and other commercial centers.

- Live grid of 50 slots per lot (A1–E10): green = Free, red = Occupied
- Driver taps a free slot; it turns red, and turns green again when they leave
- 5-minute hold: a selected slot is reserved for the driver; if they don’t confirm parking it is released. One slot per driver at a time.
- Driver marks "I’ve left the lot" to free the slot (manual for now)
- Live counter, e.g. "12/50 slots remaining"; full lots tell drivers to go elsewhere

## Files
- `index.html`: offline demo (no backend, simulated cars) that runs anywhere, e.g. GitHub Pages
- `prototype/parkey-live.html`: shared live version using the Claude artifact database; it only works when published as a Claude artifact. Features: 5-min "I’m here" hold, 30-min "Reserve ahead" hold, still-parked reminder after 30 min, automatic release after 60 min. Open with `#fast` to test with short timers.

## Next step
Replace the Claude artifact database with a real backend (Firebase or Supabase) with user login and server-side rules.

## Status
Front-end prototype (`index.html`, no build step). Slot data is simulated in the page; a shared backend is the next step.
