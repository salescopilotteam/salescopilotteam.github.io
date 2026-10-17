# salescopilotteam.github.io

세일즈 코파일럿 팀의 공개 사이트입니다. CardKeep, 보증서 코파일럿, 하루조각의 지원·법률 문서를
한국어, 영어, 일본어로 제공합니다.

```
/                 제품 소개
/cards/           CardKeep (com.salescopilot.cards)
/warranty/        보증서 코파일럿 (com.salescopilot.warranty)
/diary/           하루조각 / Four Pieces (com.salescopilot.harujogak)
```

- 개인정보처리방침: [cards/privacy-ko.html](cards/privacy-ko.html) · [English](cards/privacy-en.html) · [日本語](cards/privacy-ja.html)
- 이용약관: [cards/terms-ko.html](cards/terms-ko.html) · [English](cards/terms-en.html) · [日本語](cards/terms-ja.html)
- 도움말: [cards/help-ko.html](cards/help-ko.html) · [English](cards/help-en.html) · [日本語](cards/help-ja.html)

보증서 코파일럿 문서는 `warranty/` 아래, 하루조각 개인정보처리방침은 `diary/` 아래에 둡니다.

운영자: 세일즈 코파일럿 팀 · salescopilot.team@gmail.com

## 앱에서 생성하는 문서

CardKeep과 보증서 코파일럿의 법률 문서는 각각 앱 소스의 `documents.ts`에서 생성합니다. 앱 안에서
보이는 문서와 웹에 공개된 문서가 어긋나면 스토어 심사와 이용자 안내 양쪽에서 문제가 되므로, 원본을 하나로 둡니다.

문구를 고칠 때는 앱 저장소에서 `documents.ts`를 고치고 아래를 실행한 뒤, 생성된 결과를 이 저장소에
커밋합니다.

```
cd expo
node --experimental-strip-types scripts/generate-legal-site.mjs <이 저장소 경로>/cards
```

보증서 코파일럿도 같은 명령으로 출력 대상만 `warranty`로 바꿉니다. 하루조각은 앱 저장소의
`docs-site/` 정적 문서를 `diary/`에 동기화합니다. 루트의 `index.html`은 제품 소개 페이지이며 직접 작성합니다.

## 번역본의 효력

영어와 일본어 문서는 이해를 돕기 위한 번역입니다. 정식 문서는 한국어판이며, 내용이 다를 경우
한국어판이 우선합니다. 각 번역본 머리에도 같은 안내가 있습니다.
