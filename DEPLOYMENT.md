# Deployment notes

## Render (Node web service)
- Build command: `npm install`
- Start command: `npm start`
- Add environment variable `MPESA_MODE=mock` for the first deployment.
- Set `PORT` is supplied by Render automatically; the app reads it.
- The SQLite database on an ephemeral filesystem may be lost on redeploy/restart. Attach a persistent disk and set `DB_PATH` to a path on that disk, or use PostgreSQL for reliable production records.
- For live Daraja callbacks, the deployed service must have a stable public HTTPS address.

Do not switch to production until Safaricom has approved and supplied the correct live credentials and Till configuration.
