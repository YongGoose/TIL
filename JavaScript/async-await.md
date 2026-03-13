# JavaScript async / await

## 개요

`async/await`는 Promise 기반 비동기 코드를 동기 코드처럼 읽기 쉽게 작성할 수 있는 ES2017 문법입니다.

## 기본 사용법

```javascript
// async 함수 선언
async function fetchData(url) {
  const response = await fetch(url);
  const data = await response.json();
  return data;
}

fetchData('https://api.example.com/items')
  .then(data => console.log(data));
```

## 에러 처리

```javascript
async function fetchWithErrorHandling(url) {
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`HTTP error: ${response.status}`);
    }
    return await response.json();
  } catch (error) {
    console.error('요청 실패:', error.message);
  }
}
```

## 병렬 실행

```javascript
// 순차 실행 (느림)
const a = await fetchA();
const b = await fetchB();

// 병렬 실행 (빠름)
const [a, b] = await Promise.all([fetchA(), fetchB()]);
```

## Promise와 비교

```javascript
// Promise 체이닝
function getUser(id) {
  return fetch(`/users/${id}`)
    .then(res => res.json())
    .then(user => user.name);
}

// async/await (동일한 동작, 더 읽기 쉬움)
async function getUser(id) {
  const res = await fetch(`/users/${id}`);
  const user = await res.json();
  return user.name;
}
```

## 참고
- [MDN - async function](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/async_function)
- [MDN - await](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/await)
