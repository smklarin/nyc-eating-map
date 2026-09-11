# NYC Eating Map — first iPhone-friendly prototype

A static mobile web app for the family restaurant list. It uses Leaflet + OpenStreetMap, browser GPS, and universal links into Apple Maps / Google Maps.

## What works
- iPhone-friendly responsive map
- “Use my location” / recenter button
- live blue location dot (when permission is granted)
- restaurant pins and popup details
- nearest-first restaurant list with straight-line distance
- search and food-category filters
- one-tap walking directions in Apple Maps or Google Maps
- Share button using the iPhone share sheet
- basic Add-to-Home-Screen/PWA support when hosted over HTTPS

## Important: location requires HTTPS
Safari geolocation generally requires a secure origin. For real iPhone testing, host this folder using HTTPS (GitHub Pages, Netlify, Cloudflare Pages, etc.). Opening the HTML directly as a local file is useful for visual testing but may not provide GPS access.

## Data notes
The restaurant names, notes, and original locations came from the family Word document. For this prototype:
- “184 And Avenue” was interpreted as **184 2nd Avenue**, matching Tompkins Square Bagels’ official site.
- Hamburger America was updated from the document’s “55 West Houston St” to **155 W Houston St**, which its official site currently lists. (Apple Maps may identify the same corner/storefront by MacDougal St.)
- Pins are seeded with coordinates so the app is immediately usable; the final pre-trip version should get one last coordinate/address audit.
- Family notes such as prices/Bib Gourmand labels are displayed as notes, not live claims.

## Quick deployment with GitHub Pages
1. Create a new public GitHub repository, e.g. `nyc-eating-map`.
2. Upload the contents of this folder to the repository root.
3. In the repository: **Settings → Pages**.
4. Under “Build and deployment,” choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
5. Save. GitHub will provide an HTTPS URL. Share that URL with the family.

## Test checklist on iPhone
1. Open the HTTPS link in Safari.
2. Tap **Use my location** and choose Allow.
3. Confirm a blue dot appears.
4. Tap a restaurant pin and then **Apple Maps**.
5. Test the category chips and search box.
6. Optional: Safari Share → **Add to Home Screen**.

## v2 features
- Interactive restaurant pins across Manhattan plus Lucali in Brooklyn
- iPhone/Safari geolocation with a live "you are here" marker
- Closest-first restaurant list after location is enabled
- **Near me** mode showing the nearest 8 restaurants that match the current search/filter
- Closest restaurant shortcut displayed directly on the map
- Search and cuisine filters
- Restaurant **Website / Menu** button
- One-tap walking directions in Apple Maps
- One-tap walking directions in Google Maps
- Share button using the iPhone share sheet
- Mobile-friendly controls and larger touch targets
- Add-to-Home-Screen tip for iPhone users

## Deploying on GitHub Pages
Replace the repository's existing `index.html` with the v2 `index.html` and commit the change to the `main` branch. GitHub Pages should redeploy automatically.

For this repository, the public site should remain:
`https://smklarin.github.io/nyc-eating-map/`

## Notes
The restaurant notes came from the family's source document and are not live hours or pricing. Restaurant website/menu links were researched separately. Apple Maps and Google Maps handle the actual navigation route.
