# Weather-App-JS

Simple client-side weather app that uses the OpenWeatherMap API to show temperature, humidity and wind for a city.

## Prerequisites
- Modern browser
- OpenWeatherMap API key (free tier available)

## Get an OpenWeatherMap API key
1. Sign up at https://home.openweathermap.org/users/sign_up.
2. Sign in and open Dashboard → API keys.
3. Create or copy the default key (may take a few minutes to activate).

## Provide the key to this project (do NOT commit keys)
Option 1 — Quick (local testing)
- Open `index.html`, find:
  const apiKey = "Enter-Your-Key-Here";
  and replace the placeholder with your key locally. Do not commit this change.

Option 2 — Safer (recommended)
- Create a local file `key.js` (ignored by git) with your key and expose it on `window`.
- Add `key.js` to `.gitignore`:
  echo "key.js" >> .gitignore
- Include `key.js` in `index.html` before the inline script:
  <script src="key.js"></script>

Example `key.js` is provided below.

## Usage
1. Open `index.html` in a browser (or serve via local static server).
2. Type a city name and click search.

## Security
- Never commit API keys or other secrets.
- If a key is accidentally committed, remove it from the index and rotate the key:
  git rm --cached path/to/file
  git commit -m "Remove secret"
  Then generate a new API key on OpenWeatherMap.