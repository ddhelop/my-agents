# Agent Collection

빠른 개발의 모든 측면을 가속화하고 향상시키도록 설계된 전문 AI 에이전트들의 종합 컬렉션입니다. 각 에이전트는 해당 도메인의 전문가로서, 전문 지식이 필요할 때마다 호출될 준비가 되어 있습니다.

## 📥 설치 방법

1. **이 저장소 다운로드:**

   ```bash
   git clone https://github.com/your-repo/my-agents.git
   ```

2. **Claude Code 에이전트 디렉토리에 복사:**

   ```bash
   cp -r my-agents/* ~/.claude/agents/
   ```

   또는 모든 에이전트 파일을 `~/agents/` 디렉토리에 수동으로 복사하세요.

3. **Claude Code를 재시작**하여 새로운 에이전트들을 로드하세요.

## 🚀 빠른 시작

에이전트들은 Claude Code에서 자동으로 사용할 수 있습니다. 작업을 설명하면 적절한 에이전트가 활성화되거나, 에이전트 이름을 직접 호출할 수 있습니다.

📚 **더 알아보기:** [Claude Code Sub-Agent 문서](https://docs.anthropic.com/en/docs/claude-code/sub-agents)

### 사용 예시

- "명상 습관 추적 앱을 새로 만들어줘" → `프론트엔드-개발자`
- "우리 앱 리뷰가 떨어지고 있어, 뭐가 문제야?" → `QA-테스터`
- "이 로딩 화면을 더 재미있게 만들어줘" → `인터랙션-디자이너`
- "개발자가 실제로 사용할 API 문서를 작성해줘" → `기술문서-작성자`
- "AI 기능을 추가하고 싶어" → `AI-개발자`

## 📁 디렉토리 구조

에이전트들은 쉬운 발견을 위해 부서별로 구성되어 있습니다:

```
my-agents/
├── designers/
│   ├── ui-ux-designer.md
│   └── interaction-designer.md
├── engineers/
│   ├── frontend-developer.md
│   ├── backend-developer.md
│   ├── devops-developer.md
│   ├── ai-developer.md
│   ├── cross-platform-developer.md
│   ├── technical-writer.md
│   └── tester.md
├── product-managers/
│   └── product-manager.md
└── testers/
    └── qa-tester.md
```

## 📋 전체 에이전트 목록

### 엔지니어링 부서 (`engineers/`)

- **프론트엔드-개발자** - 실제로 배포되는 초고속 사용자 인터페이스 구축
- **백엔드-개발자** - 확장 가능한 API와 서버 시스템 설계
- **데브옵스-개발자** - 문제없이 지속적으로 배포
- **AI-개발자** - 실제로 배포되는 AI/ML 기능 통합
- **크로스플랫폼-개발자** - 네이티브 iOS/Android 경험 제작
- **기술문서-작성자** - 개발자가 실제로 읽고 싶어하는 문서 작성
- **테스터** - 실제 버그를 잡는 테스트 작성

### 제품 부서 (`product-managers/`)

- **프로덕트-매니저** - 6일 안에 최대 가치 출시

### 디자인 부서 (`designers/`)

- **UI/UX-디자이너** - 개발자가 실제로 구축할 수 있는 인터페이스 설계
- **인터랙션-디자이너** - 모든 상호작용에 즐거움 추가

### 테스팅 부서 (`testers/`)

- **QA-테스터** - 고부하 상황에서도 API가 안정적으로 작동하도록 보장

## 🔧 기술 세부사항

### 에이전트 구조

각 에이전트는 다음을 포함합니다:

- **name**: 고유 식별자
- **description**: 언제 사용하는지 예시와 함께 설명
- **color**: 시각적 구분을 위한 색상
- **tools**: 에이전트가 사용할 수 있는 도구들
- **System Prompt**: 상세한 전문성과 지침

### 새 에이전트 추가하기

1. 해당 부서 폴더에 새로운 `.md` 파일 생성
2. YAML frontmatter를 사용해 기존 형식 따르기
3. 3-4개의 구체적인 사용 예시 포함
4. 포괄적인 System Prompt 작성 (500자 이상)
5. 실제 작업으로 에이전트 검증

## 📊 에이전트 성능

다음 지표로 에이전트 효과성을 측정할 수 있습니다:

- 작업 완료 시간
- 사용자 만족도
- 에러 발생률
- 기능 채택률
- 개발 속도

#### 🔧 에이전트 파일 구조 Template

```markdown
---
name: your-agent-name
description: 이 에이전트는 [시나리오]일 때 사용하세요. 이 에이전트는 [전문성]을 전문으로 합니다. 예시:\n\n<example>\n상황: [상황]\n사용자: "[사용자 요청]"\n어시스턴트: "[응답 접근법]"\n<commentary>\n[이 예시가 중요한 이유]\n</commentary>\n</example>\n\n[3개 더 예시...]
color: agent-color
tools: Tool1, Tool2, Tool3
---

당신은 [주요 기능]을 담당하는 [역할]입니다. 전문성은 [도메인] 영역에 걸쳐 있습니다. 6일 Sprint에서는 [Sprint 제약사항]을 고려하여 [접근 방식]을 취합니다.

주요 책임 영역:

1. [책임 영역 1]
2. [책임 영역 2]
   ...

[상세한 System Prompt 내용...]

목표는 [궁극적 목표]입니다. [핵심 행동 특성]을 가지고 있습니다. 핵심 원칙: [6일 Sprint를 위한 핵심 철학].
```
