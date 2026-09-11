NYC Eating Map — first iPhone-friendly prototype

A static mobile web app for the family restaurant list. It uses Leaflet + OpenStreetMap, browser GPS, and universal links into Apple Maps / Google Maps.

What works

iPhone-friendly responsive map

“Use my location” / recenter button

live blue location dot (when permission is granted)

restaurant pins and popup details

nearest-first restaurant list with straight-line distance

search and food-category filters

one-tap walking directions in Apple Maps or Google Maps

Share button using the iPhone share sheet

basic Add-to-Home-Screen/PWA support when hosted over HTTPS

Important: location requires HTTPS

Safari geolocation generally requires a secure origin. For real iPhone testing, host this folder using HTTPS (GitHub Pages, Netlify, Cloudflare Pages, etc.). Opening the HTML directly as a local file is useful for visual testing but may not provide GPS access.

Data notes

The restaurant names, notes, and original locations came from the family Word document. For this prototype:

“184 And Avenue” was interpreted as 184 2nd Avenue, matching Tompkins Square Bagels’ official site.

Hamburger America was updated from the document’s “55 West Houston St” to 155 W Houston St, which its official site currently lists. (Apple Maps may identify the same corner/storefront by MacDougal St.)

Pins are seeded with coordinates so the app is immediately usable; the final pre-trip version should get one last coordinate/address audit.

Family notes such as prices/Bib Gourmand labels are displayed as notes, not live claims.

Quick deployment with GitHub Pages

Create a new public GitHub repository, e.g. nyc-eating-map.

Upload the contents of this folder to the repository root.

In the repository: Settings → Pages.

Under “Build and deployment,” choose Deploy from a branch, branch main, folder / (root).

Save. GitHub will provide an HTTPS URL. Share that URL with the family.

Test checklist on iPhone

Open the HTTPS link in Safari.

Tap Use my location and choose Allow.

Confirm a blue dot appears.

Tap a restaurant pin and then Apple Maps.

Test the category chips and search box.

Optional: Safari Share → Add to Home Screen.
