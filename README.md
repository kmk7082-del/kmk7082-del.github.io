# 한 칸의 여유 무료 공식 홈페이지 배포 안내

## 공개 홈페이지 현황
- GitHub Pages 배포 설정 완료 (`main / (root)`).
- 개인정보처리방침에 개발자명 **NOVAPIXEL**, 공개 문의 이메일 **kmk7082@gmail.com**, 시행일 **2026-10-26** 반영.
- 정책의 제3자 광고 정보 처리·국외 이전·보관 관련 문구도 실제 SDK와 Google Play 데이터 보안 양식에 맞게 최종 검토하세요.
- `app-ads.txt`는 제공된 AdMob 게시자 식별자를 이용해 준비했습니다. 반드시 AdMob 콘솔 > 앱 > app-ads.txt 안내의 **개인화된 코드를 확인**해 동일한지 비교하세요.

## Github Pages로 무료 사이트 만들기
1. `https://github.com/new`에서 **공개(Public)** 저장소를 만드세요.
2. 이름을 GitHub 사용자명과 정확히 맞춰 `kmk7082-del.github.io` 로 지정합니다. 기존 비공개 `quiet-sudoku` 저장소를 공개로 바꾸면 안 됩니다.
3. `index.html`, `privacy.html`, `app-ads.txt`, `.nojekyll`을 저장소 **최상위 경로**에 각각 업로드합니다. ZIP 파일 자체를 업로드하는 것은 안 됩니다.
4. 저장소의 **Settings > Pages**에서 **Deploy from a branch**, Branch **main**, Folder **/(root)**, Save를 선택합니다.
5. 게시되면 다음 URL에 접근해서 확인합니다.
   - 홈페이지: `https://kmk7082-del.github.io/`
   - 개인정보처리방침: `https://kmk7082-del.github.io/privacy.html`
   - 광고 판매자 선언: `https://kmk7082-del.github.io/app-ads.txt`
6. 개인정보방침의 개발자명·연락처·시행일을 반영했습니다. 스토어 제출 전 실제 SDK 데이터 처리와 일치하는지 검토합니다. 파일은 GitHub에 등록되어 있으며 Pages에서 main / (root)로 배포 설정했습니다.

## Google Play 및 AdMob 연결
- Play Console 앱 상세 스토어 설정에서 개발자 웹사이트로 `https://kmk7082-del.github.io/` 을 설정합니다.
- 앱 콘텐츠의 개인정보처리방침 주소로 `https://kmk7082-del.github.io/privacy.html`를 설정합니다.
- 동일한 방침 URL을 GitHub Actions Secrets의 `PRIVACY_POLICY_URL`로 설정하면 앱 안 개인정보 버튼에 반영됩니다.
- AdMob 앱을 Play 스토어 앱과 연결하고, app-ads.txt 인증 상태 및 크롤링 주소를 확인합니다.
- Google 공식 지침에 따르면 앱은 스토어에 게시되어야 AdMob이 스토어 정보를 이용해 app-ads.txt를 정상 크롤링할 수 있습니다.

## 중요한 제약
- GitHub Pages의 `github.io` 도메인은 **AdMob이 자동으로 인증해준다는 보장이 없습니다**. 만약 앱 공개 후에도 인증에 실패한다면, AdMob에서 공식적으로 안내하는 Firebase Hosting이나 본인 소유 도메인으로 이전하는 방법을 고려합니다.
- GitHub Pages는 일반적인 설명·정책 게시용 정적 사이트로 활용하며, 기존 게임 소스나 민감한 설정·서명키 등을 공개 저장소에 넣지 마세요.