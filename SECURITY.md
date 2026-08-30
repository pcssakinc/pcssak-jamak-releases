# Security Policy / 보안 정책

## Supported releases

Security fixes are evaluated for the **latest approved public PCssak Jamak Free Early Access release**. Older 0.1.x builds may not receive a separate fix. If no approved release is visible, no public Jamak build is supported from this repository.

Free Early Access can contain undiscovered defects. This policy provides a reporting route; it is not a warranty that Jamak is free of vulnerabilities or that a fix will be provided by a particular date.

## Report a vulnerability privately

Do not post exploitable details in a public issue. Email `support@pcssak.com` with `[Jamak security report]` in the subject when a problem could enable or contribute to:

- substituting an untrusted installer, engine, model, or update; bypassing pinned SHA-256 verification; or executing a file outside the managed component directory;
- reading or writing a media, subtitle, recovery, export, or unrelated file outside the user-approved scope;
- command injection through media paths, subtitle text, codec metadata, prompts, archive names, or external tool arguments;
- unsafe archive extraction, path traversal, DLL or executable substitution, or execution through the current directory or ordinary `PATH`;
- escaping the intended `127.0.0.1` local-model server boundary or exposing prompts, subtitles, or model traffic to another interface;
- code execution, privilege escalation, secret exposure, unauthorized network transfer, or a persistent denial of service.

Include, when safely possible:

- the Jamak version, exact installer filename, SHA-256, and official install source;
- Windows edition, OS build, x64 architecture, security product, CPU/GPU, and driver version;
- the affected workflow and security impact;
- minimal reproduction steps using synthetic media and subtitles;
- whether details or proof of concept are already public;
- a safe contact method and any reasonable disclosure constraints.

Do not send passwords, private keys, tokens, payment information, personal identifiers, license keys, customer media, private subtitles, confidential prompts, production credentials, malicious executables, or a full archive of the affected project. Describe sensitive evidence first and agree on a safer transfer method before sending it. Ordinary email is not an encrypted security portal.

PCSSAK will triage reports by user impact, data-loss risk, exploitability, and reproducibility; investigate within solo-maintainer capacity; and prepare a fix and regression check where practical. This is not a guaranteed response-time, fix-deadline, bug-bounty, CVE-assignment, or payment program.

## Authenticity and current security boundary

- Download only from this official `pcssakinc` repository or the PCSSAK product page linked by the same approved release.
- Compare the installer with `SHA256SUMS.txt` from that exact release.
- v0.1.1 is not Authenticode-signed. SHA-256 proves byte equality with the published file, not publisher identity or absence of malware.
- Do not disable SmartScreen, Microsoft Defender, Smart App Control, or another security product.
- User media and subtitles are processed locally; Jamak has no telemetry or analytics upload.
- User-initiated engine and model downloads use fixed upstream URLs and pinned SHA-256 values.
- FFmpeg is downloaded directly from the pinned BtbN upstream release and is not included in or mirrored with the Jamak installer for v0.1.1.
- The local LLM server is intended to bind only to `127.0.0.1` and is cleaned up with the application process.
- v0.1.1 does not install updates silently. It checks the fixed PCSSAK HTTPS endpoint and applies an update only after the user starts it and the mandatory Tauri signature validates against the public key embedded in the app. This updater signature is separate from the current Authenticode-unsigned status.

These controls reduce risk but do not guarantee safety. Unsigned software, downloaded external executables, large AI models, loopback services, media decoders, codec libraries, and GPU runtimes can still have supply-chain, compatibility, or antivirus-detection risks.

## 한국어

보안 수정은 **최신 승인 공개 PCssak Jamak 무료 얼리액세스 버전**을 기준으로 검토합니다. 이전 0.1.x 빌드에는 별도 수정이 제공되지 않을 수 있습니다. 승인된 릴리스가 보이지 않는다면 이 저장소에서 지원하는 공개 Jamak 빌드도 없습니다.

무료 얼리액세스에는 발견되지 않은 오류가 남아 있을 수 있습니다. 이 정책은 안전한 제보 경로를 설명하며, 보안 결함이 없거나 특정 날짜까지 수정된다는 보증이 아닙니다.

다음 문제는 공개 Issue에 악용 가능한 세부 내용을 올리지 말고 이메일 제목에 `[Jamak 보안 제보]`를 붙여 `support@pcssak.com`으로 보내주세요.

- 신뢰하지 않은 설치기·엔진·모델·업데이트 바꿔치기, 고정 SHA-256 검증 우회 또는 관리 구성요소 폴더 밖 파일 실행
- 사용자 승인 범위 밖의 미디어·자막·복구·내보내기 파일이나 관계없는 파일 읽기·쓰기
- 미디어 경로, 자막 문구, 코덱 메타데이터, 프롬프트, 압축 파일명이나 외부 도구 인자를 통한 명령 삽입
- 안전하지 않은 압축 해제, 경로 이탈, DLL·실행 파일 바꿔치기 또는 현재 폴더·일반 `PATH`를 통한 실행
- `127.0.0.1` 로컬 모델 서버 경계 이탈 또는 다른 인터페이스로 프롬프트·자막·모델 통신 노출
- 코드 실행, 권한 상승, 비밀정보 노출, 승인되지 않은 네트워크 전송 또는 지속적인 서비스 거부

가능하면 Jamak 버전, 정확한 설치기 파일명·SHA-256·공식 설치 출처, Windows 에디션·OS 빌드·x64 여부·보안 제품·CPU/GPU·드라이버, 영향받은 작업과 보안 영향, 합성 미디어·자막을 사용한 최소 재현 절차, 이미 공개됐는지 여부와 안전한 연락 방법을 포함하세요.

비밀번호, 개인키, 토큰, 결제 정보, 개인 식별정보, 라이선스 키, 고객 미디어, 비공개 자막, 회사 프롬프트, 운영 자격증명, 악성 실행 파일이나 실제 프로젝트 전체 압축본은 보내지 마세요. 민감한 증거가 필요하면 먼저 설명만 보내고 안전한 전달 방법을 합의하세요. 일반 이메일은 암호화된 전용 보안 포털이 아닙니다.

PCSSAK은 사용자 영향, 데이터 손실 위험, 악용 가능성과 재현 가능성을 기준으로 우선순위를 정하고 1인 운영 범위에서 조사하며 가능한 경우 수정과 회귀 검증을 준비합니다. 응답 시간·수정 기한·버그 바운티·CVE 발급·금전 보상을 보장하는 제도가 아닙니다.

공식 설치 파일은 이 `pcssakinc` 저장소 또는 같은 승인 릴리스가 안내하는 PCSSAK 제품 페이지에서만 받고 같은 릴리스의 `SHA256SUMS.txt`와 비교하세요. v0.1.1은 Authenticode 미서명이며 SHA-256 일치는 공개 파일과 바이트가 같다는 뜻이지 게시자 신원이나 악성 코드 부재를 보증하지 않습니다. SmartScreen·Microsoft Defender·Smart App Control이나 다른 보안 제품을 끄지 마세요.

사용자 미디어와 자막은 로컬에서 처리되고 텔레메트리·분석 업로드가 없습니다. 사용자가 선택한 엔진·모델 다운로드는 고정된 상위 URL과 SHA-256을 사용합니다. FFmpeg는 v0.1.1 설치기에 포함하거나 PCSSAK이 미러링하지 않고 고정 BtbN 상위 릴리스에서 직접 내려받습니다. 로컬 LLM 서버는 `127.0.0.1`에만 바인딩하고 앱 프로세스와 함께 정리하도록 설계했습니다. v0.1.1은 업데이트를 조용히 자동 설치하지 않으며, PCSSAK 고정 HTTPS 엔드포인트에서 승인된 새 버전을 확인한 뒤 사용자가 시작하고 앱에 포함된 Tauri 공개키로 필수 서명을 검증한 경우에만 적용합니다. 이 업데이터 서명은 현재 Authenticode 미서명 상태와 별개입니다.

이 장치들은 위험을 줄이지만 안전을 보장하지 않습니다. 미서명 소프트웨어, 외부 실행 파일 다운로드, 대용량 AI 모델, 루프백 서비스, 미디어 디코더, 코덱 라이브러리와 GPU 런타임에는 공급망·호환성·백신 탐지 위험이 남을 수 있습니다.
