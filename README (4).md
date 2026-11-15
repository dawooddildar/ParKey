# ParKey

Live parking-slot app for malls, hospitals and other commercial centers.

- Live grid of 50 slots per lot (A1–E10): green = Free, red = Occupied
- Driver taps a free slot; it turns red, and turns green again when they leave
- 5-minute hold: a selected slot is reserved for the driver; if they don’t confirm parking it is released. One slot per driver at a time.
- Driver marks "I’ve left the lot" to free the slot (manual for now)
- Live counter, e.g. "12/50 slots remaining"; full lots tell drivers to go elsewhere

## Files
- `index.html`: the app, backed by Supabase (shared live slots, email sign-in, realtime updates)
- `supabase/schema.sql`: database table, security rules and functions; run once in the Supabase SQL Editor
- `prototype/offline-demo.html`: earlier demo with no backend
- `prototype/parkey-live.html`: earlier shared prototype that only works as a Claude artifact

## Setup
1. Run `supabase/schema.sql` in the Supabase SQL Editor.
2. In Supabase: Authentication, Sign In / Providers, make sure **Email** sign-in is enabled (anonymous sign-ins are not used). For quick testing you can turn off "Confirm email"; otherwise set Authentication, URL Configuration, Site URL to the address where the app is served so confirmation links open it.
3. Serve the folder (for example `python3 -m http.server`) or use GitHub Pages, then open `index.html`.

Rules: a 5-minute "I’m here" hold, a 30-minute "Reserve ahead" hold, one active slot per driver, a still-parked reminder after 30 minutes, automatic release after 1 hour.
