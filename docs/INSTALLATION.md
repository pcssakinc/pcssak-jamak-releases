# Install and Update PCssak Jamak

[한국어](INSTALLATION.ko.md) · [System requirements](../SYSTEM_REQUIREMENTS.md) · [Known limitations](KNOWN-LIMITATIONS.md)

This guide applies to the Windows x64 Free Early Access build. Download Jamak only from the
[official product page](https://pcssak.com/jamak) or this repository's
[latest release](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest).

## Before installation

1. Confirm that Windows is x64 and within the documented beta scope.
2. Download `PCssak-Jamak-Beta-Windows-x64-Setup.exe` and `SHA256SUMS.txt` from the same release.
3. Compare the installer's SHA-256 with the published value.
4. Keep a separate backup of important media and subtitle files.
5. Do not disable SmartScreen, Microsoft Defender, Smart App Control, or another security product.

The v0.1.0 installer is not Windows Authenticode-signed. Windows can therefore show **Unknown
publisher** or a reputation warning even when the downloaded bytes match the official SHA-256.
The hash confirms byte equality; it is not a code-signing certificate or a malware guarantee.

## First interactive installation

A normal first installation shows a language selector before the installer pages. The available
installer languages are English, Korean, Japanese, Simplified Chinese, Traditional Chinese,
Russian, Brazilian Portuguese, Latin American Spanish, German, and French.

Choose the installation language, review the final EULA displayed by the installer, and continue
only if you agree. `PCSSAK` is the publisher and software-brand display name. The final EULA that
ships with the exact release controls the license terms; a draft or a website preview is not a
substitute.

Jamak uses a **current-user installation**. Ordinary installation and removal do not request
administrator rights, and the application is installed inside the current Windows user's scope.
An organization policy or security product can still block an unsigned installer.

## Required and optional components

Microsoft Edge WebView2 Runtime is required for the interface. If it is missing, the installer
can use Microsoft's official WebView2 bootstrapper, which requires a network connection. Some
optional whisper.cpp and llama.cpp packages require Microsoft's Visual C++ 2015-2022 x64 runtime.

FFmpeg, transcription engines, models, and local-translation components are not bundled in the
v0.1.0 installer. Install only the components you need from Jamak settings. Jamak obtains them
from the fixed upstream location documented for that release and verifies the pinned SHA-256
before use. Large models require substantial download time, storage, memory, and sometimes GPU
resources.

## Repair, reinstall, and update

- A manual reinstall over an existing installation preserves the selected installer language and
  does not repeatedly present the first-install language and EULA pages.
- An in-app update runs in update mode and likewise does not interrupt with the first-install
  pages.
- Jamak displays its installed version. It checks the fixed PCSSAK HTTPS endpoint for a strictly
  newer, approved version and does not install anything silently.
- When an update is available, the user starts the download and installation. The updater must
  verify the mandatory PCSSAK Tauri signature before installation.
- The Tauri updater signature is separate from Windows Authenticode. A valid update signature
  does not remove the initial installer's Unknown publisher or SmartScreen warning.
- The initial v0.1.0 publication does not offer itself as an update. Its endpoint remains
  `204 No Content`; a verified v0.1.1 or later release can be offered with `200 OK` metadata.

If an update check fails, continue using the installed version or visit the official release page.
Do not bypass signature verification, substitute another download URL, or install a repackaged
copy.

## Uninstall

Use Windows **Installed apps** to remove PCssak Jamak. The uninstaller can offer removal of local
application data, but keeping it is the default so an accidental uninstall does not silently erase
settings or recovery information. Select data removal only after exporting important subtitles and
confirming that the data is no longer needed.

Downloaded engines, models, partial downloads, exported subtitles, rendered videos, Windows
Recycle Bin contents, and files stored outside Jamak's application-data scope can require separate
review or removal. Never delete an unfamiliar folder merely because it has a similar name.

See [Support](../SUPPORT.md) for safe troubleshooting and [Security](../SECURITY.md) for private
vulnerability reporting.
