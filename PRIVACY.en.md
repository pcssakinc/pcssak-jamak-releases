# PCssak Jamak Privacy and Local Data Notice

- Applies to: v0.1.1 Free Early Access
- Last updated: August 30, 2026
- Product display name: PCssak Jamak
- App and web operator display name: PCSSAK
- Privacy contact: privacy@pcssak.com

## Language and operator notice

This English text is a convenience translation of [PRIVACY.md](PRIVACY.md). The Korean text
is the source of record. This translation has not been represented as separately reviewed by
local legal counsel, and mandatory law applicable to you prevails wherever it provides
otherwise.

`PCSSAK` is the operator display name used for the Jamak app and its official web and update
channels. This does not separately represent that PCSSAK is a registered company or registered
business name. The Free Early Access release does not publish a physical postal address and
uses the email address above as the official contact for privacy questions and rights requests.
If mandatory law or a distribution platform in your country requires additional legal identity,
postal-address, or local-representative information, that requirement prevails, and distribution
or some support in that region may be restricted until the requirement is satisfied.

## Key points

- Jamak processes opened video, audio, subtitles, and generated results on your PC.
- The Jamak app has no account, advertising, telemetry, usage analytics, or automatic crash-report upload.
- Jamak does not upload media, subtitles, prompts, or translation results to a media-collection server operated by the Jamak operator.
- A distribution build connects once after launch to the PCSSAK update endpoint to check whether a new version is available. The request does not contain media, subtitles, or local paths.
- If you choose component installation, Jamak connects to GitHub or Hugging Face. If WebView2 is absent, the Windows installer may connect to Microsoft.
- Editing sessions and settings are stored locally for crash recovery and convenience.

This notice describes the current behavior of the Jamak desktop app. If the website later adds
a contact form, payment, sign-in, advertising, cookies, or visitor analytics, a separate notice
and any required consent flow must be added for the actual web service.

## Data processed locally by the app

| Item | Purpose | Default location or form | External transmission |
|---|---|---|---|
| Media and subtitles you open | Playback, transcription, editing, translation, and burn-in | Original location selected by you and temporary working files | None |
| Auto-saved session | Restore editing after a crash | `%LOCALAPPDATA%\com.pcssak.jamak\session.json` | None |
| Engines and models | Transcription, media processing, and local translation | `%LOCALAPPDATA%\com.pcssak.jamak\tools` and `models` | None |
| Language, selected model, burn-in quality, cue length, terminology rules, and user styles | Preserve settings | WebView2 local storage and app-local data | None |
| Offline license key and purchaser name contained in the key | Future local entitlement verification | `%APPDATA%\com.pcssak.jamak\license.key`, only if you enter a key | Verification is local |

The auto-saved session contains the local path of the source media, subtitle cues, subtitle
style, and save time, not the media file itself. A local path may contain a user name or folder
name, so delete it after use on a shared PC.

Jamak may create extracted audio and burn-in temporary files in a working temporary location.
It is designed to remove those files after success, cancellation, or a handled error, but it
cannot completely rule out remnants after an abnormal termination.

## When the network is used

Media processing itself does not require the internet. Network access is required or may occur
for the following operations.

| Network operation | Destination | Data downloaded | Media transmitted |
|---|---|---|---|
| Automatic check after launch or manual update check in Settings | `https://pcssak.com/jamak/update/latest.json` and its web hosting or CDN | No-update response or version, release-note, signature, and download-URL metadata | None |
| You select `Update and restart` | The official PCSSAK update asset URL specified by that metadata | NSIS update package verified with a Tauri signature | None |
| Install FFmpeg, whisper.cpp, or llama.cpp | `github.com` and GitHub release-asset servers | Fixed-version ZIP files, executables, and DLLs | None |
| Install Whisper, VAD, or Qwen models | `huggingface.co` and its CDN | Model files from a fixed commit | None |
| Install the app when WebView2 is absent | Microsoft WebView2 distribution service | WebView2 bootstrapper and runtime | None |
| You send support email | Your email service and the receiving email service | Content and attachments you choose to send | Only content you choose |

External services may process ordinary HTTPS metadata such as IP address, access time, user
agent, and the requested file. Their own privacy policies and terms apply.

- [GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
- [Hugging Face Privacy Policy](https://huggingface.co/privacy)
- [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement)
- [Cloudflare Privacy Policy](https://www.cloudflare.com/privacypolicy/)

The update hosting or CDN may retain standard web-request logs such as IP address, request time,
and user agent. This differs from an analytics SDK or media upload, but it does mean that network
metadata can exist.

Jamak downloads optional external assets from fixed URLs and verifies SHA-256 before use. App
updates are verified by the Tauri updater with the public key bundled in the app, and a package
with an invalid signature is not installed. Integrity verification does not eliminate the
external service's own processing of network metadata.

## Review and delete local data

### Delete only components

1. Open `Settings` in Jamak.
2. Select delete beside FFmpeg, whisper.cpp, the CUDA engine, transcription model, AI engine, or AI model. If a cancelled or failed `.part` download remains, review its size under `Partial download files` and delete it separately if you will not resume it.
3. After you confirm, Jamak deletes the selected local file. You can download it again later.

### Delete the auto-saved session

1. Export any subtitles you need as SRT, VTT, ASS, or TXT.
2. Select `Settings → Open data folder`.
3. Exit Jamak completely.
4. Delete `session.json` from the opened folder.

Opening a new video or subtitle may replace the previous document and auto-save after
confirmation. If you need definite deletion, delete the file directly as described above.

### Delete all Jamak local data

1. Back up any results you need and exit Jamak.
2. Uninstall Jamak from Windows Apps. The uninstaller's `Delete app data` option is unchecked by default so an ordinary uninstall preserves recoverable local work unless you explicitly select deletion.
3. To remove remaining data, delete `%LOCALAPPDATA%\com.pcssak.jamak` yourself.
4. If you entered an offline license key, deactivate it in the app first or delete `%APPDATA%\com.pcssak.jamak\license.key` after the app exits.
5. A PC used for private older builds may contain `%APPDATA%\com.pcssak.jamak` or data under a previous identifier. Inspect and delete only paths created by versions you tested.

Deleting the whole folder also deletes subtitle recovery data, downloaded models, and user
settings that cannot then be restored. Confirm the exact path before deletion.

## Support email

Support email is a communication you initiate; it is not automatic collection by the Jamak app.
Do not send personal information, source video or audio, private subtitles, or a complete license
key unless necessary. If a reproduction file is essential, first agree by email on a secure
transfer method and the minimum required scope.

Before adding a web contact form or analytics, PCSSAK must update the notice for the actual
operator, collected fields, purposes, retention, processors, international handling, and deletion
request process.

## Changes

If the app's network or storage behavior changes, the date and applicable version of this notice
will be updated. A future policy change does not retroactively treat continued use of v0.1.1 as
consent to new data collection.
