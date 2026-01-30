# spotifyESPthing

this is like a spotify car thing, but like way cheaper (10-15$???)

# components
- a ssd1306 display (128x32)
- ESP32 (with WiFi)
- 4 wires


# how to set up
assuming you already have Arduino IDE and esp32 drivers, do this:
1. sign up for a Spotify Developer Account (https://developer.spotify.com)
2. Go to the Dashboard -> Create App
3. In here tou can name your app, description. The most important thing is to tick Web API and Web Playback SDK. Also, put this link into the Redirect URIs: https://spotify-refresh-token-generator.netlify.app/
4.