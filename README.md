# Los Angeles Cartographic Archive
### Pre-1930 Street Maps & Ephemera — Private Collection

A personal repository website for a collection of pre-1930 Los Angeles street maps, atlases, ephemera, stocks, and related cartographic materials.

---

## Hosted Setup (GitHub + Netlify)

### 1. Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **New repository** (the green button)
3. Name it something like `la-map-archive`
4. Set it to **Public** (required for free Netlify hosting)
5. Click **Create repository**

### 2. Upload the files
1. In your new repo, click **Add file → Upload files**
2. Drag in `index.html`, `README.md`, and the `images/` folder
3. Click **Commit changes**

### 3. Connect to Netlify
1. Go to [netlify.com](https://netlify.com) and sign in with your GitHub account
2. Click **Add new site → Import an existing project**
3. Choose **GitHub** and select your `la-map-archive` repo
4. Leave all build settings blank (this is a plain HTML site)
5. Click **Deploy site**

Your site will be live at a URL like `https://la-map-archive.netlify.app` within seconds.

---

## Adding Images to the Collection

### Step 1 — Prepare your scan
- Recommended format: **JPEG**, medium-high quality
- Recommended size: **1200–2400px** on the long edge (balance of quality and load speed)
- Name the file something meaningful, e.g. `baist-1913-plate2.jpg`

### Step 2 — Add to the images/ folder
Upload your scan to the `images/` folder in your GitHub repository.

### Step 3 — Update the collection data
In `index.html`, find the item you want to add an image to and update the `imageUrl` field:

```javascript
// Before:
imageUrl: ""

// After:
imageUrl: "images/baist-1913-plate2.jpg"
```

### Step 4 — Commit and push
GitHub will save the change, and Netlify will automatically republish the site within 30 seconds.

---

## Adding New Items to the Collection

Each item in `index.html` follows this structure inside the `COLLECTION` array:

```javascript
{
  id: 44,                          // next sequential number
  title: "Title of the item",
  year: "1915",
  type: "Map",                     // Map, Atlas, Ephemera, Stock, Blueprint, Illustration, Photo Book
  publisher: "Publisher name",
  dimensions: '18" × 24"',
  accession: "LAC-1915-044",       // your accession number
  imageUrl: "",                    // or "images/your-file.jpg"
  rumseyUrl: "",                   // David Rumsey or other source URL if applicable
  photographed: false,             // true if you've photographed it
  recent: false,                   // true if it's a recent acquisition
  description: "Description of the item.",
  tags: ["Tag1", "Tag2"],
},
```

---

## David Rumsey Collection Links

For items that have a matching entry on [davidrumsey.com](https://www.davidrumsey.com), set the `rumseyUrl` field to the item's page URL. A **"View on David Rumsey Collection ↗"** button will appear in the lightbox.

Many items also exist on the [Internet Archive](https://archive.org/details/david-rumsey-map-collection) following Rumsey's 2022 donation.

---

## File Structure

```
la-map-archive/
├── index.html        ← the entire website (one file)
├── README.md         ← this file
└── images/           ← place your scans here
    ├── .gitkeep      ← keeps the empty folder tracked by git
    └── your-scan.jpg
```

---

*Los Angeles Cartographic Archive — Pre-1930 Collection*
