---
name: setup-sandbox
description: Create org and artist folder structure using the Recoup CLI
---

# Setup Sandbox

Create the folder structure for the connected account's organizations and artists.

## Steps

1. Run `recoup orgs list --json` to get all organizations
2. For each organization, run `recoup artists list --org <organization_id> --json` to get its artists
3. Create the folder structure using mkdir:
   - `mkdir -p orgs/<organization_name>/artists/<artist_name>` for each org/artist pair
4. Commit and push:
   - `git add -A && git commit -m "setup: create org and artist folders" && git push origin main`
