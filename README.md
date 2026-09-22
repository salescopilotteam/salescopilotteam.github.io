# salescopilotteam.github.io

세일즈 코파일럿 시리즈의 공개 사이트입니다. 각 앱의 개인정보처리방침, 이용약관, 도움말을 한국어,
영어, 일본어로 제공합니다.

```
/                 시리즈 소개
/cards/           CardKeep (com.salescopilot.cards)
```

- 개인정보처리방침: [cards/privacy-ko.html](cards/privacy-ko.html) · [English](cards/privacy-en.html) · [日本語](cards/privacy-ja.html)
- 이용약관: [cards/terms-ko.html](cards/terms-ko.html) · [English](cards/terms-en.html) · [日本語](cards/terms-ja.html)
- 도움말: [cards/help-ko.html](cards/help-ko.html) · [English](cards/help-en.html) · [日本語](cards/help-ja.html)

운영자: 세일즈 코파일럿 팀 · salescopilot.team@gmail.com

## `cards/` 아래 파일은 직접 고치지 않습니다

모든 HTML은 앱 소스의 `expo/src/legal/documents.ts` 하나에서 생성됩니다. 앱 안에서 보이는 문서와
웹에 공개된 문서가 어긋나면 스토어 심사와 이용자 안내 양쪽에서 문제가 되므로, 원본을 하나로 둡니다.

문구를 고칠 때는 앱 저장소에서 `documents.ts`를 고치고 아래를 실행한 뒤, 생성된 결과를 이 저장소에
커밋합니다.

```
cd expo
node --experimental-strip-types scripts/generate-legal-site.mjs <이 저장소 경로>/cards
```

루트의 `index.html`은 시리즈 소개 페이지이며 직접 작성합니다. 앱이 늘어나면 폴더를 하나 더 만들고
여기에 항목을 추가합니다.

## 번역본의 효력

영어와 일본어 문서는 이해를 돕기 위한 번역입니다. 정식 문서는 한국어판이며, 내용이 다를 경우
한국어판이 우선합니다. 각 번역본 머리에도 같은 안내가 있습니다.
