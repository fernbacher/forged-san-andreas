# Forged San Andreas

The complete website, ready for GitHub Pages or any static web host. The design, mod directory, credits, download links, checksum and mission notes are included.

## Publish on GitHub Pages

1. Create a **public** repository named `forged-san-andreas` on GitHub. Enable **Add a README file** so the repository starts with a `main` branch.
2. Extract this ZIP. Open the extracted `forged-san-andreas` folder.
3. In your repository, choose **Add file > Upload files**. Upload the contents of the extracted folder, including `assets` and `downloads`, and commit to `main`. `index.html` must be at the top level of the repository, not inside another folder. Upload the extracted files, not the ZIP.
4. Include the hidden `.nojekyll` file. On KDE, Alt+. shows hidden files. If it was missed, use **Add file > Create new file**, name it `.nojekyll`, leave it empty and commit it.
5. Open **Settings > Pages**. Under **Build and deployment**, choose **Deploy from a branch**, then **main** and **/(root)**. Click **Save**.
6. Wait for deployment to finish. The Pages settings screen will show the website URL. For the `fernbacher` account and this repository name, the expected address is `https://fernbacher.github.io/forged-san-andreas/`.

GitHub Pages is free for public repositories. No Node.js installation, build command, custom workflow, API key or backend is required. Future commits to `main` publish automatically.

GitHub instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Other static hosts

Use this extracted folder as the publish directory. Leave the build command empty when the host permits it. All website assets use relative paths, so the site also works in a subdirectory.

The game archive stays on VoidDrive. This ZIP contains the website and the small checksum file; the download buttons already point to the supplied links.

## Preview locally

From the extracted folder, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open http://127.0.0.1:8000 in your browser. Stop the server with Ctrl+C. Opening `index.html` directly displays the page, but browser restrictions can prevent the searchable catalogue from loading.

## Files and edits

- `index.html`: page content, downloads, mission notes and the complete no-JavaScript mod directory.
- `style.css`: layout, colours, responsive styling and Google Fonts import.
- `app.js`: search, filters, creator index and copy-hash button.
- `mods.json`: the searchable mod directory and source links. If you change entries, update the matching entries in `index.html` too so the no-JavaScript directory stays in sync.
- `assets/cj-artwork.webp`: the credited promotional artwork.
- `downloads/GTA-San-Andreas.7z.sha256`: the supplied archive checksum.
- `.nojekyll`: tells GitHub Pages to serve the files directly.

To change the archive, update its link and displayed SHA-256 in `index.html`, replace the checksum file and update the checksum mirror link. Keep the filename inside the checksum file identical to the downloadable archive filename.

## Credits

Mod creators and original release links are credited on the website. The original mod packages retain their own credits and terms. The promotional artwork is by Rockstar Games, sourced from GTA Base's San Andreas artwork archive. Typography uses UnifrakturCook, Barlow and Barlow Condensed through Google Fonts.

Forged San Andreas is Fernbacher's independent fan project.
