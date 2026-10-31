# YouTube Medusa

YouTube Medusa brings the customization spirit of ReVanced and RVX to Android TV, with a familiar TV interface and controls designed for your remote. Skip sponsored segments, listen to translated videos, and recover from selected connection issues without leaving the player.

## Key features

- **SponsorBlock integration:** automatically skip community-marked sponsorships, with configurable handling of intros, outros, self-promotion and other segment categories. Skipping also applies when seeking back into a marked segment.
- **Ad controls:** filter supported video-ad data and hide promotional elements. Effectiveness depends on YouTube's current delivery behavior.
- **Yandex-powered dubbing:** select **Russian or English** directly from the TV player, next to the subtitles control. Adjust original and translated audio volumes, with automatic source-language detection.
- **Medusa Fix:** an optional connection-recovery mode that automatically tries alternative connection tactics and remembers successful ones. It can help with selected loading and playback problems and applies only to this app's connections.
- **TV-first settings:** a dedicated Medusa section in YouTube TV settings, navigable with a remote. Medusa menus use Russian on Russian-language systems and English otherwise; YouTube keeps its own language settings.
- **Return YouTube Dislike integration:** display community-provided dislike estimates.
- **Built-in updates:** check GitHub Releases from Medusa, download the correct APK variant and install verified updates while keeping your settings.

## Dubbing languages

The Yandex/VOT translation backend supports source languages including **English, Russian, German, French, Spanish, Italian, Chinese, Japanese, Korean and Arabic**. Medusa offers **Russian and English as dubbing targets**. Arabic input relies on automatic language detection; it is not an Arabic output voice option.

Availability depends on the source video, language pair and translation service. Russian and English output have been tested on our stand; not every input/output pair has been independently verified. See the upstream [VOT language support table](https://github.com/ilyhalight/voice-over-translation/blob/master/LANG_SUPPORT.md).

Dubbing is **off by default**. Medusa Fix is **on by default**; updates preserve your saved preference.

## Current release: 80.6

Version 80.6 adds **experimental AFR (automatic frame-rate matching)**, off by default. Enable it in **Settings → YouTube Medusa → AFR: match frame rate**. Medusa detects the video's frame rate and requests a compatible mode exposed by the firmware, preserving resolution. It restores the previous display request when disabled, on playback end or when the app moves to the background.

Fractional rates such as 23.976, 29.97 and 59.94 are distinguished from integer rates. Hardware and firmware support determine which display modes are actually available; physical fractional switching still needs TV testing. Brief display blanking may occur during a supported switch. The 80.5 menu and service-compatibility fixes remain included.

Install over your existing Medusa to preserve preferences. See [CHANGELOG.md](CHANGELOG.md) for the release history.

## Downloads

[Download the latest release](https://github.com/whitedictator/youtube-medusa/releases/latest)

| APK | Choose this for |
| --- | --- |
| **Universal** | Both ARM32 and ARM64 in one download |
| **ARM32 / armeabi-v7a** | TVs with a 32-bit Android system, including the older Hi compatibility profile |
| **ARM64 / arm64-v8a** | TVs with a 64-bit Android system |

All three APKs contain the same features and use compatible packaging, the same package name (`local.rvxtv.youtube`) and signing certificate. Install the appropriate APK over your existing Medusa installation to retain settings.

Requires Android 7 or newer on a supported ARM device. Architecture depends on the Android system, not just the processor model.

## Installation and built-in updates

### First installation

1. Open the [latest release](https://github.com/whitedictator/youtube-medusa/releases/latest) and download **one** APK: Universal, armeabi-v7a (ARM32), or arm64-v8a (ARM64). Use Universal if you are unsure which ARM architecture your TV uses.
2. Transfer the APK to your TV or download it on the TV. Open it with your file manager and allow installation from that source if Android asks.
3. Install Medusa. If you already use an older version, install over it to keep your settings; do not uninstall first.

### Update directly from Medusa

Starting with **version 80**, an updater is included in the app.

1. Open **Settings → YouTube Medusa → Updates**.
2. Select **Check for updates**. Medusa also checks automatically after app launch; you can turn this option off on the update screen.
3. When a newer release is available, select **Download update**. Medusa keeps your installed APK variant: Universal, ARM32 or ARM64.
4. After download and verification, Android’s installer opens automatically. If installation was cancelled, select **Install update** to retry. If Android asks, allow Medusa to install apps from this source, then return to the app.
5. Confirm **Update** in the Android system installer. Your settings are retained.

Medusa checks the download checksum, package identity, version and signing certificate before handing the APK to Android. Installation requires your confirmation.

**Upgrading from 79.1 or earlier?** Install the latest version manually once using the APK from GitHub Releases. After that, use the built-in updater for future published releases.

## Compatibility and release status

Medusa is an experimental, unofficial project. All three variants retain Android 7+ compatibility packaging, including the ARM32 packaging previously installed on a Hi VHIX-55U169TSY with Android 9.

For 80.6, emulator checks cover the native AFR toggle with a remote, repeated settings entry, real decoder detection on a 30 fps video, 60 Hz mode acknowledgement, restoring original requests, and leaving unsupported fractional modes unchanged. Android 9 legacy-service regression checks passed. Both emulators expose only 1920×1080 at 60 Hz: physical fractional refresh-rate switching, HDR and HDMI receiver behavior remain unverified. See the release's `validation-public.json` for scope and limits.

## Credits

Inspired by **ReVanced** and **ReVanced Extended (RVX)**. Built on YouTube TV 7.24.300, with integrations drawing on anddea, VOT, SponsorBlock, Return YouTube Dislike, ByeDPI and xHook. The source player solver uses yt-dlp/ejs (Unlicense), Meriyah (ISC) and Astring (MIT). Component notices are included in the APK and patch-source archive.

This project is not affiliated with or endorsed by Google, YouTube, Yandex, ReVanced or RVX. Third-party software and services retain their respective rights and terms.
