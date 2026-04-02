# 실전 프로젝트: 포트폴리오 사이트

## 프로젝트 개요

지금까지 배운 HTML, CSS, JavaScript를 활용하여 개인 포트폴리오 사이트를 만들어봅니다.

### 구현 기능

- 반응형 네비게이션 바
- 자기소개 섹션
- 프로젝트 카드 갤러리 (Grid 레이아웃)
- 연락처 폼
- 스크롤 시 네비게이션 하이라이트

## 1단계: HTML 구조

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>나의 포트폴리오</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <div class="nav-brand">Portfolio</div>
        <ul class="nav-links">
            <li><a href="#about">소개</a></li>
            <li><a href="#projects">프로젝트</a></li>
            <li><a href="#contact">연락처</a></li>
        </ul>
    </nav>

    <main>
        <section id="about" class="section">
            <h1>안녕하세요, 웹 개발자입니다.</h1>
            <p>HTML, CSS, JavaScript를 활용하여 웹 서비스를 만듭니다.</p>
        </section>

        <section id="projects" class="section">
            <h2>프로젝트</h2>
            <div class="project-grid">
                <article class="project-card">
                    <h3>프로젝트 1</h3>
                    <p>투두 리스트 앱</p>
                </article>
                <article class="project-card">
                    <h3>프로젝트 2</h3>
                    <p>날씨 대시보드</p>
                </article>
                <article class="project-card">
                    <h3>프로젝트 3</h3>
                    <p>블로그 플랫폼</p>
                </article>
            </div>
        </section>

        <section id="contact" class="section">
            <h2>연락처</h2>
            <form class="contact-form">
                <input type="text" placeholder="이름" required>
                <input type="email" placeholder="이메일" required>
                <textarea placeholder="메시지" rows="5" required></textarea>
                <button type="submit">전송</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 My Portfolio</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

## 2단계: CSS 스타일링

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    line-height: 1.6;
    color: #333;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background: #1a1a2e;
    color: white;
    position: sticky;
    top: 0;
    z-index: 100;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-links a {
    color: white;
    text-decoration: none;
}

.section {
    padding: 4rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
}

.project-card {
    padding: 2rem;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.contact-form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    max-width: 500px;
    margin-top: 2rem;
}

.contact-form input,
.contact-form textarea {
    padding: 0.75rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 1rem;
}

.contact-form button {
    padding: 0.75rem;
    background: #1a1a2e;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

footer {
    text-align: center;
    padding: 2rem;
    background: #f5f5f5;
    color: #666;
}
```

## 3단계: JavaScript 인터랙션

```javascript
// 폼 전송 처리
const form = document.querySelector('.contact-form');
form.addEventListener('submit', (e) => {
    e.preventDefault();
    alert('메시지가 전송되었습니다!');
    form.reset();
});

// 스크롤 시 네비게이션 하이라이트
const sections = document.querySelectorAll('.section');
const navLinks = document.querySelectorAll('.nav-links a');

window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
        const top = section.offsetTop - 100;
        if (scrollY >= top) {
            current = section.getAttribute('id');
        }
    });
    navLinks.forEach(link => {
        link.style.fontWeight = link.getAttribute('href') === `#${current}` ? 'bold' : 'normal';
    });
});
```

## 과제 안내

위 코드를 기반으로 **본인만의 포트폴리오 사이트**를 완성하세요.

### 필수 요구사항
- 반응형 레이아웃 (모바일/태블릿/데스크톱)
- 최소 3개의 프로젝트 카드
- 작동하는 연락처 폼

### 추가 도전 과제
- 다크 모드 토글
- 스무스 스크롤
- CSS 애니메이션 (fade-in, slide-up 등)
