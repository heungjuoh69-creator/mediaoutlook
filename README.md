# MEDIA OUTLOOK — mediaoutlook.co.kr 올리기

## 1. 깃허브에 올리기
1. github.com → + → New repository → 이름 `mediaoutlook` → Public → Create repository
2. Add file → Upload files → 이 폴더의 `index.html`, `CNAME` 두 파일을 끌어다 놓기 → Commit changes
3. Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save

## 2. 가비아 DNS 설정 (네임서버는 가비아 기본값 그대로)
My가비아 → 서비스 관리 → 도메인 → mediaoutlook.co.kr → DNS 관리 → 레코드 추가

| 타입 | 호스트 | 값 |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | 내깃허브아이디.github.io. |

## 3. 연결 확인
- 깃허브 Settings → Pages → Custom domain 에 `mediaoutlook.co.kr` 이 들어가 있는지 확인 (CNAME 파일이 자동으로 넣어줌)
- 몇 분~하루 뒤 초록색 체크가 뜨면 **Enforce HTTPS** 체크

## 4. 애드센스 준비
- 애드센스에서 사이트 추가 → `mediaoutlook.co.kr`
- 애드센스가 알려주는 한 줄을 `ads.txt` 파일로 만들어 저장소 맨 위에 올리기
  예: `google.com, pub-0000000000000000, DIRECT, f08c47fec0942fa0`
- index.html의 CONFIG.adsenseClient 에 `ca-pub-...` 번호 입력

## 5. 매일 뉴스 업데이트
- 지금은 매일 새벽 2시에 새 `index.html`이 메일·앱으로 옵니다 → 깃허브에서 Add file → Upload files 로 덮어쓰기
- 깃허브를 Claude와 연결하면 이 과정도 자동화할 수 있습니다
