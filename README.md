# Weather-App-JS

A simple, client-side weather app built with **HTML, CSS, and JavaScript**.

It lets you search for any city and displays current weather data from the **OpenWeatherMap API**, including:
- Temperature
- Humidity
- Wind speed
- Weather condition/description

---

## How it works

1. Enter a city name.
2. The app sends a request to OpenWeatherMap.
3. The API response is rendered in the UI.

Because this project runs entirely in the browser, it is easy to test locally.

---

## Get an API key from OpenWeatherMap

To use this app, you need a free API key.

1. Go to: https://openweathermap.org/ and create an account.
2. After signing in, open your account dashboard: https://home.openweathermap.org/api_keys
3. Create a new key (or use the default key).
4. Wait a few minutes for key activation if requests fail at first.

---

## Configure your API key

### Option 1: Quick local test

Open `index.html` and replace:

```js
const apiKey = "Enter-Your-Key-Here";
```

with your real key.

> Do not commit this key to GitHub.

### Option 2: Recommended (keep key out of tracked files)

1. Create `key.js` in the project root:

```js
window.OPENWEATHER_API_KEY = "your_api_key_here";
```

2. Add `key.js` to `.gitignore`:

```bash
echo "key.js" >> .gitignore
```

3. Load `key.js` before your app script in `index.html`:

```html
<script src="key.js"></script>
```

4. In your app code, read the key from `window.OPENWEATHER_API_KEY`.

---

## Run the project

- Open `index.html` directly in your browser, **or**
- Serve the folder with a local static server and open it in the browser.

Then search for a city to see live weather results.

---

## Security notes

- Never commit API keys or secrets.
- If a key is exposed, rotate it immediately in OpenWeatherMap.
- Remove accidentally tracked secret files and commit the removal.
