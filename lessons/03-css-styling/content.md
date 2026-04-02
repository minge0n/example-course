# CSS 스타일링

## CSS 선택자

CSS 선택자는 스타일을 적용할 HTML 요소를 지정합니다.

```css
/* 태그 선택자 */
h1 { color: navy; }

/* 클래스 선택자 */
.highlight { background: yellow; }

/* ID 선택자 */
#header { font-size: 24px; }

/* 자식 선택자 */
.card > .title { font-weight: bold; }

/* 가상 클래스 */
a:hover { text-decoration: underline; }
button:disabled { opacity: 0.5; }
```

## 박스 모델

모든 HTML 요소는 **박스 모델**로 구성됩니다.

```
┌─────────────── margin ───────────────┐
│ ┌──────────── border ──────────────┐ │
│ │ ┌────────── padding ──────────┐  │ │
│ │ │                             │  │ │
│ │ │         content             │  │ │
│ │ │                             │  │ │
│ │ └─────────────────────────────┘  │ │
│ └──────────────────────────────────┘ │
└──────────────────────────────────────┘
```

```css
.box {
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    margin: 16px;
    box-sizing: border-box; /* padding과 border를 width에 포함 */
}
```

## Flexbox

1차원 레이아웃(가로 또는 세로)에 적합합니다.

```css
.container {
    display: flex;
    justify-content: space-between; /* 가로 정렬 */
    align-items: center;            /* 세로 정렬 */
    gap: 16px;                      /* 요소 간 간격 */
}

.item {
    flex: 1; /* 균등 분배 */
}
```

### justify-content 옵션

- `flex-start` - 시작점 정렬
- `flex-end` - 끝점 정렬
- `center` - 중앙 정렬
- `space-between` - 양 끝 정렬, 사이 균등
- `space-around` - 요소 주변 균등 간격

## Grid

2차원 레이아웃(가로 + 세로)에 적합합니다.

```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3열 균등 */
    grid-template-rows: auto;
    gap: 20px;
}

/* 특정 요소가 2칸 차지 */
.wide {
    grid-column: span 2;
}
```

## 반응형 디자인

미디어 쿼리를 사용하여 화면 크기에 따라 스타일을 변경합니다.

```css
/* 모바일 우선 */
.grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
}

/* 태블릿 (768px 이상) */
@media (min-width: 768px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* 데스크톱 (1024px 이상) */
@media (min-width: 1024px) {
    .grid {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

## 핵심 정리

- CSS 선택자로 원하는 요소를 정확히 지정할 수 있다.
- `box-sizing: border-box`를 사용하면 레이아웃 계산이 쉬워진다.
- Flexbox는 1차원, Grid는 2차원 레이아웃에 적합하다.
- 미디어 쿼리로 반응형 디자인을 구현할 수 있다.
