# sunmatch

sunmatch tells you how strong the sun is where you are, in terms of a place and date you already know.

For example, 16:00 in Gran Canaria on 21 December matches London on 20 June at about 18:33, or 07:32 in the morning.

## How it works

- The sun's height above the horizon is computed with the NOAA solar position algorithm.
- The app finds the times of day when the sun reaches the same height at the comparison place and date.
- The UV figures are clear-sky estimates derived from sun height alone, assuming sea level and typical ozone. Cloud, haze and the real ozone column change the actual value.
- Optional altitude and surroundings adjustments (under "Altitude and surroundings") show a second, adjusted match below the main result. Altitude adds about 10% UV per 1,000 m (WHO) and is ignored below 500 m; with current location, the phone's GPS altitude is used unless a value is entered. Reflection from the surroundings multiplies exposure by about 1.10 near water, 1.15 on sand and 1.5 on fresh snow. Both are estimates; the main sun-height match is unchanged.

## Privacy

Everything runs in the browser. Your location is used only on your device to calculate sun height, and it is never sent anywhere. There is no server, no account and no tracking.

## Install on iPhone

1. Open the site in Safari.
2. Tap Share, then **Add to Home Screen**.

Once opened, the app works offline.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: interface, solar calculations and place data |
| `manifest.webmanifest` | Home-screen name, icon and display settings |
| `sw.js` | Service worker that caches the app for offline use |
| `icon-*.png` | App icons: dark version for the home screen and dark mode |
| `icon-light-*.png` | Light version of the icon, used as the browser tab icon in light mode |

## Data

Place data © [GeoNames](https://www.geonames.org/), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). It is filtered to places with a population of at least 15,000, plus national capitals and a few hand-added islands, regions and towns. About 130 major ski resorts are added by hand, each with an approximate typical skiing altitude (halfway between the lowest and highest lifts), which the altitude adjustment uses automatically. Time zones are derived from coordinates.
