# Popcorn Files website

The marketing website for Popcorn Files. It's a single file, `index.html`, with no build step.

## Preview locally
Open `index.html` in a browser.

## Put it live (free options)

**Option A: GitHub Pages**
1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**. Under "Build and deployment", choose **Deploy from a branch**, then select `main` and `/ (root)`.
3. Under **Custom domain**, enter your domain (e.g. `popcornfiles.com`) and save. This creates a `CNAME` file.
4. At your domain registrar, add DNS records:
   - For the root domain: four `A` records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - For `www`: a `CNAME` record pointing to `<your-github-username>.github.io`
5. When the certificate is ready, tick **Enforce HTTPS**.

**Option B: Netlify or Vercel**
Import the GitHub repo. No build command, publish directory is `/`. Add your domain in the project's domain settings and follow the DNS instructions shown.

Check the hosting provider's own docs for the current DNS values before changing anything.

## Editing
See `CLAUDE.md` for the design decisions and structure. Claude reads it automatically when this repo is connected.
