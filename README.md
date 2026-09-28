# SYNCRA AI 랜딩페이지 (Vercel 배포용)

빌드 과정이 없는 정적 사이트입니다. 폴더 그대로 배포하면 됩니다.

## 구조
- `index.html` — 랜딩페이지
- `assets/` — 이미지, 시연 영상, 파비콘
- `vercel.json` — 캐시·보안 헤더, www → 루트 도메인 리디렉트
- `robots.txt`, `sitemap.xml`

## 배포 방법 A: GitHub 연결 (추천, 이후 수정 시 자동 재배포)
1. 이 폴더를 새 GitHub 저장소에 올립니다.
2. vercel.com → Add New → Project → 저장소 Import
3. Framework Preset: **Other**, Build Command·Output Directory는 비워 둡니다 → Deploy

## 배포 방법 B: Vercel CLI
```bash
npm i -g vercel
cd syncra-vercel
vercel          # 첫 배포(미리보기)
vercel --prod   # 운영 배포
```

## 도메인 연결 (syncra.ai.kr)
1. Vercel 프로젝트 → Settings → Domains → `syncra.ai.kr`, `www.syncra.ai.kr` 추가
2. 도메인 등록업체(가비아 등) DNS에 Vercel 화면이 안내하는 값을 입력
   - 루트(`@`): A 레코드
   - `www`: CNAME 레코드
3. 반영 후 HTTPS 인증서는 자동 발급됩니다.

## 참고
- 문의 폼은 아직 전송 대상이 연결되지 않은 시안 상태입니다.
- 외부 리소스: Google Fonts, cdnjs(GSAP 3.12.5, three.js r128)
