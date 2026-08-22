# Third-Party Notices / 제3자 고지

This document describes the v0.1.0 distribution boundary and the optional external components Jamak can obtain at the user's request. It does not replace the exact generated npm and Rust notices, license texts, final extracted-file inventory, or CycloneDX SBOM required for an approved release.

PCssak Jamak's own application remains proprietary. Every third-party component remains under its own license, and those licenses are not changed by this repository or the Jamak EULA.

## Bundled application dependencies

The Jamak application is built with Tauri, Rust crates, React, and npm dependencies under licenses that include Apache-2.0, MIT, BSD-family, ISC, Zlib, Unicode-3.0, Unlicense, and MPL-2.0. Before public release, the exact versions and license texts must be regenerated from the final `package-lock.json` and Windows-target `Cargo.lock`, compared with the final binary inventory, and published with the same tag. A summary written before the final build is not an adequate substitute.

Unmodified MPL-2.0 Rust components identified in the current lock set include `cssparser`, `cssparser-macros`, `dtoa-short`, `option-ext`, and `selectors`. Their source archives are available by exact package name and version from [crates.io](https://crates.io/), and the license text is available from [Mozilla](https://www.mozilla.org/MPL/2.0/). The final release inventory determines the exact versions and obligations.

## Optional user-initiated downloads

The following items are not included in the v0.1.0 Jamak installer. Jamak downloads an item only after the user chooses to install it, uses a fixed upstream tag or commit, and verifies a pinned SHA-256 before use.

| Component | Current fixed source | License or terms |
| --- | --- | --- |
| FFmpeg Windows x64 static build | [BtbN autobuild `autobuild-2026-07-31-14-10`](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-07-31-14-10), asset `ffmpeg-N-125875-g5d4d3bdc61-win64-gpl.zip` | GPL-3.0-or-later for this selected build; bundled codec terms also apply |
| whisper.cpp CPU/CUDA x64 | [ggml-org/whisper.cpp v1.9.1](https://github.com/ggml-org/whisper.cpp/releases/tag/v1.9.1) | MIT and any file-specific notices in the release archive |
| OpenAI Whisper GGML model weights | [ggerganov/whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp), fixed repository commit in the application manifest | MIT; original Whisper copyright remains with OpenAI |
| Silero VAD v5.1.2 GGML model | [ggml-org/whisper-vad](https://huggingface.co/ggml-org/whisper-vad), fixed repository commit in the application manifest | MIT; original Silero copyright remains with the Silero Team |
| llama.cpp CPU/CUDA x64 | [ggml-org/llama.cpp b10068](https://github.com/ggml-org/llama.cpp/releases/tag/b10068) | MIT and any file-specific notices in the release archive |
| Qwen2.5 14B Instruct GGUF | [bartowski/Qwen2.5-14B-Instruct-GGUF](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF), fixed repository commit in the application manifest | Apache-2.0; original model copyright remains with the Qwen team |
| NVIDIA CUDA runtime files in optional CUDA archives | [NVIDIA CUDA Toolkit EULA](https://docs.nvidia.com/cuda/eula/) | NVIDIA terms for the included runtime files |
| Microsoft Visual C++ Redistributable x64 | [Microsoft official installer](https://aka.ms/vs/17/release/vc_redist.x64.exe) | Microsoft terms; Jamak does not automatically redistribute it |
| Microsoft Edge WebView2 Runtime | [Microsoft WebView2 distribution guidance](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) | Microsoft terms; Windows installer bootstrapper behavior may apply |

### FFmpeg distribution boundary

For v0.1.0, PCSSAK does not bundle FFmpeg in the Jamak installer, upload it as a Jamak release asset, or mirror it from a PCSSAK server. A user-initiated component installation downloads the exact pinned GPL build directly from the upstream BtbN GitHub release and checks the archive SHA-256 before extraction. See [FFmpeg source and distribution details](docs/THIRD-PARTY-SOURCE.md).

If a future release bundles or mirrors FFmpeg, PCSSAK must reassess the selected build, license, corresponding-source offer or delivery, build information, notices, patent considerations, and asset inventory before distribution. It must not reuse this v0.1.0 description as automatic approval.

H.264/AVC patent and licensing considerations are separate from FFmpeg's open-source license. Availability in an open-source build does not grant every patent license that may be required for every commercial, regional, or distribution use.

## Final-release gate

An approved public tag must match all of the following:

- generated npm and Windows-target Rust notices from the final lock files;
- the exact final NSIS application and optional extracted DLL inventory;
- the final CycloneDX SBOM and all dependency names, versions, licenses, hashes, and source locations;
- all complete license and attribution texts required for binary distribution;
- the versions and SHA-256 values embedded in the shipped application.

Until that comparison is complete, this repository must not publish an installer.

## 한국어

이 문서는 v0.1.0 배포 경계와 사용자가 선택할 때 Jamak이 내려받는 외부 구성요소를 설명합니다. 승인 릴리스에 필요한 정확한 npm·Rust 생성 고지, 라이선스 전문, 최종 추출 파일 인벤토리나 CycloneDX SBOM을 대신하지 않습니다.

PCssak Jamak 애플리케이션 자체는 독점 소프트웨어입니다. 제3자 구성요소는 각각의 라이선스를 따르며 이 저장소나 Jamak EULA가 그 조건을 바꾸지 않습니다.

Jamak은 Tauri, Rust 크레이트, React와 npm 의존성으로 빌드되며 Apache-2.0, MIT, BSD 계열, ISC, Zlib, Unicode-3.0, Unlicense, MPL-2.0 등이 포함될 수 있습니다. 공개 전에는 최종 `package-lock.json`과 Windows 대상 `Cargo.lock`에서 정확한 버전·라이선스 전문을 다시 만들고 최종 바이너리 인벤토리와 대조한 뒤 같은 태그에 공개해야 합니다. 최종 빌드 전에 작성한 요약은 이를 대신하지 못합니다.

현재 잠금 집합에서 확인된 수정하지 않은 MPL-2.0 Rust 구성요소에는 `cssparser`, `cssparser-macros`, `dtoa-short`, `option-ext`, `selectors`가 있습니다. 정확한 이름·버전의 원본 압축 파일은 [crates.io](https://crates.io/)에서, 라이선스 전문은 [Mozilla](https://www.mozilla.org/MPL/2.0/)에서 받을 수 있습니다. 실제 의무는 최종 릴리스 인벤토리를 기준으로 확정합니다.

위 표의 선택형 구성요소는 v0.1.0 Jamak 설치기에 들어 있지 않습니다. 사용자가 설치를 선택할 때만 고정된 상위 태그·커밋에서 내려받고 사용 전에 고정 SHA-256을 확인합니다.

특히 FFmpeg는 v0.1.0 설치기에 포함하거나 Jamak 릴리스 자산으로 올리거나 PCSSAK 서버에서 미러링하지 않습니다. 사용자가 구성요소 설치를 선택하면 BtbN의 고정 GitHub 릴리스에서 정확한 GPL 빌드를 직접 내려받고 압축 파일 SHA-256을 검사합니다. 자세한 내용은 [FFmpeg 원본 소스와 배포 경계](docs/THIRD-PARTY-SOURCE.md)를 확인하세요.

향후 FFmpeg를 동봉하거나 미러링하면 선택한 빌드·라이선스·대응 원본 소스 제공·빌드 정보·고지·특허 고려사항과 자산 인벤토리를 새로 검토해야 합니다. 이 v0.1.0 설명을 자동 승인으로 재사용하면 안 됩니다. H.264/AVC 특허·라이선스 문제는 FFmpeg 오픈소스 라이선스와 별개이며, 오픈소스 빌드에 기능이 있다는 이유만으로 모든 상업·지역·배포 용도의 특허 허락을 받는 것은 아닙니다.

승인 공개 태그는 최종 잠금 파일에서 만든 npm·Windows 대상 Rust 고지, 최종 NSIS 앱과 선택 구성요소 추출 DLL 인벤토리, 최종 CycloneDX SBOM의 이름·버전·라이선스·해시·원본 위치, 바이너리 배포에 필요한 전체 라이선스·귀속 문구와 앱에 고정된 버전·SHA-256을 모두 일치시켜야 합니다. 이 대조가 끝나기 전에는 설치기를 공개하면 안 됩니다.
