# papirglider

PapirGlider Klubben, the paper-plane guide site by Laden AS. A small static site in Norwegian: a landing page with the club logo, and a guide page with folding models, darts, trim and throwing tips, a trim table and embedded YouTube videos.

Live site: [https://laden.no/levi/](https://laden.no/levi/)

Docker copy: [https://laden.no/docker/levi/](https://laden.no/docker/levi/) (stack in [kim-laden/papirglider-docker](https://github.com/kim-laden/papirglider-docker))

## What is here

The site exactly as it is served live at `/levi/` on the Laden VPS.

- `index.html`: intro and landing page with the club logo.
- `guider.html`: guides, trim table and embedded videos.
- `css/stil.css`: the design.
- `img/`: logo and photos.
- `README.txt`: the original Norwegian notes that ship with the site.

No build step, no framework, no backend.

## Run it

Any static file server works. With Python:

```bash
python3 -m http.server 8080
```

Open [http://127.0.0.1:8080/](http://127.0.0.1:8080/). You can also open `index.html` straight in the browser.

The pages also load three site-wide files from the host by root-absolute path: `/assets/theme.js`, `/css/soundcloud-player.css` and `/js/soundcloud-player.js`. On laden.no they come from the main site and Lab'z ([kim-laden/laden.no](https://github.com/kim-laden/laden.no)). Served locally they return 404 and the site still works, just without the theme switch and the SoundCloud player.

## Copyright and licence

Copyright Laden AS (Org.nr. 937 285 833). The code is open source under the MIT License. See [LICENSE](LICENSE). The Laden name, mark and brand are trademarks of Laden AS and are not given away by that licence.

The embedded YouTube videos belong to their creators and are only linked, not included.

## Not in this repo

No secrets. This site needs none: no `.env`, no keys, no database. Editor and deploy backups (`*.bak*`) from the server are left out.
