# Known Limitations

[한국어](KNOWN-LIMITATIONS.ko.md)

## Free Early Access status

- Jamak v0.1.0 is Free Early Access below version 1.0. Features, layouts, translations, component
  sources, model support, file behavior, and system requirements can change before a stable release.
- Undiscovered defects, crashes, performance problems, transcription errors, mistranslations,
  subtitle timing mistakes, rendering differences, and compatibility issues can remain.
- Solo-maintainer support has no guaranteed response, repair, update, or long-term-support deadline.
- Free availability does not promise a future 1.0 release, price, payment model, permanent feature,
  update schedule, or continued availability.

## Windows and installation

- The public build is x64 only. 32-bit Windows, native or emulated Windows on ARM, Windows S mode,
  Windows Server, macOS, Linux, and Wine are unsupported.
- A currently serviced Windows 11 Home/Pro x64 installation is recommended. Windows 10 22H2 x64
  receives limited Early Access compatibility only and is outside Microsoft's general support
  unless an applicable ESU program covers the device.
- A successful build or startup does not prove compatibility with every Windows update, GPU,
  driver, codec, media container, security product, language, policy, or storage configuration.
- The v0.1.0 installer is not Windows Authenticode-signed and can show Unknown publisher,
  SmartScreen, Smart App Control, or organization-policy blocking. Do not disable security controls.
- The current-user installer normally needs no administrator rights. A managed environment can
  still require administrator or IT approval for WebView2, runtime installation, policy changes,
  or optional components.

## Transcription and translation

- Speech recognition and AI translation are probabilistic. They can omit speech, invent text,
  confuse speakers or languages, mistranslate names and technical terms, or produce unsafe wording.
- Automatic language detection and English-direction translation are not guaranteed for short,
  noisy, overlapping, accented, musical, or mixed-language audio.
- Local model quality depends on the selected model, quantization, prompt, terminology, language
  pair, available memory, and hardware. A larger model is not a guarantee of correct output.
- Human review is required before publishing, accessibility use, legal or medical use, education,
  customer delivery, or another consequential workflow.

## Subtitle editing, preview, and export

- Preview and exported or burned-in output can differ because of font availability, fallback,
  line wrapping, resolution, scaling, container timestamps, codec behavior, and player differences.
- SRT and VTT do not preserve every ASS style or karaoke feature. Converting formats can discard
  unsupported information.
- Undo, redo, recovery sessions, and safe-write controls reduce risk but are not backup, version
  control, or guaranteed recovery after operating-system, storage, power, or external-program failure.
- Keep the original media and important subtitles in a separate tested backup. Review the actual
  exported file before deleting or replacing an earlier result.

## Video processing and external components

- Video burn-in uses an optional FFmpeg build obtained directly from the pinned upstream BtbN
  release. FFmpeg is not bundled or mirrored by PCSSAK in v0.1.0.
- Media decoding and encoding can fail on damaged files, unsupported codecs, unusual timestamps,
  variable frame rates, protected media, large dimensions, insufficient disk space, or hardware and
  driver limitations.
- H.264 output availability does not itself resolve every patent, licensing, delivery, or regional
  obligation for every user's project.
- CPU and CUDA packages have different compatibility, download size, memory, speed, and antivirus
  detection risks. Intel and AMD GPU acceleration is unsupported in v0.1.0.

## Privacy and network boundary

- Media, subtitle text, prompts, transcription, translation, and generated output are processed on
  the user's PC and are not sent to a PCSSAK processing server.
- This does not mean Jamak never uses the network. User-selected component downloads, update checks
  and approved update downloads, required WebView2 delivery, and user-opened websites or email can
  contact GitHub, Hugging Face, Microsoft, or another named provider.
- Those providers can independently process ordinary connection metadata such as IP address,
  request time, URL, and user agent under their own terms.
- A public GitHub Issue or email is outside the local-processing boundary. Remove media content,
  subtitle text, personal paths, filenames, customer data, credentials, and confidential material.

## Updates

- Tauri update signatures are mandatory for the in-app update path but are separate from Windows
  Authenticode and SmartScreen reputation.
- The initial v0.1.0 endpoint remains `204 No Content`; it must not offer v0.1.0 to the same v0.1.0
  client. A newer v0.1.1 or later update is offered only after release assets, signature, hashes,
  anonymous downloads, and installed upgrade behavior are independently verified.
- If the update service is unavailable, Jamak should fail safely without replacing the installed
  application. Use only the official release page for a manual update.

See [Quality and safety](QUALITY-AND-SAFETY.md), [installation](INSTALLATION.md),
[system requirements](../SYSTEM_REQUIREMENTS.md), and [support](../SUPPORT.md).
