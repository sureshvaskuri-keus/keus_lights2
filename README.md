# KEUS Lighting Catalogue

GitHub Pages-ready static catalogue with a clean folder structure.

## Repository structure

```text
keus_lights/
│
├── index.html
├── .nojekyll
├── README.md
│
├── data/
│   ├── downlights.csv
│   ├── tracklights.csv
│   ├── profiles.csv
│   └── outdoor-lights.csv
│
└── scripts/
    ├── optimize_csv_images.py
    └── optimize_images.bat
```

## Catalogue mapping

- Downlights → `./data/downlights.csv`
- Tracklights → `./data/tracklights.csv`
- Profiles → `./data/profiles.csv`
- Outdoor Lights → `./data/outdoor-lights.csv`

## Image optimization workflow

When you replace any CSV with fresh ImgBB image URLs:

1. Put the updated CSV in the `data` folder.
2. Keep the filename unchanged.
3. Open the `scripts` folder.
4. Run `optimize_images.bat`.

The script scans the CSV files in `../data` and converts raw ImgBB image URLs to optimized WebP delivery URLs.

## GitHub Pages

Upload this entire folder structure to the root of your GitHub repository.

Then:

1. Repository → Settings → Pages
2. Source → Deploy from a branch
3. Branch → `main`
4. Folder → `/ (root)`
5. Save

Your `index.html` will automatically read the CSV files from `/data`.


## Mobile catalogue experience

The mobile layout has been optimized to behave more like an e-commerce catalogue:

- sticky KEUS header
- horizontally scrollable category navigation
- prominent product selector and search
- compact filter chips
- horizontally scrollable finishes
- two-column product grid on phones
- square product imagery
- MRP shown directly on product cards when available
- compact specifications
- product detail view opens as a full-screen mobile sheet
- sticky pagination control
