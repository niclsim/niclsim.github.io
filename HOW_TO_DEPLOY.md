# How to publish your portfolio with GitHub Desktop

End result: your site lives at **https://niclsim.github.io** — free, on your existing GitHub account, deploys in ~5 minutes the first time and ~30 seconds for every update after.

---

## Step 1 — Preview locally first (10 seconds)

Before you publish, double-click `index.html` to open it in your browser. Make sure it looks right. If you want any copy or layout changes, tell Claude before deploying.

---

## Step 2 — Add the folder to GitHub Desktop

1. **Open GitHub Desktop.**
2. **File → Add Local Repository…**
3. Click **Choose…** and navigate to:
   `/Users/nicolesimmons/Documents/Claude/Projects/Portfolio/niclsim.github.io`
4. Click **Add Repository**.
5. GitHub Desktop will say: *"This directory does not appear to be a Git repository."* → click **create a repository** in that message.
6. In the dialog:
   - **Name:** `niclsim.github.io`  *(this exact name is critical — it's what gives you the clean URL)*
   - **Description:** *(optional)* "Personal portfolio site"
   - Leave Git Ignore and License blank (already handled).
   - Click **Create Repository**.

---

## Step 3 — First commit

GitHub Desktop will now show all your files as changes ready to commit.

1. In the bottom-left, type a commit message: `Initial portfolio site`
2. Click **Commit to main**.

That commits locally. Next, push it to GitHub.

---

## Step 4 — Publish to GitHub

1. At the top of GitHub Desktop, click **Publish repository**.
2. In the dialog:
   - Confirm name is `niclsim.github.io`.
   - **Uncheck "Keep this code private"** — GitHub Pages requires a public repo on free accounts.
   - Click **Publish Repository**.

GitHub Desktop pushes to GitHub. Your repo now exists at `https://github.com/niclsim/niclsim.github.io`.

---

## Step 5 — Enable GitHub Pages (one-time, takes 1 minute)

1. Open **https://github.com/niclsim/niclsim.github.io** in your browser.
2. Click **Settings** (top nav of the repo).
3. In the left sidebar, click **Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Under **Branch**, select `main` and folder `/ (root)`. Click **Save**.
6. Wait ~30 seconds, then refresh. GitHub will show a green box: *"Your site is live at https://niclsim.github.io"*.

That's it. Your portfolio is online.

---

## Updating the site later

1. Tell Claude what to change (or edit `index.html` yourself).
2. Open GitHub Desktop — you'll see the changed files.
3. Type a commit message ("update hero copy", "swap PD slide", etc.).
4. Click **Commit to main**, then **Push origin**.
5. Live site updates within ~30 seconds.

---

## Custom domain (optional, ~$12/year)

Want `nicolesimmons.com` instead of `niclsim.github.io`?

1. Buy the domain at [Cloudflare Registrar](https://www.cloudflare.com/products/registrar/) or [Porkbun](https://porkbun.com) (cheapest options, ~$10–$12/year for `.com`).
2. In your repo on github.com → **Settings → Pages → Custom domain** → enter your domain.
3. At your registrar, add the DNS records GitHub gives you (it'll tell you the exact records).
4. Wait ~15 minutes for DNS propagation. Done.

GitHub handles HTTPS automatically.

---

## Troubleshooting

**GitHub Pages shows 404 after enabling.** Wait 60 seconds and refresh. First deploy can take a moment.

**Images not showing.** Check that the `images/` folder pushed with the rest. In GitHub Desktop, the file list under "History" should include all the files in `images/`.

**Want to keep the repo private.** GitHub Pages on free accounts requires public. If you want it private, either upgrade to GitHub Pro ($4/mo) or use Netlify instead — Netlify allows private GitHub repos on the free tier.

**Need a non-`niclsim` URL.** Buy a custom domain (see above).
