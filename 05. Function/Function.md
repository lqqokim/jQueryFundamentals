# __함수__
## 함수
### 기본 함수 정의문
#### 일반 함수 정의
```js
function 함수명() {
    //code
}
```
#### 익명 함수 정의
```js
참조변수 = function() {
    //code
}
```
#### 두 방식의 차이점
```js
//일반 함수 정의 방식 (정상 작동)
testFunc();

function testFunc() {
    //code
}

//익명 함수 선언 참조 방식(오류 발생)
testFunc();

var testFunc = function() {
    //code
}
```
## 함수 스코프 개념
### 함수 스코프란?
 - 스코프(Scope)의 사전적인 의미는 '범위'이며, 여기에서는 변수 또는 함수의 유효범위를 가리킨다. 
- 스코프를 이해하기 위해서는 지역 변수(Local Variable)와 전역 변수(Global Variable)의 개념과 차이를 알아야한다.

### 전역 변수와 지역 변수의 갸념과 차이
