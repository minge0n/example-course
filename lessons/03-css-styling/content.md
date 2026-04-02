# 공개 lesson + 비공개 quiz 조합

이 회차는 lesson은 공개되어 있지만 quiz는 `published: false`로 설정되어 있습니다.

## 확인 포인트

- 회차 목록에는 노출된다
- 본문은 정상적으로 열린다
- 학생 quiz 목록에서는 이 회차의 quiz가 보이지 않아야 한다
- staff는 quiz를 볼 수 있어야 한다

## 운영 시나리오

1. 본문 먼저 공개
2. 퀴즈는 강의 직후 별도 공개
3. 플랫폼 UI에서 나중에 quiz `is_published`를 다시 열어도 된다

## 참고

이 회차는 GitHub source에서 `published: false`가 quiz 레벨에 들어간 예시다.
