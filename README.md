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

## Reflection

My original idea was to design an instructional app for art galleries. For people who are not very familiar with art, gallery visits can be confusing. What’s more, it is inconvenient to repeatedly look up background information about artworks. That’s why I designed this app: users only need to simply take and upload a photo or enter the artwork’s title to retrieve relevant information about the piece. The target users of this design are beginners or casual enthusiasts with limited knowledge of fine art and art history. The simple interaction built into this software generates a detailed introduction page after a photo is submitted or a title is typed in.

After giving prompts to Codex, the resulting website largely matched my vision. Codex’s design even included features beyond my expectations — for instance, it linked to external websites to display more in-depth information about the artworks. However, these external links could not actually open during testing. I asked Codex to explain this issue and learned it stemmed from permission restrictions, so I did not request further refinements. This made me curious about how permissions for external data are defined and implemented in the real-world development of websites or mobile apps.

Codex’s design also had some flaws. The core interactions I envisioned — artwork search and photo upload — were not prominent enough, and some text was cut off. I therefore asked it to make adjustments. I found, though, that the first round of revisions only touched isolated parts of the interface, leaving the whole design visually disjointed. I then requested more holistic tweaks to create better visual consistency.

In my opinion, AI is extremely useful for hands-on practice. It can refine an initial concept and turn it into a functional prototype with decent aesthetics. Still, AI struggles to fully account for usability from the end user’s perspective, which is an area we human designers need to improve.

Currently, my app can only identify a small number of paintings. This limitation arises because it cannot connect to external networks, and I have a limited Codex usage quota, which prevents me from building richer content.
