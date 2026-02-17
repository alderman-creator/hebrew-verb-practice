# Hebrew Bible Verb Practice

This app now starts with a step-by-step setup wizard:
1. Choose stem
2. Choose aspect
3. Choose verb type (strong, 1 nun, etc.)
Each setup step supports multi-select (one or many choices).

After setup, it opens the parse quiz screen.
The app also saves your latest setup choices in browser local storage.

## Data source

The app reads from:
- `publish-site/hebrew_verbs_all_stems.json` (full BHSA-derived multi-stem dataset)
- `publish-site/hebrew_verbs_all_stems.js` (embedded auto-load source for direct `file://` opens)
- fallback: `publish-site/qal_strong_top100.json` / `publish-site/qal_strong_top100.js`

Direct `index.html` opens from Finder should now auto-load from `hebrew_verbs_all_stems.js`. If anything still blocks it in your browser, use the **Load JSON file** button and choose `hebrew_verbs_all_stems.json`.

Current full dataset exposes multiple stems (including Qal, Niphal, Piel, Pual, Hiphil, Hophal, Hitpael and additional BHSA stem labels), with aspects currently available as Perfect/Imperfect/Imperative in the filtered quiz set.

## Run locally

```bash
cd /Users/cityarts/Documents/New\ project/publish-site
python3 -m http.server 8000
```

Then open:
- `http://127.0.0.1:8000/`
