# Gallery Guide

A dependency-free HTML, CSS, and JavaScript gallery visitor demo.

Open `dist/index.html` in a browser, or serve `dist` with a local HTTP server.

- Search the three-artwork collection by title or artist.
- Open artist, date, medium, historical context, and close-looking prompts.
- Take a photo on supported mobile browsers or choose an image file.
- Experimental photo matching compares a 16×16 RGB reference grid locally, then asks the visitor to confirm. It is not general-purpose AI recognition and performs poorly with crops, glare, perspective, and unknown artworks. Photos are not sent to a server.

Edit the `artworks` array in `dist/app.js` to expand the collection. A production recognition feature should use a backend service and a larger verified catalog; never put a secret API key in client JavaScript.

## Image sources

Public-domain works and reproductions:
- Van Gogh: https://commons.wikimedia.org/wiki/File:Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg
- Hokusai: https://www.metmuseum.org/art/collection/search/56353
- Vermeer: https://commons.wikimedia.org/wiki/File:Girl_with_a_Pearl_Earring.jpg

Museum sources for artwork information are linked directly from each artwork detail.
