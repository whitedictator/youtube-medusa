# YouTube Medusa

YouTube Medusa brings the customization spirit of ReVanced and RVX to Android TV, with a familiar TV interface and controls designed for your remote. Skip sponsored segments, listen to translated videos, and recover from selected connection issues without leaving the player.

## Key features

- **SponsorBlock integration:** automatically skip community-marked sponsorships, with configurable handling of intros, outros, self-promotion and other segment categories. Skipping also applies when seeking back into a marked segment.
- **Ad controls:** filter supported video-ad data and hide promotional elements. Effectiveness depends on YouTube's current delivery behavior.
- **Yandex-powered dubbing:** select **Russian or English** directly from the TV player, next to the subtitles control. Adjust original and translated audio volumes, with automatic source-language detection.
- **Medusa Fix:** an optional connection-recovery mode that automatically tries alternative connection tactics and remembers successful ones. It can help with selected loading and playback problems and applies only to this app's connections.
- **TV-first settings:** a dedicated Medusa section in YouTube TV settings, navigable with a remote. Medusa menus use Russian on Russian-language systems and English otherwise; YouTube keeps its own language settings.
- **Return YouTube Dislike integration:** display community-provided dislike estimates.

## Dubbing languages

The Yandex/VOT translation backend supports source languages including **English, Russian, German, French, Spanish, Italian, Chinese, Japanese, Korean and Arabic**. Medusa offers **Russian and English as dubbing targets**. Arabic input relies on automatic language detection; it is not an Arabic output voice option.

Availability depends on the source video, language pair and translation service. Russian and English output have been tested on our stand; not every input/output pair has been independently verified. See the upstream [VOT language support table](https://github.com/ilyhalight/voice-over-translation/blob/master/LANG_SUPPORT.md).

Dubbing is **off by default**. Medusa Fix is **on by default**; updates preserve your saved preference.

## Downloads

[Download the latest release](https://github.com/whitedictator/youtube-medusa/releases/latest)

| APK | Choose this for |
| --- | --- |
| **Universal** | Both ARM32 and ARM64 in one download |
| **ARM32 / armeabi-v7a** | TVs with a 32-bit Android system, including the older Hi compatibility profile |
| **ARM64 / arm64-v8a** | TVs with a 64-bit Android system |

All three APKs contain the same features and use compatible packaging, the same package name (`local.rvxtv.youtube`) and signing certificate. Install the appropriate APK over your existing Medusa installation to retain settings.

Requires Android 7 or newer on a supported ARM device. Architecture depends on the Android system, not just the processor model.

<a id="update-with-obtainium"></a>

## Install and update with Obtainium

[Obtainium](https://github.com/ImranR98/Obtainium/releases/latest) installs Medusa from this repository's GitHub releases and checks for future updates.

### Install Medusa

1. Download and install Obtainium on your TV. Choose an Obtainium APK compatible with your device.
2. Open Obtainium, select **Add App**, and paste this repository URL:

   `https://github.com/whitedictator/youtube-medusa`

3. Confirm **Add**, then select **Install**. If Android asks, allow Obtainium to install unknown apps.
4. If asked to choose a Medusa APK, use the table below. Install only one variant.

| Medusa APK | Which one should I choose? |
| --- | --- |
| **Universal** | Contains ARM32 and ARM64. Choose this if you are unsure which ARM architecture your TV uses. |
| **armeabi-v7a (ARM32)** | For TVs running a 32-bit Android system. Uses the compatibility packaging that installed on the older Hi Android 9 TV. |
| **arm64-v8a (ARM64)** | For TVs running a 64-bit Android system. |

A 64-bit processor does not necessarily mean the TV runs 64-bit Android. All variants provide the same Medusa features.

### Keep Medusa updated

Keep Medusa in Obtainium's app list. Select **Check for Updates**, then **Update** when a newer version is available. You can also enable background update checks in Obtainium's settings; their availability depends on your TV's background-app restrictions.

Install updates over the existing Medusa app. **Do not uninstall it first:** your settings are preserved during a normal update. Keep the same APK variant for subsequent updates.

### One-tap setup by APK variant

If Obtainium is already installed, open **one** link below on the same device and confirm the import. These configurations filter future releases to your chosen APK variant:

- [Add Universal to Obtainium](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22local.rvxtv.youtube%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Fwhitedictator%2Fyoutube-medusa%22%2C%22author%22%3A%22whitedictator%22%2C%22name%22%3A%22YouTube%20Medusa%22%2C%22additionalSettings%22%3A%7B%22apkFilterRegEx%22%3A%22-universal%5C%5C.apk%24%22%2C%22appId%22%3A%22local.rvxtv.youtube%22%7D%7D)
- [Add ARM32 to Obtainium](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22local.rvxtv.youtube%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Fwhitedictator%2Fyoutube-medusa%22%2C%22author%22%3A%22whitedictator%22%2C%22name%22%3A%22YouTube%20Medusa%22%2C%22additionalSettings%22%3A%7B%22apkFilterRegEx%22%3A%22-armeabi-v7a%5C%5C.apk%24%22%2C%22appId%22%3A%22local.rvxtv.youtube%22%7D%7D)
- [Add ARM64 to Obtainium](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22local.rvxtv.youtube%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Fwhitedictator%2Fyoutube-medusa%22%2C%22author%22%3A%22whitedictator%22%2C%22name%22%3A%22YouTube%20Medusa%22%2C%22additionalSettings%22%3A%7B%22apkFilterRegEx%22%3A%22-arm64-v8a%5C%5C.apk%24%22%2C%22appId%22%3A%22local.rvxtv.youtube%22%7D%7D)

If your TV cannot open these links, use the manual repository-URL steps above and choose the matching APK when prompted.

## Compatibility and release status

Medusa is an experimental, unofficial project. The ARM32 compatibility packaging was successfully installed on a Hi VHIX-55U169TSY running Android 9. Universal 79.1 passed an update installation, home-page/image loading and video-playback checks on an Android 13 ARM64 test device. Universal and ARM64-only installation on physical models still need wider testing; compatibility with every TV is not guaranteed.

## Credits

Inspired by **ReVanced** and **ReVanced Extended (RVX)**. Built on YouTube TV 7.24.300, with integrations drawing on anddea, VOT, SponsorBlock, Return YouTube Dislike, ByeDPI and xHook. Component notices are included in the APK and patch-source archive.

This project is not affiliated with or endorsed by Google, YouTube, Yandex, ReVanced or RVX. Third-party software and services retain their respective rights and terms.
