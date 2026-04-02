# 온라인강의실 통합 기능 테스트 코스

이 저장소는 온라인강의실의 GitHub 기반 콘텐츠 기능을 한 번에 점검하기 위한 샘플 강의입니다.

## 이 코스로 테스트할 수 있는 것

- `course.yaml`, `lesson.yaml`, `content.md`, `quiz.yaml` 기반 sync
- lesson 공개/비공개
- lesson availability window
- lesson별 asset 업로드
- 루트 PDF asset과 `assets/` 하위 이미지 asset
- 퀴즈 공개/비공개
- 퀴즈 없음 lesson
- `mcq`, `short_answer`, `essay` 문제 유형
- question `order_index`
- ID write-back

## 회차 구성

1. `01-web-introduction`
   GitHub sync와 기본 강의실 동선. 공개 lesson + 공개 quiz + PDF + SVG asset
2. `02-html-basics`
   Markdown과 asset 중심 회차. 공개 lesson + active availability + quiz 없음
3. `03-css-styling`
   lesson은 공개지만 quiz는 비공개인 케이스
4. `04-javascript-basics`
   future availability가 걸린 예약 공개 회차
5. `05-project`
   available_until이 지난 만료 회차
6. `06-staff-preview`
   `published: false`인 staff 확인용 비공개 회차

## 플랫폼에서 추가로 해볼 것

이 저장소만으로는 아래 운영 기능은 표현되지 않습니다. import 후 플랫폼 UI에서 같이 테스트하면 됩니다.

- 강의 visibility / status
- 수강생 등록
- 강사 / 조교 권한
- quiz deadline 설정
- 서술형 수동 채점
- lesson / quiz published 토글
