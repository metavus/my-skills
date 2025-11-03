# Claude Code 전용 스킬 모음

Claude Code의 `.claude/skills/` 폴더에 설치하여 사용하는 스킬들입니다.

---

## 🚀 빠른 설치 (전체 스킬 한 번에)

### 전역 설치 (모든 프로젝트에서 사용)

```bash
cd ~/my-skills
cp -r skills/code-changelog ~/.claude/skills/
cp -r skills/meta-prompt-generator ~/.claude/skills/
cp -r skills/prompt-enhancer ~/.claude/skills/
cp -r skills/flutter-init ~/.claude/skills/
cp -r skills/nextjs15-init ~/.claude/skills/
cp -r skills/codex ~/.claude/skills/
cp -r skills/codex-claude-loop ~/.claude/skills/
```

### 프로젝트별 설치 (특정 프로젝트에만)

```bash
cd /path/to/your/project
cp -r ~/my-skills/skills/code-changelog ./.claude/skills/
cp -r ~/my-skills/skills/meta-prompt-generator ./.claude/skills/
cp -r ~/my-skills/skills/prompt-enhancer ./.claude/skills/
cp -r ~/my-skills/skills/flutter-init ./.claude/skills/
cp -r ~/my-skills/skills/nextjs15-init ./.claude/skills/
cp -r ~/my-skills/skills/codex ./.claude/skills/
cp -r ~/my-skills/skills/codex-claude-loop ./.claude/skills/
```

### 스킬 확인

```
/skills
```

---

## 📦 개별 스킬 설치 및 사용법

### 1. Code Changelog

**설명**: AI가 생성한 모든 코드 변경사항을 자동으로 문서화하고 웹 브라우저에서 실시간으로 확인

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/code-changelog ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/code-changelog ./.claude/skills/
```

**실행**: Claude Code에서
```
code-changelog
```

**주요 기능**:
- 자동 문서 생성 (Markdown)
- HTML 뷰어 (Python 서버)
- 다크 모드 UI (GitHub 스타일)
- 실시간 서버 (http://localhost:4000)

**사용 시나리오**:
- 코드 리뷰 문서 자동 생성
- 변경 이력 추적
- 팀원과 변경사항 공유

---

### 2. Meta Prompt Generator

**설명**: 간단한 설명을 받아 단계별 병렬 처리가 가능한 구조화된 커스텀 슬래시 커맨드를 자동 생성

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/meta-prompt-generator ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/meta-prompt-generator ./.claude/skills/
```

**실행**: Claude Code에서
```
meta-prompt-generator
```

**주요 기능**:
- 지능형 지식 수집 (웹 검색)
- 단계 기반 워크플로우 설계
- 포괄적인 테스트 생성
- 병렬 처리 최적화

**사용 시나리오**:
- 복잡한 프로젝트 워크플로우 자동화
- 재사용 가능한 슬래시 커맨드 생성
- 체계적인 테스트 스위트 작성

---

### 3. Prompt Enhancer

**설명**: 프로젝트 컨텍스트를 분석하여 간단한 개발 요청을 명확하고 상세한 요구사항으로 변환

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/prompt-enhancer ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/prompt-enhancer ./.claude/skills/
```

**실행**: Claude Code에서
```
prompt-enhancer
```

**주요 기능**:
- 프로젝트 구조 자동 분석
- 기존 패턴 인식
- 구조화된 요구사항 생성
- 프레임워크별 최적화

**사용 예시**:
- "로그인 기능 만들어줘" → 상세한 구현 요구사항
- Clean Architecture 기반 설계 제안
- 프로젝트 컨벤션 자동 적용

**지원 스택**:
- Flutter (Clean Architecture, Riverpod)
- Next.js/React (App Router, Zustand)
- Python (Django, FastAPI)

---

### 4. Flutter Init

**설명**: 도메인 기반 Flutter 프로젝트를 Clean Architecture로 자동 생성

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/flutter-init ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/flutter-init ./.claude/skills/
```

**실행**: Claude Code에서
```
flutter-init
```

**주요 기능**:
- 도메인 선택 (Todo/Habit/Note/Expense/Custom)
- 스택 프리셋 (Minimal/Essential/Full Stack/Custom)
- Clean Architecture 자동 생성
- Riverpod 3.0, Drift, Freezed 설정

**기술 스택**:
- Riverpod 3.x (상태 관리)
- Drift (로컬 데이터베이스)
- Freezed (불변 모델)
- Easy Localization (다국어)
- FluentUI Icons

**사용 시나리오**:
- 새로운 Flutter 앱 빠른 시작
- Clean Architecture 보일러플레이트
- 도메인 중심 설계

---

### 5. Next.js 15 Init

**설명**: 도메인 기반 Next.js 15 프로젝트를 App Router로 자동 생성

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/nextjs15-init ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/nextjs15-init ./.claude/skills/
```

**실행**: Claude Code에서
```
nextjs15-init
```

**주요 기능**:
- 도메인 선택 (Todo/Blog/Dashboard/E-commerce/Custom)
- 스택 프리셋 (Minimal/Essential/Full Stack/Custom)
- App Router 기반 구조
- TypeScript Strict Mode

**기술 스택**:
- Next.js 15 (App Router)
- ShadCN/ui (UI 컴포넌트)
- Zustand (클라이언트 상태)
- Tanstack Query (서버 상태)
- Drizzle ORM (TypeScript ORM)
- Better Auth (인증)

**사용 시나리오**:
- 새로운 Next.js 앱 빠른 시작
- 타입 안전한 풀스택 앱
- 도메인 중심 설계

---

### 6. Codex

**설명**: OpenAI Codex CLI를 사용하여 코드 분석, 리팩토링, 자동화된 편집을 수행

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/codex ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/codex ./.claude/skills/
```

**실행**: Claude Code에서
```
codex
```

**주요 기능**:
- 대화형 모델 및 추론 레벨 선택 (gpt-5, gpt-5-codex)
- 샌드박스 모드 (read-only, workspace-write, danger-full-access)
- 세션 재개 기능 (codex exec resume --last)
- 자동화된 코드 편집 (--full-auto)

**샌드박스 모드**:
- `read-only`: 코드 분석 전용 (읽기만)
- `workspace-write`: 로컬 파일 수정
- `danger-full-access`: 네트워크 접근 포함 전체 권한

**주요 명령어**:
```bash
# 기본 실행
codex exec -m gpt-5-codex --sandbox read-only

# 고도 추론 모드
codex exec -m gpt-5-codex --config model_reasoning_effort="high" --sandbox read-only

# 세션 재개
codex exec resume --last

# 전체 자동 모드
codex exec --full-auto
```

**사용 시나리오**:
- 코드 리뷰 및 분석
- 대규모 리팩토링 자동화
- 코드베이스 전체 수정 작업
- 이전 세션 이어서 작업

---

### 7. Codex-Claude Loop 🔄

**설명**: Claude Code와 Codex를 결합한 이중 AI 엔지니어링 루프로 최상의 코드 품질을 보장

**설치**:
```bash
# 전역
cp -r ~/my-skills/skills/codex-claude-loop ~/.claude/skills/

# 프로젝트별
cp -r ~/my-skills/skills/codex-claude-loop ./.claude/skills/
```

**실행**: Claude Code에서
```
codex-claude-loop
```

**핵심 워크플로우**:
1. **Claude (계획 + 구현)** → 아키텍처 설계 및 코드 작성
2. **Codex (검증)** → 로직 에러, 보안 취약점 검토
3. **피드백** → 개선 사항 제안
4. **Claude (수정)** → 피드백 기반 코드 수정
5. **Codex (재검증)** → 수정사항 확인
6. **반복** → 품질 기준 충족 시까지

**주요 기능**:
- 계획 단계: Claude가 아키텍처와 구현 계획 수립
- 검증 단계: Codex가 계획의 로직 에러, 보안 취약점 검토
- 구현 단계: Claude가 검증된 계획으로 코드 작성 (Edit/Write 도구 사용)
- 코드 리뷰: Codex가 구현된 코드의 버그, 성능, 보안 검증
- 수정 반영: Claude가 Codex 피드백 기반으로 코드 수정
- 재검증: Codex가 수정사항 확인

**언제 사용하나요**:
- ✅ 복잡한 기능 개발 (여러 단계)
- ✅ 보안/성능이 중요한 작업
- ✅ 대규모 리팩토링
- ✅ 높은 코드 품질이 필요할 때
- ❌ 간단한 일회성 수정 (과함)
- ❌ 프로토타입/실험 코드 (과함)

**실전 예시**:
```bash
# 1. Claude가 OAuth 2.0 로그인 계획 수립
# 2. Codex로 계획 검증
echo "Review this plan for OAuth 2.0 implementation..." | codex exec -m gpt-5-codex --config model_reasoning_effort="high" --sandbox read-only

# 3. Claude가 검증된 계획으로 구현 (Edit/Write 도구 사용)
# 4. Codex가 구현된 코드 리뷰
echo "Review implementation in auth/oauth.ts..." | codex exec --sandbox read-only

# 5. Claude가 피드백 반영하여 코드 수정
# 6. Codex가 재검증
echo "Verify fixes in auth/oauth.ts..." | codex exec resume --last
```

**역할 분담**:
- **Claude**: 모든 코드 작성 및 수정
- **Codex**: 모든 검증 및 리뷰

**모델 선택 가이드**:
- `gpt-5`: 빠른 일반 작업
- `gpt-5-codex`: 복잡한 코드 분석 (권장)

**Reasoning Effort**:
- `low`: 간단한 검증
- `medium`: 일반적인 작업 (권장)
- `high`: 보안/critical 로직

---

## 🎯 사용 시나리오별 추천

### 코드 품질 관리
```
code-changelog        # 코드 변경 이력 추적
codex                 # 코드 리뷰 및 분석
codex-claude-loop     # 고품질 코드 개발 (복잡한 작업)
```

### 프로젝트 빠른 시작
```
flutter-init          # Flutter 프로젝트 생성
nextjs15-init         # Next.js 15 프로젝트 생성
```

### 프롬프트/워크플로우 작성
```
prompt-enhancer       # 간단한 요청을 상세 요구사항으로
meta-prompt-generator # 재사용 가능한 슬래시 커맨드 생성
```

---

## 📚 상세 문서

각 스킬의 상세 정보는 다음 파일들을 참고하세요:

```bash
# Code Changelog
cat ~/my-skills/skills/code-changelog/SKILL.md

# Meta Prompt Generator
cat ~/my-skills/skills/meta-prompt-generator/SKILL.md

# Prompt Enhancer
cat ~/my-skills/skills/prompt-enhancer/SKILL.md

# Flutter Init
cat ~/my-skills/skills/flutter-init/SKILL.md

# Next.js 15 Init
cat ~/my-skills/skills/nextjs15-init/SKILL.md

# Codex
cat ~/my-skills/skills/codex/SKILL.md

# Codex-Claude Loop
cat ~/my-skills/skills/codex-claude-loop/SKILL.md
cat ~/my-skills/skills/codex-claude-loop/README.md
```

---

## 💡 팁

1. **전역 설치 추천**: 모든 프로젝트에서 스킬을 사용할 수 있습니다
2. **스킬 목록 확인**: Claude Code에서 `/skills` 명령어로 설치된 스킬 확인
3. **Codex-Claude Loop는 신중하게**: 복잡하고 중요한 작업에만 사용 (간단한 작업에는 과함)
4. **Init 스킬은 빈 폴더에서**: 새 프로젝트 시작 시 사용

---

## 🔧 문제 해결

### 스킬이 보이지 않을 때
```bash
# 설치 경로 확인
ls ~/.claude/skills/
ls ./.claude/skills/

# Claude Code 재시작
# (터미널에서 Claude Code 종료 후 재실행)
```

### Codex 관련 오류
```bash
# Codex CLI 설치 확인
which codex

# Codex CLI 설치 (없을 경우)
# OpenAI Codex CLI 공식 문서 참고
```

---

## 📄 라이선스

MIT License
