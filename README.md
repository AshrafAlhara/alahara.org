# Alhara.org Website

A simple, clean landing page for Alhara, hosted on GitHub Pages.

## Local Development

To view the site locally, simply open `index.html` in your web browser.

Alternatively, you can use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (npx)
npx serve
```

Then visit `http://localhost:8000` in your browser.

## Deployment

This site is configured for GitHub Pages deployment with a custom domain.

### GitHub Pages Setup

1. Push your changes to the `main` branch
2. Go to repository **Settings** > **Pages**
3. Under "Source", select the `main` branch and root folder (`/`)
4. Click **Save**

### Custom Domain Configuration

The `CNAME` file is already configured for `alhara.org`.

#### DNS Records

Add these records at your domain registrar:

**A Records (for apex domain):**
| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**CNAME Record (for www subdomain - optional):**
| Type | Name | Value |
|------|------|-------|
| CNAME | www | AshrafAlhara.github.io |

#### Enable HTTPS

After DNS propagation (up to 24-48 hours), go to repository **Settings** > **Pages** and check "Enforce HTTPS".

## Structure

```
Website/
├── index.html          # Main landing page
├── css/
│   └── styles.css      # Stylesheet
├── CNAME               # Custom domain config
└── README.md           # This file
```

## Customization

Edit `index.html` to update:
- Organization name and tagline
- About section content
- Services/features
- Contact information

Edit `css/styles.css` to customize:
- Colors (via CSS custom properties in `:root`)
- Typography
- Spacing and layout
