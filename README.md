# spotifyESPthing

this is like a spotify car thing, but like way cheaper (10-15$???)

# components
- a ssd1306 display (128x32)
- ESP32 (with WiFi)
- 4 wires
<img width="970" height="773" alt="image" src="https://github.com/user-attachments/assets/f60f459b-79ba-4df9-ad79-9923104662d0" />


# how to set up
assuming you already have Arduino IDE and esp32 drivers, do this:
1. sign up for a Spotify Developer Account (https://developer.spotify.com)
2. Go to the Dashboard -> Create App
3. In here tou can name your app, description. The most important thing is to tick Web API and Web Playback SDK. Also, put this link into the Redirect URIs: https://spotify-refresh-token-generator.netlify.app/
4. After you've created the app, you will need to grab your Client ID and Secret ID, paste them into notepad
5. Open this website https://spotify-refresh-token-generator.netlify.app/#welcome (click on Get started -> Already got the required data? Skip this step
6. Paste in your Client ID and Secret ID, and the Direct URI to be the same as on spotify (https://spotify-refresh-token-generator.netlify.app)
7. Check the following boxes: user-read-currently-playing and user-read-playback-state
8. Click on Get Spotify code. You should see your code, and that's is the Refresh Token (which is very important)
9. Go to my github and download the latest release (https://github.com/gabaznv/spotifyESPthing/releases/tag/SpotifyESPthing)
10. Open the file in the Arduino IDE app
11. Once you've opened this, you will need to make a few settings:
```
const char* ssid         = "YOUR_WIFI_NAME"; // put in your wifi name
const char* password     = "YOUR_WIFI_PASS"; // wifi password
const char* clientId     = "YOUR_CLIENT_ID"; // client id (can be grabbed from spotify)
const char* clientSecret = "YOUR_CLIENT_SECRET"; // client secret (can be grabbed from spotify)
const char* refreshToken = "YOUR_REFRESH_TOKEN"; // refresh token (the latest string we've grabbed, that we've generated)
```
If you did all of them correctly, it should display it on your screen realtime

# TWEAKS:
```bool scrollable_text = true;``` - line 18 (if the music title is too long, it will start scrolling it. Disabling it will disable the scrolling effect) <br>
```int scroll_speed     = 150;``` - line 19 (how fast the music title should scroll, lower value = faster) <br>
```const int delayBetweenRequests = 3000;``` - line 31 (this means that it will check what song you're playing every 3 seconds, and it will be kinda delayed. I recommend going somewhere around 1000ms)

# SUPPORT:
if you wanna support me by donating (and putting all my heart into this project), you can donate through my ko-fi
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/P5P610O2U7)
