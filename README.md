# RetroTho

A minimal portfolio for apps, tools, and experiments.

Static HTML and CSS, with one small script for the theme toggle. No dependencies,
build step, external fonts, cookies, or analytics. The theme defaults to the
system appearance. The icon cycles through system, light, and dark; manual
choices are saved in browser localStorage. All project content works without
JavaScript.

## Preview

Open `public/index.html`, or serve the public directory locally:

```sh
python3 -m http.server 8080 --directory public
```

Then visit http://localhost:8080.

## Structure

- `public/index.html` — page content and project links.
- `public/styles.css` — layout, reusable project styles, and theme colors.
- `public/theme.js` — theme preference and accessible icon toggle.
- `public/favicon.svg` — site icon.

## Updating projects

Edit the project entries directly in `public/index.html`. The page includes
selected projects and a compact list of additional work. Copy an existing entry
and update its title, description, link, and unique heading ID when adding a
project. Selected-project subtitles list the implementation language first,
followed by relevant frameworks, storage, or compiler tools. Keep what the
project does in its description. Verify technologies against the project source
before adding them.

Project details are stored in the HTML so visitors do not make GitHub API requests.
There is no API key, background sync, or runtime data dependency.

Keep the stylesheet, theme script, and icon
in the same folder as `index.html`. Asset paths are relative, so the page also
works when opened directly from disk.
