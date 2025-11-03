# 웹/독립 실행 스킬 모음

Claude Code 외부에서 독립적으로 사용하거나 웹 API로 사용하는 스킬들입니다.

---

## 📚 1. Landing Page Guide (문서/가이드)

**설명**: Next.js와 React로 고품질 전환율 높은 랜딩페이지를 제작하기 위한 종합 가이드

### 사용 방법

```bash
# 메인 가이드 읽기
cat ~/my-skills/skills/landing-page-guide/SKILL.md

# 11가지 필수 요소 참고
cat ~/my-skills/skills/landing-page-guide/references/11-essential-elements.md

# 컴포넌트 예시 코드
cat ~/my-skills/skills/landing-page-guide/references/component-examples.md
```

### 주요 내용

**DESIGNNAS의 11가지 필수 요소**:
1. 키워드가 포함된 URL
2. 회사 로고 (상단 왼쪽)
3. SEO 최적화된 제목과 부제목
4. 주요 CTA (히어로 섹션)
5. 사회적 증거 (리뷰, 통계)
6. 이미지 또는 동영상
7. 핵심 이점/기능 (3-6개)
8. 고객 후기 (4-6개)
9. FAQ 섹션 (5-10개 질문)
10. 최종 CTA (하단)
11. 연락처 정보 및 법적 페이지

**기술 스택**:
- Next.js 14+ (App Router)
- TypeScript
- Tailwind CSS
- ShadCN UI

**사용 시나리오**:
- 마케팅 랜딩 페이지 제작
- 제품 소개 페이지 개발
- 전환율 최적화가 필요한 프로모션 페이지
- SaaS/이커머스/서비스/이벤트 랜딩 페이지

---

## 🎨 2. Card News Generator (Python 독립 실행)

**설명**: 600x600 인스타그램 스타일 카드 뉴스 시리즈를 자동 생성 (단색 배경)

### 설치 및 실행

```bash
# 1. 필요한 패키지 설치
pip install pillow

# 2. 스크립트 디렉토리로 이동
cd ~/my-skills/skills/card-news-generator

# 3. 기본 실행 (베이지 배경)
python auto_generator.py --topic "당신의 주제"

# 4. 색상 지정 실행
python auto_generator.py --topic "AI 트렌드 2024" --color "245,243,238"
```

### 주요 기능

- 주제와 색상만 입력하면 자동 생성
- 5-7장의 카드 시리즈 자동 제작
- 자동 텍스트 래핑 및 레이아웃
- RGB to Hex 색상 변환
- 단일 카드/멀티 카드 모드

### 권장 색상 프리셋

```bash
# 베이지 (따뜻하고 부드러운)
python auto_generator.py --topic "주제" --color "245,243,238"

# 핑크 (부드럽고 페미닌)
python auto_generator.py --topic "주제" --color "255,229,229"

# 민트 (신선하고 깨끗한)
python auto_generator.py --topic "주제" --color "224,244,241"

# 라벤더 (우아하고 차분한)
python auto_generator.py --topic "주제" --color "232,224,245"

# 피치 (활기차고 밝은)
python auto_generator.py --topic "주제" --color "255,232,214"

# 스카이 블루 (신뢰감 있는)
python auto_generator.py --topic "주제" --color "227,242,253"
```

### 캔버스 사양

- 크기: 600x600 픽셀 (인스타그램 최적화)
- 자동 텍스트 줄바꿈
- 번호 배지, 제목, 본문 계층 구조
- 다양한 색상 프리셋 제공

### 사용 시나리오

- 소셜 미디어 카드 뉴스 제작
- 인스타그램 콘텐츠 시리즈
- 정보 전달용 카드 이미지
- 교육/마케팅 콘텐츠

---

## 🎨 3. Card News Generator V2 (Python 독립 실행) 🆕

**설명**: 배경 이미지를 지원하는 향상된 카드 뉴스 생성기

### 설치 및 실행

```bash
# 1. 필요한 패키지 설치
pip install pillow

# 2. 스크립트 디렉토리로 이동
cd ~/my-skills/skills/card-news-generator-v2

# 3. 기본 실행 (단색 배경)
python auto_generator.py --topic "당신의 주제"

# 4. 배경 이미지 사용
python auto_generator.py \
  --topic "서울 부동산" \
  --image-folder ./my-images \
  --overlay-opacity 0.6 \
  --output-dir ./output
```

### V2 새로운 기능 ✨

- **배경 이미지 지원**: 폴더의 이미지를 배경으로 자동 적용
- **Cafe24Ssurround 폰트**: 번들 폰트 포함, 별도 설치 불필요
- **반투명 박스 + 테두리**: 텍스트 영역에 둥근 박스와 흰색 테두리
- **컴팩트 디자인**: 정사각형에 가까운 중앙 정렬 박스
- **오버레이 조절**: 텍스트 가독성을 위한 어두운 오버레이 (0.0-1.0)
- **자동 텍스트 색상**: 배경 이미지 사용 시 흰색으로 자동 전환

### 기술 사양

- 배경 이미지 자동 크롭 및 리사이징 (600x600)
- 지원 형식: JPG, JPEG, PNG, WebP, BMP
- macOS/Linux 자동 폰트 감지
- 텍스트 박스 너비: 캔버스의 65% (양쪽 여백 확보)

### 상세 사용 예시

```bash
# 기본 (단색 배경)
python auto_generator.py --topic "마케팅 팁"

# 배경 이미지 + 약한 오버레이
python auto_generator.py \
  --topic "여행 가이드" \
  --image-folder ./travel-photos \
  --overlay-opacity 0.3

# 배경 이미지 + 강한 오버레이 (텍스트 가독성 향상)
python auto_generator.py \
  --topic "부동산 정보" \
  --image-folder ./building-photos \
  --overlay-opacity 0.7 \
  --output-dir ./real-estate-cards

# 단색 배경 + 커스텀 색상
python auto_generator.py \
  --topic "건강 팁" \
  --color "224,244,241" \
  --output-dir ./health-cards
```

### 배경 이미지 준비

```bash
# 배경 이미지 폴더 구조
my-images/
├── bg1.jpg
├── bg2.png
├── bg3.jpeg
└── bg4.webp

# 스크립트 실행
python auto_generator.py \
  --topic "주제" \
  --image-folder ./my-images
```

**이미지 사용 규칙**:
- 폴더의 이미지들을 순서대로 카드에 적용
- 카드 수보다 이미지가 적으면 이미지 재사용
- 카드 수보다 이미지가 많으면 처음부터 순서대로 사용
- 모든 이미지는 자동으로 600x600으로 리사이징 및 크롭

### 오버레이 투명도 가이드

```bash
# 0.0 - 오버레이 없음 (밝은 배경 이미지용)
--overlay-opacity 0.0

# 0.3 - 약한 오버레이 (배경이 어두운 경우)
--overlay-opacity 0.3

# 0.5 - 중간 오버레이 (일반적인 경우, 권장)
--overlay-opacity 0.5

# 0.7 - 강한 오버레이 (배경이 복잡하거나 밝은 경우)
--overlay-opacity 0.7

# 1.0 - 완전 불투명 (거의 단색 배경)
--overlay-opacity 1.0
```

### 사용 시나리오

- 실제 사진을 배경으로 한 카드 뉴스
- 여행, 부동산, 음식 등 비주얼이 중요한 콘텐츠
- 전문적이고 세련된 디자인이 필요한 경우
- 배경 이미지로 브랜드 아이덴티티 강화

---

## 🖼️ 4. Midjourney Card News Background (가이드)

**설명**: Midjourney API를 사용하여 카드 뉴스용 배경 이미지 생성 가이드

### 사용 방법

```bash
# 메인 가이드 읽기
cat ~/my-skills/skills/midjourney-cardnews-bg/SKILL.md

# 주제별 프롬프트 참고
cat ~/my-skills/skills/midjourney-cardnews-bg/topics_reference.md
```

### 주요 내용

- Midjourney 프롬프트 작성 가이드
- 카드 뉴스에 적합한 배경 스타일
- 주제별 프롬프트 예시
- 600x600 정사각형 이미지 생성 팁

### 실전 워크플로우

```bash
# 1. Midjourney로 배경 이미지 생성
# (가이드 문서에서 주제별 프롬프트 확인)

# 2. 생성된 이미지 다운로드
mkdir card-backgrounds
# 이미지를 card-backgrounds/ 폴더에 저장

# 3. Card News Generator V2로 카드 생성
cd ~/my-skills/skills/card-news-generator-v2
python auto_generator.py \
  --topic "당신의 주제" \
  --image-folder ../card-backgrounds \
  --overlay-opacity 0.5
```

---

## 🚀 빠른 시작 가이드

### Card News 제작 (단색 배경)

```bash
# 1. 기본 설치
pip install pillow

# 2. 카드 생성
cd ~/my-skills/skills/card-news-generator
python auto_generator.py \
  --topic "AI 트렌드 2024" \
  --color "245,243,238"
```

### Card News 제작 (이미지 배경)

```bash
# 1. 기본 설치
pip install pillow

# 2. 배경 이미지 준비
mkdir ~/card-backgrounds
# 이미지 파일들을 ~/card-backgrounds/ 에 복사

# 3. 카드 생성
cd ~/my-skills/skills/card-news-generator-v2
python auto_generator.py \
  --topic "서울 부동산 가이드" \
  --image-folder ~/card-backgrounds \
  --overlay-opacity 0.6 \
  --output-dir ~/card-output
```

### Landing Page 제작

```bash
# 1. 가이드 문서 읽기
cat ~/my-skills/skills/landing-page-guide/SKILL.md

# 2. Next.js 프로젝트 생성
npx create-next-app@latest my-landing-page

# 3. ShadCN UI 설치
cd my-landing-page
npx shadcn-ui@latest init

# 4. 가이드 참고하여 개발
# (11가지 필수 요소 체크리스트 사용)
```

---

## 📊 스킬 비교표

| 스킬 | 배경 스타일 | 난이도 | 용도 |
|------|------------|--------|------|
| Card News Generator | 단색 | ⭐ 쉬움 | 심플한 정보 전달 |
| Card News Generator V2 | 이미지 | ⭐⭐ 보통 | 비주얼 중심 콘텐츠 |
| Midjourney BG | AI 생성 | ⭐⭐⭐ 어려움 | 창의적 디자인 |
| Landing Page Guide | - | ⭐⭐⭐ 어려움 | 웹 페이지 제작 |

---

## 💡 추천 워크플로우

### 소셜 미디어 콘텐츠 제작

```bash
# 간단한 정보성 카드 → Card News Generator
python auto_generator.py --topic "주제" --color "245,243,238"

# 비주얼 중심 카드 → Card News Generator V2 + 직접 촬영한 사진
python auto_generator.py --topic "주제" --image-folder ./my-photos

# 창의적 디자인 → Midjourney BG + Card News Generator V2
# 1. Midjourney로 배경 생성
# 2. V2로 카드 제작
```

### 웹 프로젝트 제작

```bash
# 1. Landing Page Guide 참고
cat ~/my-skills/skills/landing-page-guide/SKILL.md

# 2. Next.js 프로젝트 생성 (Claude Code의 nextjs15-init 스킬 사용 가능)
# 3. 11가지 필수 요소 체크리스트 준수하여 개발
```

---

## 🔧 문제 해결

### Pillow 설치 오류

```bash
# macOS
brew install python3-pillow

# Ubuntu/Debian
sudo apt-get install python3-pil

# Windows
pip install pillow
```

### 폰트 문제 (Card News Generator V2)

```bash
# 폰트는 번들로 제공되므로 별도 설치 불필요
# 문제 발생 시 스크립트 폴더의 fonts/ 디렉토리 확인

cd ~/my-skills/skills/card-news-generator-v2
ls fonts/
# Cafe24Ssurround.ttf 파일이 있는지 확인
```

### 이미지 형식 오류

```bash
# 지원 형식: JPG, JPEG, PNG, WebP, BMP
# 다른 형식은 변환 필요

# ImageMagick으로 변환
convert image.heic image.jpg
```

---

## 📚 상세 문서

```bash
# Landing Page Guide
cat ~/my-skills/skills/landing-page-guide/SKILL.md
cat ~/my-skills/skills/landing-page-guide/references/11-essential-elements.md

# Card News Generator
cat ~/my-skills/skills/card-news-generator/SKILL.md
cat ~/my-skills/skills/card-news-generator/QUICKSTART_KR.md
cat ~/my-skills/skills/card-news-generator/COMPLETE_GUIDE_KR.md

# Card News Generator V2
cat ~/my-skills/skills/card-news-generator-v2/SKILL.md
cat ~/my-skills/skills/card-news-generator-v2/V2_FEATURES.md
cat ~/my-skills/skills/card-news-generator-v2/QUICKSTART_KR.md

# Midjourney Card News BG
cat ~/my-skills/skills/midjourney-cardnews-bg/SKILL.md
cat ~/my-skills/skills/midjourney-cardnews-bg/topics_reference.md
```

---

## 📄 라이선스

MIT License
