# Making the HOME button open PLUI

This is the most asked question about every custom Android TV launcher, and the honest answer is: **it depends on your device.** There are two completely different mechanisms, and knowing which one you are using explains every strange behaviour you may hit.

## The two mechanisms

**1. The setting (the good one).** The system itself knows your launcher is HOME. You press HOME, the system takes you there. Nothing runs in the background, nothing can be "lost". This is what happens on any device that offers a real default-launcher choice.

**2. Key interception (the fallback).** The stock launcher keeps the HOME role and an accessibility service *catches* the key press and redirects it. It works, but it is a patch: the service must stay enabled, and on most devices it is switched off by a force-stop (including when you swipe the app away from Recents).

PLUI asks for the setting first, every time. Accessibility is only offered where the setting does not exist.

## Google TV / Android TV (Android 10+)

1. Install PLUI
2. Open PLUI once — it will offer to become your home app
3. Accept the system dialog ("Make PLUI your Home app?")

If the dialog never appears: **Settings → Apps → Default apps → Home app → PLUI**. Done — no accessibility needed.

## Older Android TV (Android 6–9)

Same idea, different menu: **Settings → Apps → Home app** (or "Launcher"). If your box has no such entry, see the next section.

## Fire TV

Fire OS has no default-launcher setting at all — Amazon keeps HOME for its own launcher. Options:

- Use PLUI's accessibility shortcut (PLUI will guide you), or
- Use a third-party helper such as **Launcher Manager** (see below)

## TV boxes that ignore the setting

Many inexpensive boxes hard-wire HOME to their own launcher, no matter what the "default app" setting says. Two ways out:

**Launcher Manager** — a well-known no-root helper app (originally from XDA) that changes the real default launcher. It works by enabling *ADB over network* and talking ADB to the device itself, then disabling or overriding the stock launcher. It is not magic and it is not a hack of PLUI: it writes the system setting, which is exactly mechanism 1 above. Once it has done its job, **no accessibility service is needed at all** — the HOME key genuinely belongs to PLUI.
*You will need to enable Developer options → ADB debugging (network) and accept the "Always allow" prompt.*

**PLUI's accessibility shortcut** — no ADB, no developer options, works everywhere, but it is mechanism 2: if something force-stops PLUI, re-enable the service.

> We would rather you use Launcher Manager or the system setting. An accessibility service is our fallback, not our preference.

## Why HOME sometimes stops working after an update

If the launcher was set through accessibility and the service got switched off (force-stop, "clear data", some system updates), HOME goes back to the stock launcher. Re-enable the service — or better, take the ADB route above so it cannot happen again.

## Getting back to the stock launcher

Nothing is locked. **Settings → Apps → Default apps → Home app** and pick the original, or uninstall PLUI. If your box has no such screen, Launcher Manager reverses its own change.
