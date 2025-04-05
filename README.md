# Character Memory Management System

## 📝 Project Overview

이 프로젝트는 AI 캐릭터의 기억을 관리하는 시스템입니다. 단기 기억(ShortTermMemory)과 장기 기억(LongTermMemory)을 구분하여 저장하고, 각각의 특성에 맞는 관리 방식을 적용합니다.

## 🗂 Directory Structure

```
character-prompt/
├── SASHA/
│   ├── ShortTermMemory/
│   │   └── daily_YYYY_MM_DD.json   # 일별 대화 및 상호작용 기록
│   ├── LongTermMemory/
│   │   ├── long_term_memory.json   # 장기 기억 저장소
│   │   └── archive/                # 보관된 기억 저장소
│   └── FileConvention.txt          # 파일 관리 프로토콜
└── README.md
```

## 💾 Memory Management

### ShortTermMemory
- 일주일 단위로 기억을 관리
- 날짜별로 파일 분리 (daily_YYYY_MM_DD.json)
- 대화, 감정 상태, 활동 내역 등을 실시간으로 기록
- 구조:
  ```json
  {
    "date": "YYYY-MM-DD",
    "conversation": [
      {
        "time": "HH:mm:ss",
        "user_message": "사용자 메시지",
        "sasha_response": "AI 응답",
        "sasha_emotion": "감정 상태",
        "activity": "수행한 활동"
      }
    ],
    "meta": {
      "current_entries": 1,
      "max_entries": 500,
      "last_updated": "YYYY-MM-DD HH:mm:ss"
    }
  }
  ```

### LongTermMemory
- 중요한 기억을 영구적으로 저장
- 단일 파일로 관리 (long_term_memory.json)
- 중요도에 따른 메모리 압축 및 보관
- 구조:
  ```json
  {
    "user_id": "사용자 ID",
    "timeline": [
      {
        "original_date": "YYYY-MM-DD",
        "stored_date": "YYYY-MM-DD",
        "event_type": "이벤트 유형",
        "description": "상세 설명",
        "user_emotion": "사용자 감정",
        "importance": 1-5
      }
    ],
    "meta": {
      "current_entries": 0,
      "importance_scale": "1-5",
      "max_storage": "100MB"
    }
  }
  ```

## 📋 Development History

### Initial Setup (2025-04-05)
1. 프로젝트 구조 설정
   - SASHA 디렉토리 생성
   - 메모리 관리를 위한 하위 디렉토리 구성
   - FileConvention.txt 작성

2. 기억 관리 프로토콜 정의
   - 단기/장기 기억 구조 설계
   - 파일 명명 규칙 수립
   - 메모리 관리 로직 정의

3. 커밋 컨벤션 수립
   - 기억 관리 시스템에 특화된 커밋 타입 정의
   - 스코프 및 규칙 설정
   - 예제 커밋 메시지 작성

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