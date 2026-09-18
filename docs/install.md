# Installing PLUI

## Google Play (recommended)

[play.google.com/store/apps/details?id=com.premium.tv.launcher.ui](https://play.google.com/store/apps/details?id=com.premium.tv.launcher.ui)

Search for **"TV Launcher Premium Smart UI"** on your TV's Play Store, or send it to your device from a phone. Updates arrive automatically.

## Sideload

Use this if the Play Store says your device is unsupported (common on Chinese TV boxes and on Fire TV).

1. Download the APK from [**Releases**](../../releases)
2. Install it with one of:
   - **[Downloader by Smartago](https://play.google.com/store/apps/details?id=com.downloader.tv.installer.xapk)** — paste the release URL on the TV
   - **Send Files to TV** or **Send to TV Quick** — push it from your phone
   - **ADB** — `adb install com.premium.tv.launcher.ui.apk`
3. Allow "install from unknown sources" if your device asks

> The sideload build is the same launcher; it updates itself instead of going through Play.

## After installing

1. **Open PLUI once** — it will offer to become your home app. See [home-button.md](home-button.md) if the HOME key still opens the old launcher.
2. **Pick your language** — 45 available, chosen on first run
3. **Choose a wallpaper** — Options › Theme. The glass panels take their colour from it.
4. **Build your sidebar** — Options › Sidebar: categories, apps, widget pages, each with its own icon
5. **Add the people in the house** — Options › Users, up to 10 profiles

## Requirements

- Android 6.0 (API 23) or newer
- Android TV, Google TV, Fire TV, or any Android TV box
- Works on 1080p and 4K; TV remotes only — no touchscreen needed

## Uninstalling

Set your old launcher back as the home app first (**Settings → Apps → Default apps → Home app**), then uninstall PLUI normally. Removing a launcher while it is still the home app leaves some devices without a home screen until you reboot.
