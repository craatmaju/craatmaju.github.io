# C-RAAT Website — Plain HTML Version

## Files
```
craat-html/
├── index.html          ← Homepage (C-RAAT + summer school announcement)
├── summer-school.html  ← Full NLP Summer School 2026 page
├── events.html         ← Events grid with poster slots
├── about.html          ← About C-RAAT
├── style.css           ← All shared styles
├── images/             ← Create this folder; put event posters here
└── README.md
```

## Deploy to GitHub Pages (5 minutes)

1. Create a new repository on GitHub, e.g. `craat-website`
2. Upload all files in this folder to the repo root
3. Go to **Settings → Pages → Source → Deploy from branch → main / (root)**
4. Your site will be live at `https://yourusername.github.io/craat-website/`

### Custom Domain (e.g. craat.ac.pk or craat.org)
1. Buy a domain from Namecheap, Cloudflare, or Porkbun
2. In the repo, create a file named `CNAME` with just your domain:
   ```
   craat.org
   ```
3. In your domain registrar's DNS, add:
   - `A` records pointing to GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record: `www` → `yourusername.github.io`

## Customising Content

### Add a Registration Form Link
In `summer-school.html`, find:
```html
<a href="#" class="btn btn-gold">Register via Online Form</a>
```
Replace `#` with your Google Form or Jotform URL.

### Add Event Posters
1. Create an `images/` folder and place your poster images there
2. In `events.html`, replace the placeholder divs:
```html
<!-- Replace this: -->
<div class="poster-icon">🖼</div>
<div class="poster-label">Poster — Event Name</div>

<!-- With this: -->
<img src="images/your-poster-filename.jpg" alt="Event Name Poster">
```

### Update Event Details
Edit the `.event-date` and `.event-title` elements in `events.html` for each card.

## Maintenance

- **No build step needed** — edit HTML/CSS directly
- **No dependencies** — fonts load from Google Fonts CDN
- Changes go live as soon as you push to GitHub
