# Changelog

## 80.5 — 2026-10-31

- Keep Medusa settings rendering independent of private focus-reset helpers; retry if drawing has not completed.
- Open the Medusa section on Updates instead of an empty-looking Back page. Remote Back returns to the YouTube settings list.
- Remove misleading Google Play services install/update prompts from legacy optional-service checks, including stale update screens. Actual API errors and account-consent resolutions remain intact.
- Preserve saved settings, native sign-in, dubbing, SponsorBlock, Medusa Fix and the existing update path.
- Keep Universal, ARM32 and ARM64 packages with the older-TV compatibility packaging and the same signing certificate.


## 80.3 — 2026-10-28

- Improve source-audio retrieval using the current signed-in YouTube session and the TV engine's transport.
- Handle signature and rate-limiting parameters before downloading source audio; avoid using unprocessed player-response URLs as playable tracks.
- Fall back to standard Yandex voices when expressive voices require an unavailable Yandex session.
- Bound translation preparation and ignore stale results after a retry or video change.
- Offer **Turn off and retry** or **Keep enabled** after a connection error when Medusa Fix is on. The setting changes only when you choose; prompts are limited to one per 30 minutes.
- Add a Russian/English sign-in notice: **Yandex dubbing is not available in guest mode**.
- Treat the welcome and sign-in screens as loaded pages, avoiding unnecessary startup reloads during sign-in.
- Retain Universal, ARM32 and ARM64 compatibility packaging, the existing package identity and signing certificate.

## 80.2 — 2026-10-28

- Fix initial and repeated native Medusa settings entry rendering and selection reset.
- Consume remote confirmation for Medusa navigation without a duplicate stock action.
- Check for updates when opening the updater; show download progress and open Android’s installer automatically after successful verification.
- Keep Update Medusa available in the stock connection-error dialog, independently of Medusa Fix.
- Display release notes in startup prompts and manual checks; retain this version history.

## 80.1 — 2026-10-28

- Maintenance release for testing the built-in 80 → 80.1 update. Version metadata only; playback code unchanged.

## 80 — 2026-10-28

- Built-in GitHub Releases updater: startup/manual checks, exact APK variant selection, private downloads, checksum/package/version/signature verification and user-confirmed Android installation.
- Preserve app settings during updates. Universal, ARM32 and ARM64 releases retain compatibility packaging.

## 79.1 — 2026-10-27

- Universal, ARM32 and ARM64 release with compatibility packaging for older Android TV firmware.
- SponsorBlock, ad controls, Yandex Russian/English dubbing, Medusa Fix and remote-friendly Medusa settings.
