# Putting Your Blog Online (DEPLOY.md)

This is the only part you have to do yourself, because it needs your accounts.
It takes about 30 minutes. You do it once, then never again.

## What you need

- A free GitHub account (this stores your blog's files)
- A free Netlify account (this puts your blog on the internet)
- Your domain (probably shedarestogo.com, or a subdomain like blog.shedarestogo.com)

## Step 1. Create a GitHub account

1. Go to github.com and sign up (free).
2. Create a new repository: click the + in the top right, then "New repository".
3. Name it `shedarestogo-blog`, leave it Public, and check "Add a README file".
4. Click "Create repository".
5. On the new page, click "uploading an existing file".
6. Drag in EVERYTHING from the `shedarestogo-blog` folder on your computer, then click "Commit changes".

Make sure the default branch is called `main`. (GitHub does this automatically for new repos.)

## Step 2. Create a Netlify account

1. Go to netlify.com and sign up using your GitHub account (click "Sign up with GitHub"). This links the two accounts.

## Step 3. Put the blog on Netlify

1. In Netlify, click "Add new site", then "Import an existing project".
2. Choose GitHub, then pick the `shedarestogo-blog` repository.
3. Netlify fills in the build settings by itself (it reads the netlify.toml file). Just click "Deploy site".
4. Wait about a minute. You will get a live link like `happy-name-123.netlify.app`. Your blog is online.

## Step 4. Connect your domain

1. In Netlify, go to Site settings, then Domain management, then "Add custom domain".
2. Type your domain (for example `blog.shedarestogo.com`) and follow the prompts.
3. Netlify will tell you to add one DNS record at wherever you bought your domain (GoDaddy, Namecheap, etc). It is one copy-paste line. Your domain company has a help page called "manage DNS" if you get stuck.
4. Netlify gives you free HTTPS automatically. Nothing to do.

One more thing: open the file `src/_data/site.json` in your GitHub repo, change the `url` line to your real domain, and commit. Netlify rebuilds automatically.

Also in that same file there is a line called `amazon_store` that currently says `PASTE_YOUR_AMAZON_STOREFRONT_URL_HERE`. Paste your real Amazon storefront link there and the "Shop my Amazon storefront" button will appear on your home page and gear page. Until you do, the button stays hidden.

## Step 5. Turn on the writing editor

This gives you the simple /admin page where you write posts like an email, no code.

1. In Netlify, go to the Integrations tab for your site and enable **Identity**.
2. Go to Identity settings, set Registration to **Invite only**.
3. Scroll to Services and enable **Git Gateway**.
4. Go to the Identity tab, click "Invite users", and invite yourself.
5. Check your email, accept the invite, and set a password.
6. Go to `yourdomain.com/admin`, log in, and write your first post. It publishes when you hit publish.

## After this

- To write: go to yourdomain.com/admin. That is it.
- To change design or text on the home page: those live in the `src` folder on GitHub. Ask Emz.
- Netlify rebuilds the site automatically every time you publish a post. You do nothing.
