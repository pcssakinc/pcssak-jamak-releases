# PCssak Jamak v0.1.1 System Requirements / 시스템 요구사항

## Supported beta environment

| Item | v0.1.1 Free Early Access boundary |
| --- | --- |
| Operating system | Windows 10 version 22H2 x64 or a supported Windows 11 x64 release |
| Edition | Windows 10/11 Home or Pro |
| Processor architecture | Intel or AMD x64 only |
| Display | 960 x 640 minimum window size; 1280 x 800 or higher recommended |
| Web runtime | Microsoft Edge WebView2 Runtime required |
| Network | Not required for ordinary editing after components are installed; required for missing WebView2 and user-selected engine/model downloads |

32-bit Windows, Windows on ARM native or emulated operation, Windows S mode, Windows Server, LTSC combinations not explicitly tested, Wine/Proton, virtual desktops, sandboxes, and managed enterprise-policy environments are outside the v0.1.1 support scope. v0.1.1 is distributed only as an NSIS current-user `Setup.exe`; no MSI is provided.

Microsoft ended general support for Windows 10 Home and Pro on October 14, 2025. Jamak's beta compatibility target does not restore Microsoft support or security updates. Windows 10 users should check Microsoft's current [Windows 10 support notice](https://support.microsoft.com/en-us/windows/windows-10-support-ended-on-october-14-2025-2ca8b313-1946-43d3-b55c-2b95b107f281) and [Extended Security Updates guidance](https://www.microsoft.com/en-us/windows/extended-security-updates). A currently serviced Windows 11 x64 release with current security updates is recommended.

## Required runtimes

### Microsoft Edge WebView2 Runtime

Jamak uses WebView2 for its interface. Most Windows 10/11 PCs already have it. If it is missing, the default Tauri installer can obtain Microsoft's WebView2 bootstrapper during installation, which requires an internet connection. Managed or offline environments should have an administrator deploy Microsoft's official [Evergreen Standalone Installer](https://developer.microsoft.com/microsoft-edge/webview2/) before installing Jamak.

### Microsoft Visual C++ 2015-2022 Redistributable x64

Some optional whisper.cpp and llama.cpp binaries can require the Microsoft Visual C++ runtime. If Windows reports `VCRUNTIME140.dll` or a related runtime error, install Microsoft's official [Visual C++ Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe). Do not download an individual DLL from an unofficial site.

## CPU, memory, and GPU guidance

These are practical beta recommendations, not performance guarantees for every media file or hardware combination.

| Workflow | Recommended memory | Hardware notes |
| --- | ---: | --- |
| Subtitle editing and SRT/VTT/ASS/TXT work | 8 GB or more | x64 CPU |
| CPU transcription with tiny/base/small models | 8 GB or more | Speed varies substantially by CPU and media length |
| Medium or large transcription models | 16 GB or more | Long media requires additional headroom |
| Qwen2.5 14B local translation | 16 GB minimum; 24 GB or more recommended | The model download is about 8.4 GB |
| CUDA transcription or translation | Sufficient NVIDIA VRAM for the selected model | Optional; a CPU path is available but can be much slower |

Intel and AMD GPU acceleration is not supported in v0.1.1. A particular NVIDIA GPU, driver, or CUDA combination is not guaranteed to work. Report tested hardware during Early Access without including a device serial number or account information.

## Storage and download sizes

Engines and models are not bundled in the installer. The user chooses which components to download from Jamak settings.

| Optional component | Approximate download size |
| --- | ---: |
| FFmpeg | 170 MB |
| whisper.cpp CPU | 10 MB |
| whisper.cpp CUDA | 650 MB |
| Whisper tiny/base/small | 78 MB / 148 MB / 488 MB |
| Whisper medium/large-v3-turbo/large-v3 | 1.53 GB / 1.55 GB / 3.10 GB |
| llama.cpp local-translation engine | About 600 MB |
| Qwen2.5 14B Q4_K_M translation model | About 8.4 GB |

- Reserve at least 1 GB for a basic CPU-oriented component set.
- Reserve 5 GB or more when combining CUDA transcription and large Whisper models.
- Reserve 20 GB or more for local LLM translation because the `.part` download and extraction can temporarily require additional space.
- Keep separate free space for video burn-in output, which can be as large as or larger than the original media.

Jamak settings show the actual stored size of each component and allow individual removal. Deleting a model, recovery session, or setting can be irreversible; export important subtitles and confirm the selected path first.

## 한국어

v0.1.1 무료 얼리액세스의 베타 지원 범위는 Windows 10 버전 22H2 x64 또는 지원 중인 Windows 11 x64의 Home·Pro입니다. Intel·AMD x64만 지원하며 최소 창 크기는 960 x 640, 권장 화면은 1280 x 800 이상입니다. Microsoft Edge WebView2 Runtime이 필요합니다.

32비트 Windows, Windows on ARM 네이티브·에뮬레이션, Windows S 모드, Windows Server, 별도 검증하지 않은 LTSC 조합, Wine/Proton, 가상 데스크톱, 샌드박스와 관리형 기업 정책 환경은 v0.1.1 지원 범위가 아닙니다. 공개 설치기는 현재 사용자 범위의 NSIS `Setup.exe` 한 종류만 준비하며 MSI는 제공하지 않습니다.

Microsoft는 Windows 10 Home·Pro의 일반 지원을 2025년 10월 14일 종료했습니다. Jamak의 Windows 10 베타 호환 범위가 Microsoft의 지원이나 보안 업데이트를 대신하지 않습니다. Windows 10 사용자는 Microsoft의 최신 [Windows 10 지원 종료 안내](https://support.microsoft.com/en-us/windows/windows-10-support-ended-on-october-14-2025-2ca8b313-1946-43d3-b55c-2b95b107f281)와 [확장 보안 업데이트 안내](https://www.microsoft.com/en-us/windows/extended-security-updates)를 직접 확인해야 합니다. 현재 지원 중이며 최신 보안 업데이트가 적용된 Windows 11 x64를 권장합니다.

Jamak 화면에는 WebView2가 필요합니다. PC에 없으면 Tauri 기본 설치기가 Microsoft WebView2 부트스트래퍼를 받을 수 있어 설치 중 인터넷이 필요합니다. 관리형·오프라인 환경은 IT 관리자가 Microsoft 공식 [Evergreen Standalone Installer](https://developer.microsoft.com/microsoft-edge/webview2/)를 먼저 배포해야 합니다.

일부 whisper.cpp·llama.cpp 바이너리는 Microsoft Visual C++ 런타임을 요구할 수 있습니다. `VCRUNTIME140.dll` 관련 오류가 나타나면 Microsoft 공식 [Visual C++ Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)를 설치하고 비공식 사이트에서 개별 DLL을 받지 마세요.

권장 메모리는 일반 자막 편집과 tiny/base/small CPU 전사에 8GB 이상, medium·large 전사에 16GB 이상입니다. 약 8.4GB Qwen2.5 14B 로컬 번역 모델에는 최소 16GB, 24GB 이상을 권장합니다. CUDA는 선택 기능이며 선택한 모델에 맞는 NVIDIA VRAM과 호환 드라이버가 필요합니다. Intel·AMD GPU 가속은 v0.1.1에서 지원하지 않으며 특정 NVIDIA GPU·드라이버·CUDA 조합의 성공도 보장하지 않습니다.

엔진과 모델은 설치기에 포함하지 않고 사용자가 설정에서 선택해 내려받습니다. 대략적인 크기는 FFmpeg 170MB, whisper.cpp CPU 10MB, CUDA 650MB, Whisper 모델 78MB에서 3.10GB, llama.cpp 엔진 약 600MB, Qwen2.5 14B 모델 약 8.4GB입니다. CPU 권장 구성에는 최소 1GB, CUDA와 큰 Whisper 모델에는 5GB 이상, 로컬 LLM 번역에는 부분 다운로드·추출 공간을 포함해 20GB 이상을 준비하세요. 영상 번인 출력용 여유 공간은 별도로 필요합니다.

설정에서 구성요소별 실제 저장 용량을 확인하고 개별 삭제할 수 있습니다. 모델·복구 세션·설정을 삭제하면 복구하지 못할 수 있으므로 중요한 자막을 먼저 내보내고 선택 경로를 확인하세요.
