# M916 Pro / G49 웹허브 — 한국어 안내

Redragon G49 기본형과 M916 Pro 1K/4K용 오픈소스 WebHID 설정 페이지입니다. 원본 프로젝트: [dongkid/g49-web-control](https://github.com/dongkid/g49-web-control).

이 포크는 원본의 **영어/중국어**에 **한국어**를 추가합니다. 브라우저 언어가 한국어라면 최초 접속 시 한국어가 자동으로 선택되고, 상단 언어 메뉴에서 변경하면 선택이 브라우저에 저장됩니다.

## 주요 기능
- DPI와 폴링레이트 변경, 버튼 할당 및 온보드 프로필 관리
- 센서 설정과 배터리 상태 확인
- 매크로, 단축키, 수신기 페어링 및 펌웨어 관련 기능
- 설정을 장치 플래시 메모리에 저장하거나 JSON으로 내보내기

**주의:** 실제로 지원되는 하드웨어와 기능은 모델·펌웨어에 따라 다릅니다. G49 Pro에서 웹허브 연결, DPI 변경 및 배터리 표시가 작동한 사례는 있지만, 이 사실만으로 G49 Pro의 모든 기능이나 펌웨어 업데이트가 검증된 것은 아닙니다.

## Cloudflare Pages 배포

빌드 도구가 없는 정적 HTML/JS/CSS 프로젝트이므로 별도 프레임워크가 필요하지 않습니다.

1. [Cloudflare 대시보드](https://dash.cloudflare.com/) → **Workers & Pages** → **Create application** → **Pages** → **Import an existing Git repository**.
2. 자신의 GitHub 포크인 `pingpingjinping/g49-web-control`을 연결합니다.
3. **Production branch:** `main` (한국어 변경 PR을 먼저 병합).
4. **Framework preset:** `None`, **Build command:** `exit 0` (또는 공란), **Build output directory:** `.` (저장소 최상위).
5. 배포 후 생성된 `*.pages.dev`의 HTTPS 주소에서 Chrome 또는 Edge로 접속합니다. 최초 연결 시 브라우저의 USB/HID 접근 권한을 허용해야 합니다.

이 프로젝트는 외부 서버로 장치 설정을 보내는 별도 백엔드 없이 브라우저의 WebHID를 사용합니다. **펌웨어 업데이트는 해당 모델의 정확한 정품 파일 및 유선 연결을 확인하기 전에는 실행하지 마세요.**

## 라이선스

원본 저작권과 MIT 라이선스는 [LICENSE](LICENSE)에 따라 유지됩니다. 이 포크의 한국어 번역만 추가했습니다.
