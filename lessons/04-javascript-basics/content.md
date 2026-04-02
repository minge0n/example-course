# JavaScript 기초

## 변수 선언

```javascript
// const: 재할당 불가 (기본으로 사용)
const name = "Alice";
const PI = 3.14159;

// let: 재할당 가능
let count = 0;
count = count + 1;

// var: 사용하지 않음 (레거시)
```

## 자료형

```javascript
// 문자열
const greeting = "안녕하세요";
const template = `이름: ${name}`;  // 템플릿 리터럴

// 숫자
const age = 25;
const price = 9.99;

// 불리언
const isActive = true;

// 배열
const fruits = ["사과", "바나나", "포도"];
fruits.push("딸기");       // 추가
console.log(fruits[0]);    // "사과"
console.log(fruits.length); // 4

// 객체
const user = {
    name: "Alice",
    age: 25,
    isStudent: true,
};
console.log(user.name);    // "Alice"
```

## 함수

```javascript
// 함수 선언
function add(a, b) {
    return a + b;
}

// 화살표 함수 (권장)
const multiply = (a, b) => a * b;

// 기본값 파라미터
const greet = (name = "World") => `Hello, ${name}!`;

console.log(add(2, 3));       // 5
console.log(multiply(4, 5));  // 20
console.log(greet());         // "Hello, World!"
console.log(greet("Alice"));  // "Hello, Alice!"
```

## 조건문과 반복문

```javascript
// if-else
const score = 85;
if (score >= 90) {
    console.log("A");
} else if (score >= 80) {
    console.log("B");
} else {
    console.log("C");
}

// for 반복
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// for...of (배열 순회)
const colors = ["red", "green", "blue"];
for (const color of colors) {
    console.log(color);
}

// 배열 메서드
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(n => n * 2);        // [2, 4, 6, 8, 10]
const evens = numbers.filter(n => n % 2 === 0); // [2, 4]
const sum = numbers.reduce((a, b) => a + b, 0); // 15
```

## DOM 조작

```javascript
// 요소 선택
const title = document.querySelector("h1");
const buttons = document.querySelectorAll(".btn");

// 내용 변경
title.textContent = "새로운 제목";

// 스타일 변경
title.style.color = "blue";

// 클래스 조작
title.classList.add("active");
title.classList.remove("hidden");
title.classList.toggle("selected");

// 이벤트 리스너
const button = document.querySelector("#myButton");
button.addEventListener("click", () => {
    alert("클릭되었습니다!");
});

// 요소 생성 및 추가
const newItem = document.createElement("li");
newItem.textContent = "새 항목";
document.querySelector("ul").appendChild(newItem);
```

## 핵심 정리

- `const`를 기본으로 사용하고, 재할당이 필요할 때만 `let`을 사용한다.
- 화살표 함수(`=>`)를 사용하면 코드가 간결해진다.
- `map`, `filter`, `reduce`로 배열을 선언적으로 처리할 수 있다.
- `querySelector`와 `addEventListener`로 DOM을 조작할 수 있다.
