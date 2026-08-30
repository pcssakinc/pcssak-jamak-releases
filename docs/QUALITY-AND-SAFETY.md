# Quality and Safety

[한국어](QUALITY-AND-SAFETY.ko.md)

This document describes the safety model and release evidence expected for PCssak Jamak. It is
an engineering standard, not a promise that the software has no defects or that AI output is
correct.

## Local subtitle workflow

Jamak is designed around a reviewable local sequence:

1. The user imports supported media or subtitle files.
2. Optional local engines produce transcription or translation candidates.
3. The user reviews cue text, timing, language, style, and preview.
4. Jamak writes a new subtitle or video output only after an explicit export or burn-in action.
5. Important output is reopened and reviewed in the intended player or delivery workflow.

AI output is always a candidate for human review. Product wording, interface labels, or model size
must not be treated as evidence that a transcript or translation is complete, accurate, lawful,
accessible, or suitable for a consequential purpose.

## Original and output safety

- Original media and imported subtitle files should not be modified merely by preview,
  transcription, translation, or editing.
- Export and burn-in destinations must be explicit. Existing output, changed paths, insufficient
  space, permission failure, file locks, and external changes should cause a clear refusal or
  confirmation rather than an unnoticed overwrite.
- Temporary and partial files should remain distinguishable from completed output and should not
  be advertised as successfully exported files.
- Undo, redo, recovery sessions, and atomic-write techniques reduce common failure risk but do not
  replace an independent backup.
- A successful preview is not proof that every player, font, codec, platform, and resolution will
  render the final output identically.

## Managed external components

Optional engines and models are downloaded only after the user chooses them. Each approved package
has a fixed upstream source, expected archive type, pinned SHA-256, extraction allowlist, storage
boundary, and executable invocation path. A mismatch, unexpected entry, incomplete download, or
unsafe path must fail closed rather than bypass verification.

FFmpeg is not bundled or mirrored in v0.1.1. The selected GPL build is obtained directly from the
documented BtbN release. whisper.cpp, llama.cpp, model weights, CUDA runtime files, WebView2, and
the Visual C++ runtime remain subject to their own upstream licenses, security lifecycle, and
compatibility limits.

## Privacy boundary

- Media, subtitles, prompts, transcription, translation, recovery data, and generated output stay
  on the user's PC during the core workflow.
- The public Free Early Access build has no PCSSAK account, advertising, telemetry, usage analytics,
  tracking SDK, or automatic crash upload.
- Narrow network exceptions are the fixed update check and user-approved update, user-selected
  component delivery, required WebView2 delivery, and links or messages the user opens.
- Public reports are not local. Issue forms and support guidance require removal of personal paths,
  media content, subtitle text, customer data, credentials, license keys, and confidential work.

## Installer and update integrity

The release process requires:

- the same application version across frontend, Tauri, Rust, release notes, tag, and metadata;
- a clean, reproducible source and lockfile state recorded for the exact build;
- a current-user multilingual NSIS installer with the final EULA and first-install language flow;
- a mandatory Tauri signature generated for the exact NSIS update asset;
- `latest.json`, CycloneDX SBOM, release notes, and `SHA256SUMS.txt` generated from final assets;
- explicit asset allowlists and rejection of private keys, passwords, tokens, logs, test media,
  developer paths, unexpected binaries, and stale build output;
- independent re-download and hash comparison before any public homepage link is enabled.

The Tauri signature protects the in-app update path. It is not Windows Authenticode. Until
Authenticode is adopted, Windows can identify the installer as an unknown publisher even when the
Tauri signature and SHA-256 are correct.

The fixed homepage endpoint remains `204 No Content` until the published v0.1.1 installer,
signature, metadata, hashes, and anonymous downloads pass independent checks. After those checks,
an explicitly owner-authorized controlled live trial may return `200 OK` to an installed v0.1.0
app so the upgrade can actually be tested. The end-to-end result remains `NOT_RUN` until download,
signature verification, installation, restart, and the displayed version all succeed. A failed
trial returns the endpoint to `204` immediately.

## Validation layers

Release approval should record results for the exact release in each relevant layer:

- frontend type checking, production build, Rust formatting, linting, unit and integration tests;
- subtitle parsing, timing boundaries, split/merge/edit history, search, format conversion, style,
  karaoke, preview, export, recovery, and safe-output regression tests;
- component download interruption, resume, SHA-256 mismatch, archive traversal, storage limits,
  removal, CPU and supported CUDA-path checks;
- localization completeness and placeholder consistency for the supported app and installer
  languages;
- clean installation, first-run, repair, update, removal, and app-data choice on the documented
  Windows editions;
- actual x64 Windows 10 22H2 and currently serviced Windows 11 Home/Pro testing to the extent claimed
  in that release note;
- Defender and current security-product scanning, SmartScreen behavior, unsigned-publisher warning,
  false-positive reporting, and no recommendation to disable protection;
- a final dependency inventory, complete third-party notices, source-offer obligations where
  applicable, SBOM comparison, and legal review for the intended distribution regions.

Passing automated tests does not replace installed-app, real-media, accessibility, localization,
security, licensing, and upgrade-path review. Unsupported or incomplete combinations must remain
identified as such in the release notes.

If the release owner decides not to run the clean-Windows installed `jamak.exe` SHA-256 comparison,
the release notes must contain the exact standalone disclosure
`NOT_RUN: clean-windows-install-and-sha256`. This records an unperformed test; it is not a pass or a
Windows compatibility claim. The actual exe/DLL inventory and source hashes, PE and Authenticode
state, Tauri signature, merged SBOM, third-party notices, and six-asset allowlist remain mandatory.
Likewise, owner acceptance of known jurisdiction or H.264/AVC patent risk is not a legal-compliance
approval.

See [Known limitations](KNOWN-LIMITATIONS.md), [Installation](INSTALLATION.md),
[Security](../SECURITY.md), and [Support](../SUPPORT.md).
