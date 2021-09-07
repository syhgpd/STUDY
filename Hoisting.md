<br>

# Hoisting

#### 함수 안에 있는 선언들을 모두 끌어올려서 해당 함수 유효 범위의 최상단에 선언하는 것

<br>

``` JavaScript
var result = sum(1,3); 
var sum = function(num1, num2){
   return console.log(num1+num2);
}
```
##### 변형 전 코드
<br>

``` JavaScript
var result = undefined; 
var sum = undefined; 
result = sum(1,3); 
sum = function(num1, num2){
   return console.log(num1+num2);
}
```
##### 호이스팅(Hoisting)으로 인해 (내부적으로) 변형된 코드

<br>

### 호이스팅이란

- #### 자바스크립트 함수는 실행되기 전에 함수 안에 필요한 변수값들을 모두 모아서 유효 범위의 최상단에 선언한다
  + ##### 함수 블록 안에서 유효하다

- #### 함수 내에서 아래쪽에 존재하는 내용 중 필요한 값들을 끌어올리는 것이다

  + ##### 실제로 코드가 끌어올려지는 것은 아니며, 내부적으로 끌어올려서 처리하는 것이다

  + ##### 실제 메모리에서는 변화가 없다

  <br>

### 호이스팅의 대상

- #### var 변수 선언과 함수선언문에서만 호이스팅이 일어난다.
- #### 호이스팅은 함수선언문과 함수표현식에서 서로 다르게 동작하기 때문에 주의해야 한다.

<br>

### 함수 선언문에서의 호이스팅

- #### 함수선언문은 코드를 구현한 위치와 관계없이 자바 스크립트의 특징은 호이스팅에 따라 브라우저가 자바스크립트를 해석할 때 맨 위로 끌어 올려진다.

<br>

### 함수 표현식에서의 호이스팅

- #### 함수표현식은 함수선언문과 달리 선언과 호출 순서에 따라서 정상적으로 함수가 실행되지 않을 수 있다
  + ##### 함수 표현식에서는 선언과 할당의 분리가 발생한다.

<br>

<span style="color:red">호이스팅(Hoisting)이 일어나면 가독성이 떨어지며 유지보수가 어려워져 발생하지 않도록 해야한다.</span>