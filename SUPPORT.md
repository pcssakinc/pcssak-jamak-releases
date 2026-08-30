# Support / 고객지원

PCssak Jamak Free Early Access is maintained by a solo developer. Reports are prioritized by security impact, risk of media or subtitle loss, number of affected users, and reproducibility rather than arrival order. Early Access does not include a guaranteed response time, fix deadline, update schedule, or long-term support term.

## Before reporting

1. Confirm the Jamak version, exact installer filename, and install source.
2. Read the [installation guide](docs/INSTALLATION.md),
   [latest release notes](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest),
   and [known limitations](docs/KNOWN-LIMITATIONS.md).
3. Record the Windows edition, OS build shown by `winver`, x64 architecture, installer language,
   and app language.
4. Record the CPU, memory, GPU model and driver, and the installed CPU or CUDA engine/model path without personal folder names.
5. Reproduce with the smallest synthetic media or subtitle example that does not contain personal, customer, licensed, or confidential material.
6. Note whether the problem occurred during installation, component download, import, transcription, timeline editing, translation, styling, export, video burn-in, recovery, update, or startup.
7. Remove full paths, account names, original filenames, media content, subtitle text, tokens, credentials, and license keys from screenshots and logs.

Use the GitHub [bug report form](../../issues/new?template=bug-report.yml) for a safely reproduced defect. Use the [feature request form](../../issues/new?template=feature-request.yml) for a recurring user problem and desired outcome. General inquiries can be sent to `support@pcssak.com`.

Do not attach the original affected video, audio, subtitle, project folder, or full recovery session. A short synthetic sample is safer and usually more useful. Exploitable security issues must follow [SECURITY.md](SECURITY.md) and must not be posted publicly.

## Common installation and component issues

- **Unknown publisher or SmartScreen:** v0.1.1 is unsigned. Confirm the official source,
  `PCssak-Jamak-Beta-Windows-x64-Setup.exe` filename, and SHA-256. Do not disable Windows security
  features or add a broad exclusion.
- **WebView2 error or blank window:** apply Windows updates and install Microsoft's official [WebView2 Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/).
- **Visual C++ runtime error:** install Microsoft's official [Visual C++ 2015-2022 Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe). Do not download individual DLLs from an unofficial site.
- **Engine or model download failure:** confirm free storage, upstream GitHub or Hugging Face access, and that no other Jamak transcription, translation, burn-in, install, or removal operation is running. Repeated SHA-256 mismatch must be reported; do not bypass verification.
- **Incorrect transcription or translation:** AI output requires human review. Include the language, model, CPU/CUDA path, and non-sensitive media characteristics, not the original content.
- **Unexpected output change:** stop further processing, preserve the original backup, and report the smallest safe evidence. Do not repeatedly retry a step that could overwrite or lose output.

## Support boundary

- Windows 10 version 22H2 x64 and supported Windows 11 x64 Home/Pro are the v0.1.1 beta scope.
- Windows 11 x64 with current security updates is recommended.
- 32-bit Windows, ARM64, Windows S mode, Windows Server, macOS, Linux, Wine, unofficial repackaging, and user-modified engines or models are unsupported.
- v0.1.1 does not install updates silently. It shows the current version, checks the fixed PCSSAK
  HTTPS endpoint, and lets the user start a verified update when one is approved. If the check
  fails, use the exact official GitHub release page without bypassing verification. After the
  published assets, anonymous downloads, hashes, and Tauri signature pass independent checks, an
  owner-authorized controlled live trial may temporarily offer v0.1.1 to an installed v0.1.0 app.
  The result remains `NOT_RUN` until the full update succeeds; a failure returns the endpoint to
  `204 No Content` immediately.
- All v0.1.1 features are free during this Early Access release. No future price, payment method, feature set, update, or 1.0 release is promised.

## 한국어

PCssak Jamak 무료 얼리액세스는 1인 개발자가 운영합니다. 문의는 도착 순서만이 아니라 보안 영향, 미디어·자막 손실 위험, 영향받는 사용자 수와 재현 가능성을 기준으로 우선순위를 정합니다. 얼리액세스에는 응답 시간, 수정 기한, 업데이트 일정이나 장기 지원 기간 보장이 없습니다.

제보 전에 다음을 확인하세요.

1. Jamak 버전, 정확한 설치기 파일명과 설치 출처를 확인합니다.
2. [설치 안내](docs/INSTALLATION.ko.md),
   [최신 릴리스 노트](https://github.com/pcssakinc/pcssak-jamak-releases/releases/latest)와
   [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)를 확인합니다.
3. Windows 에디션, `winver`의 OS 빌드, x64 아키텍처, 설치기 언어와 앱 언어를 기록합니다.
4. CPU·메모리·GPU 모델과 드라이버, 설치한 CPU·CUDA 엔진/모델 경로를 기록하되 개인 폴더 이름은 지웁니다.
5. 개인정보·고객 자료·라이선스 자료·회사 비밀이 없는 가장 작은 합성 미디어나 자막으로 재현합니다.
6. 설치·구성요소 다운로드·가져오기·전사·타임라인 편집·번역·스타일·내보내기·영상 번인·복원·업데이트·시작 중 어느 단계에서 생겼는지 적습니다.
7. 화면과 로그에서 전체 경로, 계정 이름, 실제 파일명, 미디어 내용, 자막 문구, 토큰, 자격증명과 라이선스 키를 제거합니다.

안전하게 재현한 오류는 GitHub [버그 제보 양식](../../issues/new?template=bug-report.yml), 반복되는 사용자 문제와 원하는 결과는 [기능 제안 양식](../../issues/new?template=feature-request.yml)을 사용하세요. 일반 문의는 `support@pcssak.com`으로 보낼 수 있습니다.

실제 문제 영상·음성·자막·프로젝트 폴더나 전체 복구 세션은 첨부하지 마세요. 짧은 합성 자료가 더 안전하고 대체로 더 유용합니다. 악용 가능한 보안 내용은 공개하지 말고 [보안 정책](SECURITY.md)을 따라주세요.

자주 확인할 항목은 다음과 같습니다.

- **알 수 없는 게시자·SmartScreen:** v0.1.1은 미서명입니다. 공식 출처,
  `PCssak-Jamak-Beta-Windows-x64-Setup.exe` 파일명과 SHA-256을 확인하고 Windows 보안 기능을
  끄거나 넓은 예외를 추가하지 마세요.
- **WebView2 오류·빈 화면:** Windows 업데이트를 적용하고 Microsoft 공식 [WebView2 Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/)을 설치합니다.
- **Visual C++ 런타임 오류:** Microsoft 공식 [Visual C++ 2015-2022 Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)를 설치합니다. 비공식 사이트에서 개별 DLL을 받지 마세요.
- **엔진·모델 다운로드 실패:** 저장 공간과 GitHub·Hugging Face 접속, 다른 Jamak 전사·번역·번인·설치·삭제 작업이 실행 중인지 확인합니다. SHA-256 불일치가 반복되면 검증을 우회하지 말고 제보하세요.
- **전사·번역 결과 문제:** AI 결과는 사람이 검수해야 합니다. 원본 내용 대신 언어·모델·CPU/CUDA 경로와 민감하지 않은 미디어 기술 정보를 적어주세요.
- **예상하지 않은 출력 변경:** 추가 처리를 중지하고 원본 백업을 보존한 뒤 가장 작은 안전한 증거로 제보하세요. 덮어쓰기·손실 가능성이 있는 단계는 반복하지 마세요.

v0.1.1 베타 지원 범위는 Windows 10 버전 22H2 x64와 지원 중인 Windows 11 x64 Home·Pro이며, 최신 보안 업데이트가 적용된 Windows 11 x64를 권장합니다. 32비트 Windows, ARM64, Windows S 모드, Windows Server, macOS, Linux, Wine, 비공식 재패키징과 사용자가 수정한 엔진·모델은 지원하지 않습니다.

v0.1.1은 업데이트를 조용히 자동 설치하지 않습니다. 현재 버전을 표시하고 PCSSAK 고정 HTTPS
엔드포인트를 확인하며 승인된 새 버전이 있을 때 사용자가 검증된 업데이트를 직접 시작합니다.
확인이 실패하면 검증을 우회하지 말고 정확한 공식 GitHub 릴리스 페이지를 확인하세요. v0.1.1
공개 자산·익명 다운로드·해시·Tauri 서명을 독립 검증한 뒤에는 출시 소유자가 승인한 제한
실운영 시험에서 설치된 v0.1.0 앱에 v0.1.1을 제공할 수 있습니다. 전체 업데이트가 성공하기
전까지 결과는 `NOT_RUN`이며, 실패하면 엔드포인트를 즉시 `204 No Content`로 되돌립니다.
v0.1.1의 모든 기능은 이번 얼리액세스에서 무료지만 향후 가격·결제 방식·기능 구성·업데이트나
1.0 출시는 약속하지 않습니다.
