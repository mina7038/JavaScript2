# JavaScript2

## ✅ 함수(Function)의 개념

- 자판기처럼 **입력(동전, argument)**을 넣으면 **출력(결과)**이 나오는 구조
- **중간 과정**은 몰라도 되고, **결과만 알면 됨**
- 한 번 정의해 놓으면 **필요할 때마다 호출해서 재사용 가능**

```jsx
function test() {
  document.write("안녕하세요");
}
test(); // 호출
```

## ✅ 함수를 사용하는 이유

- **코드 재사용성**
- **유지보수 용이성**
- **가독성 향상**

## ✅ 함수 작성 방법

### 1. 함수 선언문

```jsx
function foo() {
  console.log("call foo");
}
foo();
```

### 2. 함수 표현식

```jsx
const bar = function() {
  console.log("call bar");
};
bar();
```

### 3. 함수 생성자

```jsx
const add = new Function('a', 'b', 'return a + b');
add(4, 5); // 9
```

## ✅ return 문

- 함수에서 **결과 값을 돌려줄 때 사용**
- `return` 이후 실행문은 **더 이상 실행되지 않음**

```jsx
function calc() {
  const result = 100 + 200;
  return result;
}

console.log(calc()); // 300
```

## ✅ 매개변수(parameter) vs 전달인자(argument)

| 용어 | 설명 | 예시 |
| --- | --- | --- |
| 매개변수 | 함수 선언 시 입력받는 변수 | `function f(x, y)` |
| 전달인자 | 함수를 호출할 때 넘기는 실제 값 | `f(3, 4)` |

✔ 매개변수(parameter)는 함수 정의 시

✔ 전달인자(argument)는 함수 호출 시

## ✅ 함수의 종류

### 1. 내장 함수

- 함수 안에 또 다른 함수를 정의

```jsx
function outer() {
  const a = 1;

  function inner() {
    const b = 100;
    console.log(a); // 외부 변수 접근 가능
    console.log(b);
  }

  inner();
}
outer();
```

### 2. 콜백 함수

- 함수의 **매개변수로 전달되는 함수**
- 주로 **비동기 처리**나 **반복 처리**에 사용

```jsx
const arr = ["사과", "바나나", "토마토"];
arr.forEach(function(element, index) {
  console.log(index + " : " + element);
});
```

### 3. 재귀 함수

- 함수가 **자기 자신을 호출하는 구조**

```jsx
function factorial(n) {
  if (n === 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```
