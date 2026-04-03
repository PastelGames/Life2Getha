# Lift

A lightweight workout tracker built as a static app for GitHub Pages.

## Launch Notes

- Main entry file: `index.html`
- Local editable source copy: `WorkoutTracker-2.html`
- Data is stored locally in the browser by default.
- Optional cloud sync uses the shared Supabase project configured inside the app.

## GitHub Pages

1. Push this folder to a GitHub repository.
2. In GitHub, open `Settings` -> `Pages`.
3. Set the source to deploy from the main branch root.
4. Wait for Pages to publish `index.html`.

## Security Notes

- The app uses the public Supabase anon key in the frontend. That is normal.
- Never add a Supabase service role key to this app.
- Keep row-level security enabled on the `lift_states` table so each user can only access their own data.
- User-created content is escaped before rendering to reduce injection risk from synced or imported data.

## Friend Setup

Friends can either:

- create an account in the `Sync` tab and use cloud save/load
- or skip accounts entirely and download their data as JSON or CSV
