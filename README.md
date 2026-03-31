# Ozmundo's Blog (Jekyll)

Personal blog for GitHub Pages, built with Jekyll and the Minima theme.

## Run locally

Use Ruby **3.1.x** (see `.ruby-version`). With [rbenv](https://github.com/rbenv/rbenv):

```bash
rbenv install 3.1.4
rbenv local 3.1.4
gem install bundler
bundle install
bundle exec jekyll serve
```

Open [http://127.0.0.1:4000](http://127.0.0.1:4000).

## Publish on GitHub Pages (user site)

Your live URL is **https://ozmundo-v.github.io** when the repository is set up as a **user** site.

1. On GitHub, create a **public** repository named **`ozmundo-v.github.io`** (must match your username exactly).

2. From this project folder, push the `main` branch (first time only):

   ```bash
   git init
   git add -A
   git commit -m "Initial blog"
   git branch -M main
   git remote add origin https://github.com/ozmundo-v/ozmundo-v.github.io.git
   git push -u origin main
   ```

3. In the repository on GitHub: **Settings → Pages → Build and deployment → Source**, choose **GitHub Actions** (not “Deploy from a branch”). The workflow `.github/workflows/github-pages.yml` will build and deploy the site on every push to `main`.

4. After the first workflow run finishes, open **https://ozmundo-v.github.io**.

If Pages was previously set to “Deploy from branch”, switch it to **GitHub Actions** so the Bundler-based build matches your `Gemfile`.
