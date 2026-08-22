# PCssak Jamak 0.1.0 - Free Early Access

상태: **v0.1.0 공개 후보 — 2026-08-22 UTC 검증 기록**

PCssak Jamak의 첫 Windows x64 무료 얼리액세스입니다. 자막 전사·편집·번역·스타일·내보내기와
영상 번인을 하나의 로컬 작업 흐름으로 제공합니다. 1.0 이전 버전이므로 화면·번역·지원 범위가
바뀔 수 있고 발견되지 않은 오류가 남아 있을 수 있습니다.

## English summary

This is the first Windows x64 Free Early Access release of PCssak Jamak. It combines local
transcription, cue and timing editing, local translation, subtitle styling and export, and optional
FFmpeg video burn-in. Human review is required for AI-generated transcription and translation.

Download only `PCssak-Jamak-Beta-Windows-x64-Setup.exe` from this official release and compare it
with `SHA256SUMS.txt`. The v0.1.0 installer is not Windows Authenticode-signed and can show Unknown
publisher or SmartScreen. Do not disable Windows security controls. The separate `.exe.sig` is the
mandatory Tauri in-app update signature; it does not replace Authenticode.

A normal first interactive installation offers English, Korean, Japanese, Simplified Chinese,
Traditional Chinese, Russian, Brazilian Portuguese, Latin American Spanish, German, and French,
then displays the final Korean-English EULA. Jamak installs for the current Windows user and
ordinary installation or removal does not require administrator rights.

Core media, subtitle, prompt, transcription, translation, and output processing stays on the
user's PC. Narrow network exceptions include the fixed update check, user-approved updates and
component downloads, required WebView2 delivery, and links or messages opened by the user. The
initial v0.1.0 endpoint remains `204 No Content`; only a verified v0.1.1 or later release can be
offered as an update.

The beta scope is Windows 10 22H2 x64 and supported Windows 11 Home/Pro x64; a currently serviced
Windows 11 x64 installation is recommended. 32-bit Windows, Windows on ARM, Windows S mode,
Windows Server, macOS, Linux, and Wine are unsupported. Read the installation guide, known
limitations, quality and safety document, system requirements, EULA, and privacy policy before
using important media.

## 한국어

## 다운로드

공식 자산은 다음 여섯 개뿐입니다.

1. `PCssak-Jamak-Beta-Windows-x64-Setup.exe`
2. `PCssak-Jamak-Beta-Windows-x64-Setup.exe.sig`
3. `latest.json`
4. `sbom-jamak-0.1.0.cdx.json`
5. `RELEASE_NOTES_v0.1.0.md`
6. `SHA256SUMS.txt`

Windows x64에서만 사용합니다. MSI, x86, ARM64, 포터블, 미러·재패키징 파일은 공식
v0.1.0 자산이 아닙니다. 실행 전 같은 릴리스의 `SHA256SUMS.txt`와 설치기 SHA-256을
비교하세요.

## 미서명 설치기 안내

v0.1.0은 Windows Authenticode로 서명되지 않아 알 수 없는 게시자, SmartScreen 또는 Smart
App Control 경고가 나타날 수 있습니다. 공식 저장소·정확한 파일명·SHA-256을 모두 확인하고
얼리액세스 위험을 받아들일 수 있을 때만 설치하세요. 설치를 위해 SmartScreen, Microsoft
Defender나 다른 보안 제품을 끄지 마세요.

Tauri 업데이터 `.sig`는 Authenticode와 별개인 필수 서명입니다. 앱 내부 업데이트는 이 서명을
검증하지만 Windows 게시자 평판 경고를 없애지는 않습니다.

## 처음 설치

- 정상적인 최초 대화형 설치에서 영어, 한국어, 일본어, 중국어 간체·번체, 러시아어,
  포르투갈어(브라질), 스페인어(라틴아메리카), 독일어, 프랑스어 중 설치 언어를 선택합니다.
- 최종 EULA를 읽고 동의할 때만 계속합니다.
- 현재 사용자 범위로 설치하므로 일반 설치·제거에는 관리자 권한이 필요하지 않습니다.
- 제거할 때 로컬 앱 데이터는 기본 유지이며 사용자가 별도로 삭제를 선택할 수 있습니다.

자세한 내용은 [설치 안내](docs/INSTALLATION.ko.md)와 [English installation guide](docs/INSTALLATION.md)를
확인하세요.

## 주요 기능

- whisper.cpp 기반 로컬 음성 전사와 자동 언어 감지
- SRT·VTT 가져오기, 자막 문구·시간 편집, 분할·병합·삽입·삭제·검색·실행 취소·다시 실행
- SRT·VTT·ASS·TXT 내보내기, 자막 스타일과 카라오케 하이라이트
- 영상 위 자막 미리보기와 선택형 FFmpeg 기반 H.264 영상 번인
- 선택형 llama.cpp·로컬 모델 번역
- 엔진·모델 선택 설치, 고정 SHA-256 검증, 이어받기, 저장 용량 확인과 개별 제거

## 개인정보와 네트워크

미디어·자막·프롬프트·전사·번역·출력은 사용자 PC에서 처리되며 PCSSAK 처리 서버로 보내지
않습니다. PCSSAK 계정, 광고, 텔레메트리, 사용량 분석, 추적 SDK와 자동 오류 업로드가
없습니다.

고정 업데이트 확인, 사용자가 승인한 업데이트·구성요소 다운로드, 필요한 WebView2 전달,
사용자가 직접 연 외부 링크·이메일에는 네트워크를 사용할 수 있습니다. GitHub·Hugging Face·
Microsoft 등 각 제공자는 일반 HTTPS 연결 메타데이터를 독립적으로 처리할 수 있습니다.

## 업데이트 동작

앱은 현재 버전을 표시하고 고정 PCSSAK HTTPS 엔드포인트에서 더 높은 승인 버전을 확인합니다.
최초 v0.1.0 공개 시 엔드포인트는 `204 No Content`를 유지하며 같은 v0.1.0을 업데이트로
제안하지 않습니다. 검증된 v0.1.1 이상이 공개된 뒤에만 새 버전의 `200 OK` 메타데이터를
제공할 수 있습니다.

## 지원 환경과 한계

- 베타 범위: Windows 10 22H2 x64, 지원 중인 Windows 11 Home·Pro x64
- 권장: 최신 보안 업데이트가 적용된 지원 중인 Windows 11 x64
- 미지원: 32비트 Windows, Windows on ARM, Windows S 모드, Windows Server, macOS,
  Linux와 Wine
- Microsoft Edge WebView2 Runtime 필요
- AI 전사·번역 결과는 사람이 검수해야 함
- 중요 원본과 자막은 별도 백업 필요

[알려진 한계](docs/KNOWN-LIMITATIONS.ko.md), [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md),
[시스템 요구사항](SYSTEM_REQUIREMENTS.md)을 확인하세요.

## 이 릴리스의 실제 검증 기록

공개 후보는 소스 커밋 `7ecccd16778e9dbaf0ab4eb809babaee2e7c56f8`에서 2026-08-22 UTC에
만들었습니다. 결정적 EULA RTF 생성, EULA 동등성, 설치기 계약, 프런트엔드·Rust 릴리스 빌드,
실제 PE·VersionInfo·Authenticode `NotSigned`, 고정 공개키를 사용한 Tauri 설치기 서명,
CycloneDX 병합 SBOM, 생성된 npm·Rust 고지, 바이너리 인벤토리와 여섯 자산 해시를 로컬 최종
검증기로 대조했습니다. 설치기 SHA-256은
`166aa60718c510ace83010132cddd8fb3850101dd7d2354d9a5296e5fc7810dc`입니다.

별도 깨끗한 Windows 장치에서의 설치 후 `jamak.exe` 해시 대조와 아래 실기 행렬은 출시
소유자 지시에 따라 실행하지 않았습니다. 따라서 Windows 설치 성공·호환성·보안 제품 무경고를
검증했다고 주장하지 않으며, 이 미실행에 따른 알려진 얼리액세스 위험을 수용합니다.

NOT_RUN: clean-windows-install-and-sha256

| 검증 | 2026-08-22 UTC 결과 |
| --- | --- |
| 소스·잠금 파일·빌드 | 승인된 private origin SHA 일치, 추적 파일 clean, `npm run release:build` 통과 |
| EULA·설치기 정적 계약 | `npm run eula:rtf`, `verify:eula`, `verify:installer` 통과 |
| Windows 10 22H2 x64 | 실제 설치·시작·핵심 작업·제거 `NOT_RUN` |
| Windows 11 Home x64 | 실제 설치·시작·핵심 작업·제거 `NOT_RUN` |
| Windows 11 Pro x64 | 실제 설치·시작·핵심 작업·제거 `NOT_RUN` |
| 10개 설치 언어·EULA | 정적 계약만 통과, 최초 설치·덮어설치·업데이트·제거 실기 `NOT_RUN` |
| Defender·SmartScreen | 실제 검사·경고 흐름·오탐 확인 `NOT_RUN`; Authenticode `NotSigned` 확인 |
| Tauri 업데이트 | 릴리스 자산 서명 검증 통과; 실제 정상·변조 인앱 업데이트 E2E `NOT_RUN`; v0.1.0 엔드포인트는 204 유지 |
| 설치기 페이로드 | 깨끗한 Windows 설치 후 빌드 원본과 SHA-256 대조 `NOT_RUN`; 알려진 위험 수용 |
| SHA-256·SBOM·제3자 고지 | 최종 여섯 자산, 병합 SBOM, 생성 고지와 외부 인벤토리 해시 대조 통과 |
| 출시 소유자 위험 수용 | PCSSAK 표시명, 신원·주소 비공개, 법률 적합성 비주장, 알려진 국가별 위험 수용 |
| H.264/AVC | 법률 적합성 비주장, 알려진 특허 위험의 출시 소유자 수용 |

## 제보

재현 가능한 오류는 공식 버그 양식을, 기능 제안은 사용자 문제 중심의 기능 제안 양식을
사용하세요. 원본 미디어·자막·개인 경로·고객 자료·자격증명·회사 비밀을 공개 Issue에 올리지
마세요. 악용 가능한 보안 문제는 `SECURITY.md`에 따라 비공개로 보내세요.
