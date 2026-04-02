# 오리엔테이션: GitHub sync와 강의실 구조

이 회차는 온라인강의실에서 가장 먼저 확인해야 할 기본 흐름을 담고 있습니다.

## 이 회차에서 확인할 것

- `course.yaml`, `lesson.yaml`, `content.md`, `quiz.yaml`가 정상 sync되는지
- 회차 루트의 PDF asset이 업로드되는지
- `assets/` 하위 SVG image asset이 업로드되는지
- 공개 lesson과 공개 quiz가 학생 화면에 바로 노출되는지
- `mcq`, `short_answer`, `essay` 3종 문제가 정상 렌더링되는지

## 콘텐츠 파일 구조

```text
01-web-introduction/
├── lesson.yaml
├── content.md
├── slides.pdf
├── assets/
│   └── request-flow.svg
└── quiz.yaml
```

## 운영 메모

1. 이 회차는 학생이 실제로 열어볼 수 있는 공개 회차입니다.
2. `slides.pdf`는 루트 asset 테스트용입니다.
3. `assets/request-flow.svg`는 nested asset 테스트용입니다.

## 체크리스트

| 항목 | 기대 결과 |
|------|-----------|
| 회차 목록 | 회차가 보인다 |
| 본문 | Markdown이 렌더링된다 |
| asset 목록 | PDF와 SVG가 모두 보인다 |
| quiz 상세 | 문제 3종이 모두 보인다 |
| 제출 | 객관식과 단답형은 자동 채점, 서술형은 수동 채점 대기 |

## 참고 asset

- 구조 다이어그램: `assets/request-flow.svg`
- 발표 자료: `slides.pdf`
