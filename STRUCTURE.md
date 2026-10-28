# STRUCTURE · paranzip-sample

```
paranzip-sample/
├─ index.html              단일 파일 (CSS·JS 인라인)
├─ wrangler.toml           name = paranzip-sample → paranzip-sample.lgt3232.workers.dev
├─ .assetsignore           img/ · 문서 · index_*.html · _deploy 배포 제외
├─ pz-myeongjo.woff2       제목 (나눔명조 400, 사용 글자만)
├─ pz-myeongjo-bold.woff2  작은 제목 (나눔명조 700)
├─ pz-pretendard.woff2     본문 (Pretendard 400–700)
├─ pz-logo.webp            "파란집 + 집" 투명 로고 (헤더)
├─ pz-house.webp           집 아이콘 (푸터) · favicon.png
├─ pz-hero.webp            히어로 선물 상자
├─ pz-gift-*.webp          선물 3장 (twine · ribbon · bulk)
├─ pz-peach / pz-fin-almond .webp   About
├─ pz-fin-*.webp           휘낭시에 5장 (tray · plate · two · choco · glass)
├─ pz-cc-*.webp            치즈케이크 4장
├─ pz-room / pz-sign / pz-cups .webp  Visit
├─ og-paranzip.jpg
├─ img/                    다올 제공 원본 77장 (배포 제외 · 손님 방명록 손글씨 이름, 타 브랜드 로고 포함이라 레포에 올리지 말 것)
└─ CHANGELOG.md / STRUCTURE.md
```

## 섹션 순서
헤더 → 히어로 → `#gift`(옅은 파랑 면) → `#about` → `#financier` → `#cheesecake` → `#visit`(옅은 파랑 면) → 푸터 + 모바일 `.quick`.

## 영업시간 수정
Visit `.info` 영업시간 1곳. 요일별 시간이 정해지면 head JSON-LD에 `openingHoursSpecification` 추가.

## 전화번호 (여러 곳)
`tel:050713352691` 링크 전부 + 표시 숫자 + JSON-LD telephone. grep `050713352691` / `1335-2691`.

## 폰트 재생성
문구를 바꾸면 빠진 글자 검사(LESSONS §26) · `pyftsubset … --name-IDs='*' --name-languages='*' --name-legacy`(§24). Pretendard는 PretendardVariable을 instancer로 wght 400–700 고정 후 서브셋.
