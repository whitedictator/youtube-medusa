# Changelog

## 80.8 — 2026-11-02

- Add a gentle two-record TLS fallback after the existing connection tactics; preserve the existing order and saved successful choices.
- Strengthen video-tactic learning: require at least 64 KiB of additional server traffic and a connection age of three seconds, rather than learning from a small initial response alone.
- Detect prolonged playback waiting without timeline progress and retire stalled media tunnels so the native player can retry with another tactic.
- Withdraw the failed tactic's saved priority and remember a successful replacement for subsequent connections and app restarts.
- Leave connections alone while media data is arriving, including slow transfers; exclude user pause, seeking and ended playback from stall recovery.
- Limit recovery to two actual interventions per video, at least one minute apart. No-op inspections do not exhaust that budget.
- Show a brief Russian/English Medusa Fix notice when a recovery actually occurs, without taking remote focus.
- Add local player-state diagnostics for investigating black screens. No new background network probes.
- Hide Android system bars in the YouTube activity on boxes running ordinary Android; reapply fullscreen on resume without changing video aspect ratio.

Restricted-network effectiveness remains unverified; the Ugoos X3 black-screen report is not confirmed fixed.


## 80.7 — 2026-11-01

- Add an **AFR stats** button at the left of the native TV player controls. Press it again to hide the indicator.
- Show the video cadence measured from decoder timestamps, the current display resolution and refresh rate reported by Android, and the AFR request/status separately.
- Statistics also work with AFR disabled. Showing or hiding them does not toggle AFR or change the display mode.
- Keep the diagnostic indicator hidden by default and reset it to hidden on a fresh app start.
- Adapt player-button integration to the current YouTube TV controls while keeping Yandex dubbing beside captions.


## 80.6 — 2026-10-31

- Add experimental automatic frame-rate matching (AFR), **off by default**, in the native Medusa settings menu.
- Detect frame rate from the video decoder, including 23.976, 29.97 and 59.94 fps, and request a compatible refresh rate exposed by the firmware without reducing resolution.
- Respect Android's frame-rate matching policy where available; leave the display unchanged when no matching mode is supported.
- Restore the previous display request when AFR is disabled, playback ends or the app moves to the background.
- Preserve the settings and service-compatibility fixes from 80.5, existing preferences and update-compatible APK packaging.

Physical fractional refresh-rate switching remains unverified; AFR is experimental and off by default.


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
