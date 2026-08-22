# PCssak Jamak - Official Windows Downloads

**Languages:** English · [한국어](README.ko.md)

[Product website](https://pcssak.com/jamak) · [Install guide](docs/INSTALLATION.md) · [Latest release](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest)

**Create, review, translate, style, and burn subtitles on your Windows PC.** PCssak Jamak brings local transcription, cue editing, subtitle styling, optional local AI translation, and video burn-in into one workflow.

> **Repository scope:** This is the official public binary-distribution, documentation, and issue-tracking repository for PCssak Jamak. The application source is private and proprietary; a public release repository is not an open-source code release.

> **Publication gate:** An installer is approved only when a GitHub Release for its exact tag is
> visible and contains the documented integrity files. If there is no release, there is no approved
> public Jamak build. Legal documents are published only after the application, installer, and
> website copies are finalized and matched.

## Download

Jamak v0.1.0 is available as a **Free Early Access** release for Windows x64. Download only from
the
[latest official release](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest) or
the [PCssak Jamak product page](https://pcssak.com/jamak).

- Use only `PCssak-Jamak-Beta-Windows-x64-Setup.exe` for the x64 Early Access installer.
- Do not use an MSI, x86, ARM64, portable, mirror, repackaged, or similarly named file.
- Compare the installer SHA-256 with `SHA256SUMS.txt` from the same release before running it.
- Confirm that the release also contains the Tauri updater `.sig`, `latest.json`, CycloneDX SBOM, and release notes for the same version.

> [!WARNING]
> The v0.1.0 installer and application are not Windows Authenticode-signed. Windows may show **Unknown publisher**, **Windows protected your PC**, or block execution under Smart App Control or organization policy. Do not disable SmartScreen, Microsoft Defender, Smart App Control, or another security product. Continue only after confirming the official source, exact filename, and SHA-256, and only on a PC where you accept the Early Access risk.

## What v0.1.0 does

All features included in v0.1.0 are available without payment during this Early Access release:

1. Local speech transcription with whisper.cpp, automatic language detection, and English-direction translation.
2. Import SRT and VTT; edit cue text and timing; split, merge, insert, delete, search, undo, and redo.
3. Export SRT, VTT, ASS, and TXT with subtitle styling and karaoke highlighting.
4. Preview subtitles on video and burn H.264 output with FFmpeg.
5. Optionally install llama.cpp and a local model for higher-quality local translation.
6. Install, verify, resume, inspect, or remove only the engines and models the user chooses.

This is not a promise about a future 1.0 release, pricing, payment method, support term, update schedule, or continued availability of a particular feature.

## Privacy and network use

- Media, subtitles, prompts, transcription, translation, and generated output are processed on the user's PC and are not uploaded to a PCSSAK server.
- Jamak has no PCSSAK account, advertising, telemetry, usage analytics, or automatic crash upload.
- Jamak stores a local recovery session so an interrupted edit can be restored.
- Network access is used for the fixed update check and a user-approved update, when the user
  chooses to install an engine or model, or when Windows needs WebView2 during installation.
  Component downloads come from fixed upstream GitHub or Hugging Face locations and are checked
  against pinned SHA-256 values.
- FFmpeg is not bundled in the Jamak installer or mirrored by PCSSAK for v0.1.0. The user-initiated component installer downloads the pinned GPL build directly from the upstream BtbN GitHub release. See [Third-party notices](THIRD-PARTY-NOTICES.md).

Ordinary HTTPS connection metadata, such as an IP address and request headers, can be processed by GitHub, Hugging Face, or Microsoft when those downloads are requested. Jamak does not send the user's media file to those services.

## Early Access boundary

- Supported beta platforms: Windows 10 version 22H2 x64 and supported Windows 11 x64, Home or Pro.
- Recommended platform: a currently serviced Windows 11 x64 installation with current security updates.
- Unsupported: 32-bit Windows, Windows on ARM, Windows S mode, Windows Server, macOS, Linux, Wine, and modified or repackaged components.
- Microsoft Edge WebView2 Runtime is required.
- AI transcription and translation can contain omissions, hallucinations, or mistranslations. Human review is required for important subtitles.
- Original media and important subtitle files should be backed up before installation or use.
- The app shows its current version and checks a fixed PCSSAK HTTPS endpoint for a verified newer version. When an update is available, the user explicitly starts the download and installation; the endpoint offers no update until publication is approved.
- Independently of the Windows Authenticode status, an in-app update is verified against the Tauri public key embedded in the app and the mandatory `.sig`. Jamak does not apply an update if that verification fails.
- Publishing the initial v0.1.0 installer does not offer v0.1.0 to itself. The update endpoint
  remains `204 No Content`; a verified v0.1.1 or later release can be returned as a newer update.

See the [installation guide](docs/INSTALLATION.md), [known limitations](docs/KNOWN-LIMITATIONS.md),
and [system requirements](SYSTEM_REQUIREMENTS.md) for setup, storage, memory, GPU, and runtime
details.

## Help improve Jamak

- Use the [bug report form](../../issues/new?template=bug-report.yml) for a defect you reproduced safely.
- Use the [feature request form](../../issues/new?template=feature-request.yml) to describe a recurring user problem and desired outcome.
- Read [Support](SUPPORT.md) before attaching screenshots or technical information.
- Report exploitable security details privately under [Security](SECURITY.md).

Do not upload original media, private subtitles, personal paths, customer data, credentials, license keys, or confidential work. Reports prepared with AI assistance must still be reproduced and verified by the submitter.

## Documentation

- [Korean introduction](README.ko.md)
- [Support](SUPPORT.md)
- [Security policy](SECURITY.md)
- [System requirements](SYSTEM_REQUIREMENTS.md)
- [Installation and update](docs/INSTALLATION.md)
- [Quality and safety](docs/QUALITY-AND-SAFETY.md)
- [Known limitations](docs/KNOWN-LIMITATIONS.md)
- [Third-party notices](THIRD-PARTY-NOTICES.md)
- [Issue and contribution guidelines](CONTRIBUTING.md)

PCssak Jamak binaries are distributed under the Jamak EULA that accompanies an approved release.
`PCSSAK` is the publisher and software-brand display name; this wording does not by itself assert
a particular registered legal-entity form. Third-party components remain under their own licenses.
PCSSAK is not affiliated with or endorsed by the upstream projects or service providers named in
the documentation.
