# Manjaro Bot – Android dashboard

Shows bot status, latest signals (entry / SL / TP) and Start/Stop buttons.

## Build the APK
**Android Studio:** open this folder → Build → Build APK(s).
**No PC:** push to GitHub; Actions → "Build APK" → download `manjaro-debug-apk`.
**Manjaro Linux CLI:** `sudo pacman -S jdk17-openjdk gradle`, install Android SDK, then `gradle assembleDebug`.

## Run the bot server (Termux/VPS)
1. Edit `TOKEN` in `server/manjaro_server.py`.
2. `python3 server/manjaro_server.py`
3. In the app: ⋮ → Settings → enter `http://YOUR_IP:8080` and the same token.

Hook your bot into it: update `state` and append to `signals`.
Use a VPN/SSH tunnel or HTTPS rather than exposing plain http publicly.
