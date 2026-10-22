# projectsaheli.org

Static site: `index.html` + `assets/`. No build step.

## Preview locally
    cd site && python3 -m http.server 8000   # open http://localhost:8000

## Deploy (GitHub Pages)
1. Create a GitHub repo and push the contents of this `site/` folder.
2. Repo Settings → Pages → Deploy from branch `main`, folder `/ (root)`.
3. Custom domain: `projectsaheli.org` (the `CNAME` file already sets this). Tick "Enforce HTTPS".
4. At your domain registrar, add DNS records:
   - A records for `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME for `www`: `<your-github-username>.github.io`

`assets/saheli.mp4` is a 1080p web version (~52 MB) of the original 4K video, under GitHub's 100 MB file limit.
Netlify or Vercel also work: drag-and-drop this folder, then add the domain in their dashboard.
