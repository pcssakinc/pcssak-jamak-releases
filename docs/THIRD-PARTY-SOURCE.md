# FFmpeg 원본 소스와 배포 경계 / FFmpeg Source and Distribution Boundary

PCssak Jamak v0.1.1은 FFmpeg를 설치기나 Jamak GitHub 릴리스 자산에 포함하지 않습니다. 사용자가 Jamak 설정에서 FFmpeg 설치를 선택할 때 다음 상위 자산을 BtbN GitHub에서 직접 내려받습니다.

- 상위 프로젝트: [BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds)
- 고정 릴리스: [`autobuild-2026-07-31-14-10`](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-07-31-14-10)
- 고정 Windows x64 자산: `ffmpeg-N-125875-g5d4d3bdc61-win64-gpl.zip`
- 적용 조건: 해당 GPL 빌드의 GPL-3.0-or-later 및 포함된 각 코덱·라이브러리 조건
- FFmpeg 공식 라이선스·법률 안내: [ffmpeg.org/legal.html](https://ffmpeg.org/legal.html)
- FFmpeg 공식 원본 소스: [ffmpeg.org/download.html](https://ffmpeg.org/download.html)

Jamak은 내려받은 압축 파일의 고정 SHA-256이 앱에 기록된 값과 일치할 때만 압축을 해제합니다. 필요한 실행 파일 이름을 허용 목록으로 제한하며 관리 데이터 폴더의 절대 경로에서 호출합니다. 이 검증은 공급망 위험을 줄이지만 BtbN·GitHub·FFmpeg 자체를 PCSSAK이 보증한다는 뜻은 아닙니다.

PCSSAK이 향후 이 바이너리를 동봉·미러링·재배포한다면 그 시점의 정확한 바이너리에 대응하는 원본 소스, 빌드 스크립트·설정, 라이선스 전문, 저작권·귀속, 설치·배포 방식과 특허 고려사항을 별도로 검토하고 충족해야 합니다. v0.1.1의 상위 직접 다운로드 구조를 다른 배포 방식에 그대로 적용할 수 없습니다.

H.264/AVC 출력 관련 특허 조건은 GPL과 별개입니다. 배포 지역·사용 방식·상업성에 따라 별도 검토가 필요할 수 있습니다.

---

PCssak Jamak v0.1.1 does not include FFmpeg in the installer or upload it as a Jamak GitHub release asset. When the user chooses to install FFmpeg in Jamak settings, Jamak downloads the exact BtbN asset identified above directly from the upstream GitHub release and verifies the pinned SHA-256 before extraction.

Jamak limits extracted executables to an allowlist and invokes managed components by absolute path. These controls reduce risk but do not constitute a PCSSAK warranty of BtbN, GitHub, FFmpeg, or every included codec.

Any future PCSSAK bundling, mirroring, or redistribution requires a new review of the exact corresponding source, build scripts and configuration, full license and attribution texts, delivery method, and patent considerations. H.264/AVC patent conditions are separate from GPL compliance and may depend on region and use.
