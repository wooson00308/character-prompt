# Character Memory Management System

## 🎯 Commit Convention

### Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- `memory`: 기억 데이터 관련 변경 (단기/장기 기억 데이터 추가, 수정, 삭제)
- `proto`: 기억 프로토콜 관련 변경 (기억 저장/검색/관리 로직)
- `char`: 캐릭터 특성 관련 변경 (성격, 말투, 행동 패턴)
- `sys`: 시스템 구조 변경 (디렉토리 구조, 설정 파일)
- `docs`: 문서 관련 변경 (README, 주석, 문서화)
- `fix`: 버그 수정
- `refactor`: 코드 리팩토링
- `test`: 테스트 코드 관련 변경

### Scope (Optional)
- `short`: 단기 기억 관련
- `long`: 장기 기억 관련
- `archive`: 보관된 기억 관련
- `emotion`: 감정 상태 관련
- `interact`: 상호작용 패턴 관련

### Subject Rules
- 50자 이내로 작성
- 현재 시제 사용 ("changed" → "change")
- 첫 글자는 소문자로 시작
- 마침표로 끝내지 않음

### Examples
```
memory(short): add daily conversation with user about coding

- 사용자와 코딩 관련 대화 내용 추가
- 감정 상태 및 반응 패턴 기록

Related to: daily_2025_04_05.json
```

```
proto(long): update memory compression algorithm

- 장기 기억 압축 알고리즘 최적화
- 중요도 기반 메모리 관리 로직 개선

Performance: 30% 저장 공간 절약
```

```
char(emotion): refine emotional response patterns

- 공감 능력 향상을 위한 감정 표현 패턴 수정
- 상황별 반응 다양성 증가

Impact: 더 자연스러운 대화 흐름 생성
```