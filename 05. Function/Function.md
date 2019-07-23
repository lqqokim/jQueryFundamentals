# __05. 함수__
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
- 일반 함수 정의는 함수 호출 시 호이스팅 기술을 지원한다.
- 그러나 익명 함수 선언 참조 방식은 호이스팅을 지원하지 않는다.
- 호이스팅을 적용하면 함수 정의문보다 호출문이 먼저 나와도 함수 정의문을 끌어올려 함수를 호출한다.
## 함수 스코프 개념
### 함수 스코프란?
- 스코프(Scope)의 사전적인 의미는 '범위'이며, 여기에서는 변수 또는 함수의 유효범위를 가리킨다. 
- 스코프를 이해하기 위해서는 지역 변수(Local Variable)와 전역 변수(Global Variable)의 개념과 차이를 알아야한다.

### 전역 변수와 지역 변수의 개념과 차이
- 전역 변수는 자바스크립트 어디에서든 사용할 수 있는 변수
- 지역 변수는 함수 스코프에서만 사용할 수 있는 변수
```js
var score = 10;

function myFunc() {
    var score = 50;
    console.log(score); //50
}

myFunc();
console.log(score); //10
```

### 전역 함수와 지역 함수의 차이
- 전역 함수는 자바스크립트 어디에서든 사용할 수 있는 함수
- 지역 함수는 함수 스코프에서만 사용할 수 있는 함수
```js
function myFunc() {
    
}

function outerFunc() {
    function myFunc() {

    }
    myFunc(); //지역 함수 호출
}

outerFunc();
myFunc(); //전역 함수 호출
```