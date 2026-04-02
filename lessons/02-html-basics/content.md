# Markdown과 asset 렌더링 확인

이 회차는 **퀴즈가 없는 회차**입니다. 학생 화면에서 빈 퀴즈 상태와 asset 리스트만 확인할 때 사용합니다.

## 본문 요소 테스트

### 체크리스트

- 제목 / 소제목
- 표
- 코드블록
- 강조 텍스트
- 목록

```yaml
title: "Markdown과 asset 렌더링 확인"
published: true
```

| 필드 | 목적 |
|------|------|
| `title` | 회차 제목 |
| `description` | 회차 설명 |
| `published` | 학생 공개 여부 |
| `available_from` | 공개 시작 시각 |
| `available_until` | 공개 종료 시각 |

## asset 안내

이 회차에는 nested image asset 하나만 둡니다.

- 설명 다이어그램: `assets/markdown-layout.svg`

## 기대 동작

- 회차는 학생에게 보여야 한다
- 본문은 정상 렌더링되어야 한다
- 퀴즈 리스트는 비어 있어야 한다
- asset 리스트에는 SVG 한 개가 보여야 한다
