# 웹 개발 소개

## 웹은 어떻게 동작하는가?

웹은 **클라이언트-서버 모델**을 기반으로 동작합니다.

1. 사용자가 브라우저에서 URL을 입력합니다.
2. 브라우저(클라이언트)가 서버에 **HTTP 요청**을 보냅니다.
3. 서버가 요청을 처리하고 **HTML, CSS, JavaScript** 파일을 응답합니다.
4. 브라우저가 응답을 받아 화면에 렌더링합니다.

## 프론트엔드 vs 백엔드

| 구분 | 프론트엔드 | 백엔드 |
|------|-----------|--------|
| 역할 | 사용자가 보는 화면 | 데이터 처리, 비즈니스 로직 |
| 언어 | HTML, CSS, JavaScript | Python, Java, Node.js 등 |
| 실행 위치 | 브라우저 | 서버 |

## 개발 환경 설정

### 필요한 도구

- **텍스트 에디터**: VS Code (추천)
- **웹 브라우저**: Chrome 또는 Firefox
- **터미널**: 기본 내장 터미널

### VS Code 설치

1. [code.visualstudio.com](https://code.visualstudio.com)에서 다운로드합니다.
2. 운영체제에 맞는 버전을 설치합니다.
3. 추천 확장 프로그램을 설치합니다:
   - **Live Server** - 실시간 미리보기
   - **Prettier** - 코드 포맷팅
   - **HTML CSS Support** - 자동완성

## 첫 번째 웹 페이지 만들기

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>나의 첫 웹 페이지</title>
</head>
<body>
    <h1>안녕하세요!</h1>
    <p>나의 첫 번째 웹 페이지입니다.</p>
</body>
</html>
```

위 코드를 `index.html` 파일로 저장하고 브라우저에서 열어보세요.

## 핵심 정리

- 웹은 클라이언트-서버 모델로 동작한다.
- 프론트엔드는 HTML, CSS, JavaScript로 구성된다.
- VS Code와 Live Server를 사용하면 편리하게 개발할 수 있다.
