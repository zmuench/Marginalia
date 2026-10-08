# Marginalia

*daily notes from life's margins*: a tiny blog that runs free on GitHub Pages.
Newest post on top, alternating gray / white, with tags you can filter by.

Your posts live in `posts.json` and your About page in `about.md`, both in this repo.
Readers just see the page; the posting tools only appear on devices you've set up.

---

## 1. Put it on GitHub (once, ~10 minutes)

1. Sign in at **github.com** → **+** (top right) → **New repository**.
   Name it `marginalia`, set it to **Public**, and click **Create repository**.
2. On the new repo's page, click **uploading an existing file**. Drag in everything from this
   folder (`index.html`, `config.js`, `posts.json`, `about.md`, `README.md`, and `.nojekyll`*).
   Click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**,
   **Branch: main**, folder **/ (root)**, then **Save**.
4. After a minute or two your site is live at **`https://YOUR-USERNAME.github.io/marginalia/`**.

\* `.nojekyll` is a hidden file, so your computer may not show it. It's optional; skip it if you can't see it.

## 2. Make a posting key (once)

This is a *fine-grained personal access token*: a password that can only edit this one repo.

1. github.com → your profile picture → **Settings → Developer settings →
   Personal access tokens → Fine-grained tokens → Generate new token**.
2. **Name:** `Marginalia`. **Expiration:** pick what you like (up to a year; you'll make a new one when it expires).
3. **Repository access:** *Only select repositories* → `marginalia`.
4. **Permissions → Repository permissions → Contents:** *Read and write*. Leave everything else alone.
5. **Generate token** and copy it (starts with `github_pat_`). GitHub only shows it once.

## 3. Set up each device you'll post from

On your phone or laptop, open **`https://YOUR-USERNAME.github.io/marginalia/#write`**,
paste the token, and tap **Save**. That device now shows the compose box, Delete links, and
an **Edit** link on the About page. Nobody else sees them.

Tip: on iPhone, tap **Share → Add to Home Screen** for one-tap posting.

---

## Daily use

- Type a note, tap tags (or add new ones, comma-separated), hit **Post** (⌘/Ctrl + Enter on a keyboard).
- `**bold**`, `*italic*`, and links work. Line breaks are kept.
- Each post is saved to GitHub as a commit. You see it right away; readers see it after
  GitHub republishes the site, usually within a minute or two.
- **About page:** open About → **Edit** → **Save**.
- **Sign out** (top right) removes the token from that device.

## Good to know

- **Security:** the token sits in that browser's storage, so only set up devices you trust.
  If one is lost, delete the token on GitHub (Settings → Developer settings → Fine-grained
  tokens) and make a new one.
- **Readers can't post.** Even someone who finds `#write` can't save anything without your token.
- **The repo is public**, so anyone can see `posts.json` and its history, the same as reading the blog.
- **Change the look:** colors are at the top of `index.html` under `:root` (`--gray`, `--white`, `--accent`).
  Title, tagline, and the tag buttons are in `config.js`.
- **Tab icon (optional):** add a small square `icon.png` to the repo.
- **Custom domain:** fine. Add it under Settings → Pages, then fill in `owner` and `repo` in `config.js`.
- **Backup:** it's already one. Every post is in the repo's history.
