# Reviewer guide — Premium TV Launcher UI (PLUI)

For journalists, YouTubers and anyone writing a fair review. Three minutes to install, six things
to look at, and the limits we would rather you heard from us. Press kit with screenshots, logos and
a fact sheet: https://pluitv.com/us/press/ · Questions: support@smartago.net, subject "Press".

One name, two spellings: the app is **Premium TV Launcher UI (PLUI)**; Google Play lists it as
**"TV Launcher Premium Smart UI"**. Same app, one package: `com.premium.tv.launcher.ui`.

## 1. Install in three minutes

**Android TV / Google TV (Play):** open Google Play on the TV, search "Premium TV Launcher UI",
install, open. The start wizard asks for the launcher role — where the device allows it, HOME now
opens PLUI. Direct link: https://play.google.com/store/apps/details?id=com.premium.tv.launcher.ui

**Fire TV, or any box without Play (sideload):** in *Downloader TV* enter code **0245** (or fetch
https://smartago.net/us/downloads/com.premium.tv.launcher.ui.apk with any downloader), install,
open. The wizard walks through HOME capture (an accessibility service, only for the HOME key) and
auto-boot. The sideload build updates itself. Full steps: [install.md](install.md).

**From a phone:** search the Play Store on your phone and use *Install on more devices* to push it
to the TV. That is how most people install it.

## 2. The HOME button

The #1 question in every review, so here is the honest version. Google Play does not allow a Play
build to capture system buttons, and many TVs (Nvidia Shield, Sony, Xiaomi, Chromecast) offer no
"home app" picker. So:

- **Play build:** PLUI requests the launcher role. On devices that allow it, HOME goes to PLUI, the
  supported way. On locked TVs, our companion app *Button Mapper TV* (Downloader code 06350, also on
  Play) finds PLUI and offers to map HOME in one press.
- **Sideload build:** HOME capture is built in (accessibility service). Android TV 14 switches off
  accessibility services by itself on some devices; Android 13+ needs "Allow restricted settings".
- **Experts:** ADB (`pm disable-user` on the stock launcher) or Launcher Manager by sweenwolf.

Every route with screenshots: https://pluitv.com/us/home-button/ · [home-button.md](home-button.md)

## 3. Six things to look at

1. **Widgets over your wallpaper.** Home → *Widgets* → add a weather face (there are 82), a clock
   (38), a forecast, radio. Panels are glass: they take their colour from the picture behind them.
   Then change the wallpaper (Theme → Background: 8K gallery, aerial video, fine art, NASA, Reddit,
   or your own photos) and watch the widgets follow.
2. **"Who's watching?"** Users → add a second profile. Each person gets their own apps, sidebar,
   wallpaper, theme, language and widgets, optionally behind a PIN. Up to ten. The administrator
   decides what each profile may change.
3. **Screen-time limit.** Parental Control → PIN → *Daily screen time limit*. Set it to a few
   minutes to see what a child sees when it runs out. PIN per category hides whole groups of apps.
4. **A camera on the home screen.** Cameras → add. Any ONVIF camera or RTSP URL works. No camera at
   hand? Any public RTSP test stream will do for a screenshot, for example one of the streams
   listed by your NVR vendor or a local camera on the same Wi-Fi. It is a live viewer; it does not
   record.
5. **45 languages.** Settings → Language. The whole launcher switches live, no restart.
6. **The Edition screen.** Settings → Edition. Elite is the full edition and it is included at no
   cost — $0, forever, no trial, no unlock. Nothing to sign up for.

Also worth a look: rows-or-grid per category, the 100-slot sidebar editor (each slot with its own
icon and lock), remote shortcut buttons (red = Cameras, Num 1 = Games, inside the launcher), the
built-in tools (device info, speed test, free-up-space, cloud backup with one Device ID), and the
screensaver.

## 4. Known limits — please quote us on these

- **Profiles are launcher profiles, not streaming logins.** Netflix, Disney+ and the rest keep
  their own accounts and pickers. No launcher can change that.
- **No "Continue watching" row from other apps.** Android's Watch Next channel is readable only
  with a system-level permission (`ACCESS_ALL_EPG_DATA`, signature/privileged) that no Play or
  sideloaded launcher can hold. A third-party launcher that shows such a row is showing its own
  data, not Netflix's. We measured it; we would rather not fake it.
- **Cameras are viewed, not recorded.** Recording, motion alerts and cloud storage stay with your
  NVR or camera app.
- **HOME on locked TVs** needs Button Mapper TV or the sideload build (section 2).
- **Not minimal.** If your reader wants the home screen they notice least, Projectivy, AT4K, Monet
  or Arc are the right recommendation, and we say so: https://pluitv.com/us/honest-take/

## 5. Facts to copy (as of 20 September 2026)

| | |
|---|---|
| Publisher | Smartago (smartago.net) — same Play account as Downloader TV, Button Mapper TV, TV Setup Suite |
| Price | Free; Elite included at no cost. No ads, no account, no data sold |
| Google Play | 4.5★, 1,032 ratings, 100K+ installs, updated 17 September 2026 (read the live numbers from the listing) |
| Devices | Android TV 8+ and Google TV; Fire TV via sideload; Android projectors |
| Languages | 45 |
| Source | Launcher closed source; focus layer open source as TV Focus Kit (MIT): https://github.com/smartago/tv-focus-kit |
| Comparison | https://pluitv.com/us/compare/ — Projectivy, AT4K, Monet, Arc, PLUI on 18 facts from each app's own listing |
| Privacy policy | https://smartago.net/us/premium-tv-launcher-privacy-policy/ |
| Support | support@smartago.net, a person, 24–48 h · https://github.com/smartago/plui-tv-launcher/issues |

## 6. What we can give you

Screenshots of any scene on the device you name, a short b-roll clip, a fact checked the same
working day, and an honest answer about what the launcher does not do. What we do not do: pay for
reviews, ask for a rating, or send anything you did not ask for.
