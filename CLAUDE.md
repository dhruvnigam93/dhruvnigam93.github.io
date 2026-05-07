# dhruvnigam93.github.io

Personal portfolio and blog for Dhruv Nigam. Jekyll site hosted on GitHub Pages.

## Project layout

```
.
├── index.html                  # Homepage — bio, profile photo
├── writing/index.html          # Blog posts + publications list
├── talks/index.html            # Conference/meetup talks with links
├── blog/index.html             # Redirects to /writing
├── About/index.html            # Minimal about page
├── _layouts/
│   ├── default.html            # Base layout: nav, footer, Google Analytics
│   ├── posts.html              # Blog post layout (extends default)
│   └── analytics.html          # GA snippet
├── _posts/                     # Markdown blog posts (Jekyll-managed)
├── css/main.css                # All styles — vanilla CSS, responsive at 600px
├── assets/
│   ├── images/profile.jpg
│   ├── lumos-slides.pdf
│   ├── lumos-swiggy-slides.pdf
│   └── resume.pdf
└── _config.yml                 # Jekyll config: kramdown, GA ID, permalinks
```

### Key pages

- **index.html**: Profile section with photo + bio. External link to LUMOS arXiv paper.
- **writing/index.html**: Mix of external links (Substack, Medium) and Jekyll `_posts`. Publications section at bottom with linked paper titles.
- **talks/index.html**: Talk entries with links to slides, videos, and papers.
- **_layouts/default.html**: Shared nav (home, writing, talks) and footer (email, linkedin, github, twitter, resume).

### External link domains

Blog posts live on two Substacks and Medium — not on this site:
- **ML Trenches**: `mltrenches.substack.com` — opinion/analysis posts
- **ML Field Notes**: `mlfieldnotes.substack.com` — technical/tutorial posts
- **Medium**: `medium.com/dreamlockerroom` — Dream11 tech blog

Papers link to arXiv or Google Drive. Do NOT use `dhruvnigam93.substack.com` — that domain is dead.

## Deployment

- **Host**: GitHub Pages, automatic Jekyll build on push to `master`.
- **Repo**: `dhruvnigam93/dhruvnigam93.github.io` (remote: `github.com-personal`)
- **No Gemfile, no package.json, no CI workflows** — relies entirely on GitHub Pages' built-in Jekyll.
- **Deploy lag**: ~2-5 minutes after push before changes are live.
- **Local build**: not configured. No Gemfile means `bundle exec jekyll serve` won't work out of the box. Edits are verified on the live site after push.

## Testing methodology

After pushing changes, wait for GitHub Pages to deploy, then verify with Playwright:

1. **Navigate to each page** (`/`, `/writing`, `/talks`) on `https://dhruvnigam93.github.io/`.
2. **Click every external link** and confirm the destination page loads correctly (correct title, no 404).
3. **Check for CORS false positives**: `fetch()` from the page will fail due to CORS on most external sites — this does NOT mean the link is broken. Always test by navigating directly to the URL.
4. **Sites with auth walls** (LinkedIn, Medium when logged out) will show login pages — that's expected, not broken.
5. **ACM Digital Library** shows Cloudflare challenge — also expected.

### Link inventory to test

**Homepage**: "foundation model" → `arxiv.org/abs/2512.08957`

**Writing page**:
- Substack posts → `mltrenches.substack.com/p/...` or `mlfieldnotes.substack.com/p/...`
- Medium LUMOS → `medium.com/dreamlockerroom/...`
- Protium article → `protium.co.in/...`
- Publication titles → arXiv or Google Drive

**Talks page**:
- YouTube videos (3 links)
- GitHub PDF slides
- LinkedIn post
- Google Slides
- arXiv papers

**Footer** (all pages): email, linkedin, github, twitter, resume PDF

## Style and conventions

- Vanilla CSS in `css/main.css`. Responsive breakpoint at 600px.
- No JavaScript except Google Analytics.
- Blog posts use `layout: posts` front matter with `title` and `date`.
- Writing page mixes hardcoded external links with Jekyll `{% for post in site.posts %}` loops filtered by year.
- Publication titles are `<a class="pub-title">` links (not `<span>` — titles link directly to the paper).
