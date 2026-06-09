# Content editor (Sveltia CMS) — one-time setup

The site now has a browser-based editor at **https://fuzzsgrill.com/admin**.
Once writing a post is as easy as filling in a form and clicking **Publish** —
no terminal, no git, no `hugo` commands.

Everything is already wired up **except login**. The CMS needs permission to
commit to the GitHub repo on your behalf, and that takes one ~15-minute setup.
You only do this once.

## What you need
- Admin access to the `fuzzsgrill/fuzzsgrill.com` GitHub repo.
- Access to the site's Netlify dashboard.

## Step 1 — Create a GitHub OAuth App
1. Go to GitHub → **Settings → Developer settings → OAuth Apps → New OAuth App**
   (direct link: https://github.com/settings/developers).
2. Fill in:
   - **Application name:** `Fuzz's Grill CMS`
   - **Homepage URL:** `https://fuzzsgrill.com`
   - **Authorization callback URL:** `https://api.netlify.com/auth/done`
3. Click **Register application**.
4. Copy the **Client ID**, then click **Generate a new client secret** and copy
   the secret. (Keep the tab open — you'll paste both into Netlify next.)

## Step 2 — Tell Netlify about it
1. In the Netlify dashboard, open the **fuzzsgrill.com** site.
2. Go to **Site configuration → Access & security → OAuth**
   (older UI: **Site settings → Access control → OAuth**).
3. Under **Authentication providers**, click **Install provider** and choose
   **GitHub**.
4. Paste the **Client ID** and **Client Secret** from Step 1. Save.

## Step 3 — Log in and write a post
1. Go to **https://fuzzsgrill.com/admin**.
2. Click **Login with GitHub** and authorize.
3. Click **New Blog Post**, fill in Title / Date / Summary, write the body,
   turn the **Draft** toggle **off**, and hit **Publish**.
4. Netlify rebuilds automatically; the post is live in about a minute.

That's it. From now on, all writing happens at `/admin`.

---

### Notes
- The editor commits straight to the `main` branch. The old habit of making a
  new git branch per post is no longer needed.
- Images dragged into the editor are saved to `static/images` and inserted
  automatically.
- The login config lives in `static/admin/config.yml`; the editor page itself is
  `static/admin/index.html`. Hugo publishes both to `/admin` automatically.

### Alternative login (no Netlify OAuth)
If you ever move off Netlify, Sveltia can authenticate through a small free
Cloudflare Worker instead — see https://github.com/sveltia/sveltia-cms-auth.
You'd then add a `base_url` line to `config.yml` pointing at that worker.
