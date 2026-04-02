# HTML 기초

## 시맨틱 태그

시맨틱 태그는 콘텐츠의 **의미**를 명확히 전달하는 HTML 태그입니다.

```html
<header>사이트 상단</header>
<nav>내비게이션</nav>
<main>
    <article>
        <section>섹션 1</section>
        <section>섹션 2</section>
    </article>
    <aside>사이드바</aside>
</main>
<footer>사이트 하단</footer>
```

### 주요 시맨틱 태그

| 태그 | 용도 |
|------|------|
| `<header>` | 페이지 또는 섹션의 머리글 |
| `<nav>` | 내비게이션 링크 |
| `<main>` | 문서의 주요 콘텐츠 |
| `<article>` | 독립적인 콘텐츠 |
| `<section>` | 주제별 그룹 |
| `<aside>` | 부가 정보 |
| `<footer>` | 바닥글 |

## 폼 (Form)

사용자로부터 데이터를 입력받는 요소입니다.

```html
<form action="/submit" method="POST">
    <label for="name">이름:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">이메일:</label>
    <input type="email" id="email" name="email" required>

    <label for="message">메시지:</label>
    <textarea id="message" name="message" rows="4"></textarea>

    <label>
        <input type="checkbox" name="agree"> 약관에 동의합니다.
    </label>

    <button type="submit">전송</button>
</form>
```

### input 타입

- `text` - 일반 텍스트
- `email` - 이메일 (형식 검증)
- `password` - 비밀번호
- `number` - 숫자
- `date` - 날짜
- `file` - 파일 업로드
- `checkbox` - 체크박스
- `radio` - 라디오 버튼

## 테이블

```html
<table>
    <thead>
        <tr>
            <th>이름</th>
            <th>나이</th>
            <th>직업</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>김철수</td>
            <td>28</td>
            <td>개발자</td>
        </tr>
        <tr>
            <td>이영희</td>
            <td>25</td>
            <td>디자이너</td>
        </tr>
    </tbody>
</table>
```

## 핵심 정리

- 시맨틱 태그를 사용하면 접근성과 SEO가 향상된다.
- `<form>`으로 사용자 입력을 수집할 수 있다.
- `<table>`로 표 형태의 데이터를 표시할 수 있다.
