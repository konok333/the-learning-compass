# The Learning Compass

Responsive Bengali-first educational website for The Learning Compass, with featured playlists, searchable video library, topic filters, pagination, social links and basic SEO metadata.

## Structure
- `index.html`: homepage, introduction, founder/leader links and featured playlists
- `assets/`: logo, favicon and Open Graph cover
- `videos/`: video library, search, topic filter, sort and pagination
- `data/`: profile, featured playlists and synchronized public videos
- `styles.css`, `script.js`: design, responsive navigation and UI
- `robots.txt`, `sitemap.xml`: replace placeholder username after publishing
- `.github/workflows/sync-youtube.yml`: scheduled/manual YouTube sync
- `scripts/sync-youtube.mjs`: API pagination and JSON generation

## Publish on GitHub Pages
1. Create a repository named `the-learning-compass`.
2. Upload the **contents** of this folder to the repository root.
3. Open **Settings → Pages**; choose **Deploy from a branch**, `main`, folder `/(root)`, then Save.
4. Replace `YOUR-GITHUB-USERNAME` in `robots.txt` and `sitemap.xml` with your real GitHub username.
5. Site URL should be `https://YOUR-GITHUB-USERNAME.github.io/the-learning-compass/`.

## Enable automatic YouTube video sync
1. In Google Cloud Console, create/select a project and enable **YouTube Data API v3**.
2. Create an API key and restrict it to YouTube Data API v3 where possible.
3. In the GitHub repository, open **Settings → Secrets and variables → Actions → New repository secret**.
4. Name it exactly `YOUTUBE_API_KEY`, then paste the API key as its value. Do not put the key in public HTML or JavaScript.
5. Open **Settings → Actions → General → Workflow permissions** and enable **Read and write permissions**.
6. Go to **Actions → Sync YouTube Videos → Run workflow**. After a successful run, the script updates `data/videos.json` and `data/playlists.json`; the website loads them.
7. The workflow is scheduled twice weekly. Only public uploads/playlists can be listed. Very large channels/playlists can use more API quota.

## Search engines
After publishing, submit the sitemap URL in Google Search Console and Bing Webmaster Tools, and link the site from your YouTube channel and social profiles. Indexing is not instant and no website can guarantee that ChatGPT will identify someone in every answer.

## Official links
- YouTube: https://www.youtube.com/@The-Learning-Compass-123
- Facebook: https://www.facebook.com/tahonik.kaumkonok
- Facebook 2: https://www.facebook.com/profile.php?id=100078224406518
- LinkedIn: https://www.linkedin.com/in/tahonik-kaum-konok-97b995378/
