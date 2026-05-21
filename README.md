# Strategy — Team Align Package

팀 align용 전략 패키지. **사업 전략 deck + 인터랙티브 prototype**이 한 폴더에 들어있습니다.

## 무엇이 들어있나

| 파일 | 용도 |
|------|------|
| `index.html` | 시작 페이지 (3개 prototype 진입점 + deck 다운로드) |
| `screens/screen-1-free.html` | 무료 진단 — freemium gate, blur 처리 |
| `screens/screen-2-connected.html` | 전체 진단 — 계정 연결 후 풀 뷰 |
| `screens/screen-3-quote.html` | 견적 만들기 — 인터랙티브 토글 |
| `Strategy_Deck.pdf` | 16장 사업 전략 deck (발표용) |
| `Strategy_Deck.pptx` | 위 deck의 PowerPoint 원본 (수정·코멘트 가능) |

## 팀에 공유하는 가장 빠른 방법 (GitHub Pages)

```bash
# 1. 이 폴더를 GitHub repo로
git init
git add .
git commit -m "Initial strategy package"
git branch -M main
git remote add origin git@github.com:<your-org>/<repo>.git
git push -u origin main

# 2. GitHub repo settings → Pages → Source를 'GitHub Actions'로 설정
#    (이 폴더에 이미 .github/workflows/pages.yml 워크플로가 들어있음)

# 3. push 직후 1-2분 뒤 다음 URL이 활성화됨
#    https://<your-org>.github.io/<repo>/
```

팀에는 그 URL 하나만 전달하면 됩니다 — `index.html` 랜딩에서 deck PDF/PPTX 다운로드 + prototype 3개 진입까지 모두 가능합니다.

## 로컬에서 미리 보기

```bash
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 열기
```

## 팀과 같이 볼 때 추천 흐름

1. **Strategy Deck PDF 슬라이드 1–10** 발표 → 전략 framing
2. **Prototype 1 → 2 → 3** 직접 만지며 시연 → "추상이 화면이 되면 이런 모습"
3. **Strategy Deck 슬라이드 11–15** → 제품 구조, 가격, wedge, moat, 90일 plan
4. **Strategy Deck 슬라이드 16 (Q1–Q5)** → 결정 필요 사항 토론

## 주의사항

- 모든 데이터는 **placeholder**입니다 (실제 광고주·실제 숫자 아님)
- Brand A는 한국 → 미국 K-Beauty 셀러의 전형적 패턴을 익명화한 가상 케이스
- 화면 디자인은 데모용이며 실제 제품 UI 결정 아님
- 모바일 대응은 부분적임 (데스크탑 시연 권장)

## 디렉토리 구조

```
.
├── index.html                  # 랜딩 페이지
├── styles.css                  # 공통 디자인 토큰·스타일
├── screens/
│   ├── screen-1-free.html
│   ├── screen-2-connected.html
│   └── screen-3-quote.html
├── vendor/
│   └── tabler/                 # 아이콘 폰트 (오프라인 작동)
├── Strategy_Deck.pdf
├── Strategy_Deck.pptx
└── .github/workflows/pages.yml # GitHub Pages 자동 배포
```
