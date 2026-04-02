# 예약 공개 회차

이 회차는 `published: true`지만 `available_from`이 미래 시점으로 설정되어 있습니다.

## 기대 동작

- staff는 회차와 quiz를 확인할 수 있다
- 학생은 회차 상세, asset, quiz 모두 접근 차단된다
- 시간이 지나 `available_from` 이후가 되면 공개된다

## 운영 메모

실제 수업에서는 사전 오픈을 막고 싶을 때 이 패턴을 사용합니다.

## asset

- 일정 다이어그램: `assets/release-window.svg`
