# ParKey

Live parking-slot app for malls, hospitals and other commercial centers.

- Live grid of 50 slots per lot (A1–E10): green = Free, red = Occupied
- Driver taps a free slot; it turns red, and turns green again when they leave
- 5-minute hold: a selected slot is reserved for the driver; if they don’t confirm parking it is released. One slot per driver at a time.
- Driver marks "I’ve left the lot" to free the slot (manual for now)
- Live counter, e.g. "12/50 slots remaining"; full lots tell drivers to go elsewhere

## Status
Front-end prototype (`index.html`, no build step). Slot data is simulated in the page; a shared backend is the next step.
