# GiggleByte website

The home page for GiggleByte's free learning games, published with GitHub Pages at
**https://gigglebyte-hub.github.io/** from the repository `GiggleByte-Hub/GiggleByte-Hub.github.io`.

- `index.html` — the whole page (no build step)
- `assets/` — logo, game icons and screenshots
- `.nojekyll` — tells GitHub Pages to publish files as-is, including the `.well-known` folder
  that will hold `assetlinks.json` for the Google Play apps

To change the site, edit `index.html` and upload it again.

## Player counters

Each game card shows how many devices have played that game. The count is anonymous: the first
time a game is opened on a device, its `player-count.js` adds 1 to that game's tally on
[GoatCounter](https://www.goatcounter.com) (no cookies, no IDs). This page reads the tallies.

To switch the counters on:

1. Create a free GoatCounter account (for example with the site name `gigglebyte-hub`).
2. In GoatCounter's site settings, tick **Allow adding visitor counts on your website**.
3. Put that site name in `GOATCOUNTER_CODE` in:
   - this site's `index.html` (the script at the bottom)
   - `Chariots-of-Grace/js/player-count.js`
   - `Messengers-of-Light/js/player-count.js`
   - `Rootwords/player-count.js`
4. Upload the changed files. Counting starts from that day, and local testing is never counted.

While `GOATCOUNTER_CODE` is empty, the games send nothing and the counters stay hidden.

## Website visits

The last line of `index.html` loads GoatCounter's `count.js`, which counts visits to this page
(path `/`) in the same GoatCounter dashboard. It uses no cookies and ignores visits from
`localhost`. Delete that `<script>` line to stop counting website visits.
