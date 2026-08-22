# PCssak Jamak - 공식 Windows 다운로드

[English](README.md) · [제품 홈페이지](https://pcssak.co.kr/jamak) · [설치 안내](docs/INSTALLATION.ko.md) · [최신 릴리스](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest)

**Windows PC 한 대에서 자막을 만들고, 검수하고, 번역하고, 꾸미고, 영상에 입힙니다.** PCssak Jamak은 로컬 음성 전사, 자막 큐 편집, 스타일, 선택형 로컬 AI 번역과 영상 번인을 한 작업 흐름으로 연결합니다.

> **저장소 범위:** 이곳은 PCssak Jamak의 공식 바이너리 배포·문서·이슈 접수 저장소입니다. 애플리케이션 소스는 비공개 독점 소프트웨어이며, 공개 릴리스 저장소가 오픈소스 코드 공개를 뜻하지 않습니다.

> **공개 조건:** 정확한 태그의 GitHub Release가 실제로 보이고 그 버전의 무결성 파일이
> 함께 있을 때만 설치기가 승인된 것입니다. 릴리스가 없다면 공개 승인된 Jamak 빌드도
> 없습니다. 법적 문서는 앱·설치기·홈페이지 사본을 확정하고 일치시킨 뒤에만 공개합니다.

## 다운로드

Jamak v0.1.0은 Windows x64용 **무료 얼리액세스**로 준비합니다. 승인된 릴리스가 게시되면
[최신 공식 릴리스](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest) 또는
[PCssak Jamak 제품 페이지](https://pcssak.co.kr/jamak)에서만 내려받으세요.

- x64 얼리액세스 설치기는 `PCssak-Jamak-Beta-Windows-x64-Setup.exe`만 사용합니다.
- MSI, x86, ARM64, 포터블, 미러, 재패키징 또는 비슷한 이름의 파일은 사용하지 않습니다.
- 실행 전에 같은 릴리스의 `SHA256SUMS.txt`와 설치기 SHA-256을 비교합니다.
- 같은 버전의 Tauri 업데이터 `.sig`, `latest.json`, CycloneDX SBOM과 릴리스 노트도 릴리스에 있는지 확인합니다.

> [!WARNING]
> v0.1.0 설치기와 앱은 Windows Authenticode로 서명되지 않았습니다. Windows에 **알 수 없는 게시자**, **Windows의 PC 보호**가 표시되거나 Smart App Control·조직 정책이 실행을 막을 수 있습니다. SmartScreen, Microsoft Defender, Smart App Control이나 다른 보안 제품을 끄지 마세요. 공식 출처·정확한 파일명·SHA-256을 모두 확인하고 얼리액세스 위험을 받아들일 수 있는 개인 PC에서만 설치 여부를 판단하세요.

## v0.1.0에서 할 수 있는 일

v0.1.0에 포함된 모든 기능은 이번 얼리액세스에서 결제 없이 사용할 수 있습니다.

1. whisper.cpp 기반 로컬 음성 전사, 자동 언어 감지와 영어 방향 번역
2. SRT·VTT 가져오기, 자막 문구·시간 편집, 분할·병합·삽입·삭제·검색·실행 취소·다시 실행
3. SRT·VTT·ASS·TXT 내보내기, 자막 스타일과 카라오케 하이라이트
4. 영상 위 자막 미리보기와 FFmpeg 기반 H.264 영상 번인
5. llama.cpp와 로컬 모델을 선택 설치해 사용하는 고품질 로컬 번역
6. 필요한 엔진·모델만 선택해 설치하고, SHA-256 검증·이어받기·용량 확인·개별 삭제

이는 향후 1.0 출시, 가격, 결제 방식, 지원 기간, 업데이트 일정이나 특정 기능의 계속 제공을 약속하는 문구가 아닙니다.

## 개인정보와 네트워크 사용

- 미디어·자막·프롬프트·전사·번역·생성 결과는 사용자 PC에서 처리되며 PCSSAK 서버로 업로드되지 않습니다.
- PCSSAK 계정, 광고, 텔레메트리, 사용량 분석과 자동 오류 업로드가 없습니다.
- 중단된 편집을 복원하기 위해 로컬 복구 세션을 저장합니다.
- 고정 업데이트 확인·사용자 승인 업데이트, 사용자가 엔진·모델 설치를 선택하거나 Windows
  설치 중 WebView2가 필요할 때 네트워크를 사용합니다. 구성요소는 고정된 GitHub·Hugging
  Face 상위 배포처에서 내려받고 고정 SHA-256으로 확인합니다.
- v0.1.0 설치기에는 FFmpeg가 포함되지 않으며 PCSSAK이 FFmpeg를 미러링하지 않습니다. 사용자가 구성요소 설치를 선택하면 고정된 GPL 빌드를 BtbN GitHub 릴리스에서 직접 내려받습니다. 자세한 내용은 [제3자 고지](THIRD-PARTY-NOTICES.md)를 확인하세요.

다운로드를 요청하면 GitHub, Hugging Face 또는 Microsoft가 IP 주소와 요청 헤더 같은 일반적인 HTTPS 연결 정보를 처리할 수 있습니다. Jamak은 사용자의 미디어 파일을 이 서비스들로 보내지 않습니다.

## 얼리액세스 지원 경계

- 베타 지원: Windows 10 버전 22H2 x64와 지원 중인 Windows 11 x64, Home·Pro
- 권장 환경: 현재 지원 중이며 최신 보안 업데이트가 적용된 Windows 11 x64
- 미지원: 32비트 Windows, Windows on ARM, Windows S 모드, Windows Server, macOS, Linux, Wine, 수정·재패키징 구성요소
- Microsoft Edge WebView2 Runtime이 필요합니다.
- AI 전사·번역에는 누락·환각·오역이 있을 수 있으므로 중요한 자막은 사람이 검수해야 합니다.
- 설치·사용 전 원본 미디어와 중요한 자막 파일을 별도로 백업하세요.
- 앱은 현재 버전을 표시하고 PCSSAK 고정 HTTPS 엔드포인트에서 검증된 새 버전을 확인합니다. 업데이트가 있을 때 사용자가 버튼을 눌러 내려받기·설치를 승인하며, 공개 승인된 업데이트가 없으면 엔드포인트는 아무 업데이트도 제안하지 않습니다.
- Windows Authenticode 미서명 상태와 별개로, 앱 내 업데이트 설치기는 앱에 포함된 Tauri 공개키와 필수 `.sig`로 검증합니다. 이 서명이 없거나 맞지 않으면 업데이트를 적용하지 않습니다.
- 최초 v0.1.0 설치기를 공개해도 v0.1.0에 같은 버전을 제안하지 않습니다. 업데이트
  엔드포인트는 `204 No Content`를 유지하며 검증된 v0.1.1 이상부터 새 업데이트로 제공할 수
  있습니다.

[설치 안내](docs/INSTALLATION.ko.md), [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)와
[시스템 요구사항](SYSTEM_REQUIREMENTS.md)에서 설치·저장 공간·메모리·GPU·런타임을 확인하세요.

## 얼리액세스 개선에 참여하기

- 안전하게 재현한 오류는 [버그 제보 양식](../../issues/new?template=bug-report.yml)을 사용하세요.
- 반복되는 사용자 문제와 원하는 결과는 [기능 제안 양식](../../issues/new?template=feature-request.yml)에 적어주세요.
- 화면이나 기술 정보를 첨부하기 전에 [지원 안내](SUPPORT.md)를 확인하세요.
- 악용 가능한 보안 내용은 [보안 정책](SECURITY.md)에 따라 비공개로 알려주세요.

원본 미디어, 비공개 자막, 개인 경로, 고객 자료, 자격증명, 라이선스 키나 회사 비밀은 올리지 마세요. AI의 도움으로 작성한 제보도 제출자가 직접 재현하고 확인해야 합니다.

## 문서

- [English introduction](README.md)
- [지원 안내](SUPPORT.md)
- [보안 정책](SECURITY.md)
- [시스템 요구사항](SYSTEM_REQUIREMENTS.md)
- [설치 및 업데이트](docs/INSTALLATION.ko.md)
- [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md)
- [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)
- [제3자 고지](THIRD-PARTY-NOTICES.md)
- [이슈·기여 원칙](CONTRIBUTING.md)

PCssak Jamak 바이너리는 승인된 릴리스에 동봉되는 Jamak EULA에 따라 배포합니다. `PCSSAK`은
게시자와 소프트웨어 브랜드 표시명이며, 이 문구만으로 특정 등록 법인 형태를 주장하지
않습니다. 제3자 구성요소는 각자의 라이선스를 따르며 PCSSAK은 문서에 언급된 상위 프로젝트나
서비스 제공자와 제휴하거나 보증을 받은 관계가 아닙니다.
