# My Skills 사용 가이드

현재 폴더의 스킬들을 Claude Code용과 웹/독립 실행용으로 구분한 가이드입니다.

---

## 📦 Claude Code 전용 스킬

Claude Code의 `.claude/skills/` 폴더에 설치하여 사용하는 스킬들입니다.

### 설치 방법

```bash
# 전역 설치 (모든 프로젝트에서 사용)
cp -r skills/code-changelog ~/.claude/skills/
cp -r skills/meta-prompt-generator ~/.claude/skills/
cp -r skills/prompt-enhancer ~/.claude/skills/
cp -r skills/flutter-init ~/.claude/skills/
cp -r skills/nextjs15-init ~/.claude/skills/
cp -r skills/codex ~/.claude/skills/
cp -r skills/codex-claude-loop ~/.claude/skills/

# 또는 프로젝트별 설치 (특정 프로젝트에만)
cp -r skills/code-changelog ./.claude/skills/
cp -r skills/meta-prompt-generator ./.claude/skills/
cp -r skills/prompt-enhancer ./.claude/skills/
cp -r skills/flutter-init ./.claude/skills/
cp -r skills/nextjs15-init ./.claude/skills/
cp -r skills/codex ./.claude/skills/
cp -r skills/codex-claude-loop ./.claude/skills/
```

### 스킬 목록 및 실행 명령어

#### 1. Code Changelog
**설명**: AI가 생성한 모든 코드 변경사항을 자동으로 문서화하고 웹 브라우저에서 실시간으로 확인

**실행**: Claude Code에서
```
code-changelog
```

**주요 기능**:
- 자동 문서 생성 (Markdown)
- HTML 뷰어 (Python 서버)
- 다크 모드 UI
- 실시간 서버 (http://localhost:4000)

---

#### 2. Meta Prompt Generator
**설명**: 간단한 설명을 받아 구조화된 커스텀 슬래시 커맨드를 자동 생성

**실행**: Claude Code에서
```
meta-prompt-generator
```

**주요 기능**:
- 지능형 지식 수집 (웹 검색)
- 단계 기반 워크플로우 설계
- 포괄적인 테스트 생성
- 병렬 처리 최적화

---

#### 3. Prompt Enhancer
**설명**: 프로젝트 컨텍스트를 분석하여 간단한 개발 요청을 명확하고 상세한 요구사항으로 변환

**실행**: Claude Code에서
```
prompt-enhancer
```

**지원 스택**:
- Flutter (Clean Architecture, Riverpod)
- Next.js/React (App Router, Zustand)
- Python (Django, FastAPI)

---

#### 4. Flutter Init
**설명**: 도메인 기반 Flutter 프로젝트를 Clean Architecture로 자동 생성

**실행**: Claude Code에서
```
flutter-init
```

**기술 스택**:
- Riverpod 3.x (상태 관리)
- Drift (로컬 데이터베이스)
- Freezed (불변 모델)
- Easy Localization (다국어)
- FluentUI Icons

---

#### 5. Next.js 15 Init
**설명**: 도메인 기반 Next.js 15 프로젝트를 App Router로 자동 생성

**실행**: Claude Code에서
```
nextjs15-init
```

**기술 스택**:
- Next.js 15 (App Router)
- ShadCN/ui (UI 컴포넌트)
- Zustand (클라이언트 상태)
- Tanstack Query (서버 상태)
- Drizzle ORM (TypeScript ORM)
- Better Auth (인증)

---

#### 6. Codex
**설명**: OpenAI Codex CLI를 사용하여 코드 분석, 리팩토링, 자동화된 편집 수행

**실행**: Claude Code에서
```
codex
```

**샌드박스 모드**:
- `read-only`: 코드 분석 전용 (읽기만)
- `workspace-write`: 로컬 파일 수정
- `danger-full-access`: 네트워크 접근 포함 전체 권한

**주요 명령어**:
```bash
# 기본 실행
codex exec -m gpt-5-codex --sandbox read-only

# 세션 재개
codex exec resume --last

# 전체 자동 모드
codex exec --full-auto
```

---

#### 7. Codex-Claude Loop 🔄
**설명**: Claude Code와 Codex를 결합한 이중 AI 엔지니어링 루프로 최상의 코드 품질 보장

**실행**: Claude Code에서
```
codex-claude-loop
```

**핵심 워크플로우**:
1. **Claude (계획 + 구현)**
2. **Codex (검증)**
3. **피드백**
4. **Claude (수정)**
5. **Codex (재검증)**
6. **반복**

**실전 예시**:
```bash
# 1. Claude가 계획 수립 후
# 2. Codex로 계획 검증
echo "Review this plan..." | codex exec -m gpt-5-codex --config model_reasoning_effort="high" --sandbox read-only

# 3. Claude가 구현 후
# 4. Codex가 코드 리뷰
echo "Review implementation..." | codex exec --sandbox read-only

# 5. Claude가 수정 후
# 6. Codex가 재검증
echo "Verify fixes..." | codex exec resume --last
```

**언제 사용하나요**:
- ✅ 복잡한 기능 개발 (여러 단계)
- ✅ 보안/성능이 중요한 작업
- ✅ 대규모 리팩토링
- ✅ 높은 코드 품질이 필요할 때

---

## 🌐 웹/독립 실행 스킬

Claude Code 외부에서 독립적으로 사용하거나 웹 API로 사용하는 스킬들입니다.

### 1. Landing Page Guide

**설명**: Next.js와 React로 고품질 전환율 높은 랜딩페이지를 제작하기 위한 종합 가이드

**사용 방법**:
```bash
# 문서 읽기
cat skills/landing-page-guide/SKILL.md
cat skills/landing-page-guide/references/11-essential-elements.md
cat skills/landing-page-guide/references/component-examples.md
```

**주요 내용**:
- DESIGNNAS의 11가지 필수 요소 프레임워크
- ShadCN UI 컴포넌트 통합
- SEO 최적화 및 접근성 표준
- 반응형 디자인 및 성능 최적화

**11가지 필수 요소**:
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

---

### 2. Card News Generator (Python 독립 실행)

**설명**: 600x600 인스타그램 스타일 카드 뉴스 시리즈를 자동 생성 (단색 배경)

**설치 및 실행**:
```bash
# 필요한 패키지 설치
pip install pillow

# 스크립트 실행
cd skills/card-news-generator
python auto_generator.py --topic "당신의 주제" --color "245,243,238"
```

**주요 기능**:
- 주제와 색상만 입력하면 자동 생성
- 5-7장의 카드 시리즈 자동 제작
- 자동 텍스트 래핑 및 레이아웃
- RGB to Hex 색상 변환

**권장 색상**:
```bash
# 베이지
--color "245,243,238"

# 핑크
--color "255,229,229"

# 민트
--color "224,244,241"

# 라벤더
--color "232,224,245"

# 피치
--color "255,232,214"

# 스카이 블루
--color "227,242,253"
```

---

### 3. Card News Generator V2 (Python 독립 실행) 🆕

**설명**: 배경 이미지를 지원하는 향상된 카드 뉴스 생성기

**설치 및 실행**:
```bash
# 필요한 패키지 설치
pip install pillow

# 기본 실행 (단색 배경)
cd skills/card-news-generator-v2
python auto_generator.py --topic "당신의 주제"

# 배경 이미지 사용
python auto_generator.py \
  --topic "서울 부동산" \
  --image-folder ./my-images \
  --overlay-opacity 0.6 \
  --output-dir ./output
```

**V2 새로운 기능**:
- ✨ **배경 이미지 지원**: 폴더의 이미지를 배경으로 자동 적용
- ✨ **Cafe24Ssurround 폰트**: 번들 폰트 포함, 별도 설치 불필요
- ✨ **반투명 박스 + 테두리**: 텍스트 영역에 둥근 박스와 흰색 테두리
- ✨ **컴팩트 디자인**: 정사각형에 가까운 중앙 정렬 박스
- ✨ **오버레이 조절**: 텍스트 가독성을 위한 어두운 오버레이 (0.0-1.0)
- ✨ **자동 텍스트 색상**: 배경 이미지 사용 시 흰색으로 자동 전환

**지원 이미지 형식**: JPG, JPEG, PNG, WebP, BMP

**상세 옵션**:
```bash
python auto_generator.py \
  --topic "여행 가이드" \
  --image-folder ./backgrounds \
  --overlay-opacity 0.5 \
  --output-dir ./travel-cards \
  --color "245,243,238"  # 배경 이미지 없을 때 사용할 색상
```

---

### 4. Midjourney Card News Background

**설명**: Midjourney API를 사용하여 카드 뉴스용 배경 이미지 생성

**파일 위치**:
```bash
skills/midjourney-cardnews-bg/
```

**사용 방법**:
```bash
# 문서 읽기
cat skills/midjourney-cardnews-bg/SKILL.md
cat skills/midjourney-cardnews-bg/topics_reference.md
```

**주요 내용**:
- Midjourney 프롬프트 가이드
- 카드 뉴스에 적합한 배경 스타일
- 주제별 프롬프트 예시

---

## 📋 빠른 참조 테이블

### Claude Code 스킬 설치 (한 번에)

```bash
# 전역 설치
cd ~/my-skills
for skill in code-changelog meta-prompt-generator prompt-enhancer flutter-init nextjs15-init codex codex-claude-loop; do
  cp -r skills/$skill ~/.claude/skills/
done

# 프로젝트별 설치
cd /path/to/your/project
for skill in code-changelog meta-prompt-generator prompt-enhancer flutter-init nextjs15-init codex codex-claude-loop; do
  cp -r ~/my-skills/skills/$skill ./.claude/skills/
done
```

### Python 스킬 필수 패키지

```bash
# Card News Generator 및 V2용
pip install pillow
```

---

## 🎯 사용 시나리오별 추천

### 코드 품질 관리
- `code-changelog`: 코드 변경 이력 추적
- `codex`: 코드 리뷰 및 분석
- `codex-claude-loop`: 고품질 코드 개발

### 프로젝트 시작
- `flutter-init`: Flutter 앱 시작
- `nextjs15-init`: Next.js 앱 시작
- `landing-page-guide`: 랜딩페이지 제작

### 프롬프트 작성
- `prompt-enhancer`: 간단한 요청을 상세 요구사항으로
- `meta-prompt-generator`: 재사용 가능한 슬래시 커맨드 생성

### 콘텐츠 제작
- `card-news-generator`: 단색 배경 카드 뉴스
- `card-news-generator-v2`: 이미지 배경 카드 뉴스
- `midjourney-cardnews-bg`: AI 생성 배경 이미지

---

## 🔗 상세 문서 링크

### Claude Code 스킬
- [Code Changelog](./skills/code-changelog/SKILL.md)
- [Meta Prompt Generator](./skills/meta-prompt-generator/SKILL.md)
- [Prompt Enhancer](./skills/prompt-enhancer/SKILL.md)
- [Flutter Init](./skills/flutter-init/SKILL.md)
- [Next.js 15 Init](./skills/nextjs15-init/SKILL.md)
- [Codex](./skills/codex/SKILL.md)
- [Codex-Claude Loop](./skills/codex-claude-loop/SKILL.md)

### 웹/독립 실행
- [Landing Page Guide](./skills/landing-page-guide/SKILL.md)
- [Card News Generator](./skills/card-news-generator/SKILL.md)
- [Card News Generator V2](./skills/card-news-generator-v2/SKILL.md)
- [Midjourney Card News BG](./skills/midjourney-cardnews-bg/SKILL.md)

---

## 💡 팁

1. **Claude Code 스킬은 전역 설치 추천**: 모든 프로젝트에서 사용 가능
2. **Python 스킬은 독립 실행**: 필요할 때만 실행하면 됨
3. **Landing Page Guide는 참고 문서**: 랜딩페이지 제작 시 읽어보기
4. **Codex-Claude Loop는 복잡한 작업에**: 간단한 작업에는 과함

---

## 📄 라이선스

MIT License
