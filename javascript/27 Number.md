# 27. Number

표준 빌트인 객체로, 원시 타입 숫자를 다룰 때 유용한 프로퍼티와 메서드를 제공한다. 

## ✔️ 생성자 함수

`new` 연산자와 호출시 [[NumberData]] 내부 슬롯에 인수로 전달받은 숫자를 할당한 **Number 래퍼 객체 생성.**

## ✔️ 프로퍼티

|  | 설명 |
| --- | --- |
| Number.EPSILON | 1과 1보다 큰 숫자 중에서 가장 작은 숫자와의 차이. ⇒ 부동소수점으로 인해 발생하는 오차 해결 |
| Number.MAX_VALUE | 가장 큰 양수 값. MAX: Infinity |
| Number.MIN_VALUE | 가장 작은 양수 값. MIN: 0 |
| Number.MAX_SAFE_INTEGE | 가장 큰 정수값 |
| Number.MIN_SAFE_INTEGER | 가장 작은 정수값 |
| Number.POSITIVE_INFINITY | 양의 무한대 |
| Number.NEGATIVE_INFINITY | 음의 무한대 |

## ✔️ 메서드

- `Number.isFinite()`
    
    인수로 전달된 값이 정상적인 **유한수인지 판별하여 `boolean` 값을 반환.** 빌트인 전역함수 isFinite와 다르게 **숫자로 ~~암묵적 타입 변환~~을 하지 않는다.** 
    
- `Number.isInteger()`
    
    인수로 전달된 값이 **정수인지 판별하여 `boolean` 값을 반환.** ~~**암묵적 타입 변환**~~을 하지 않는다.
    
- `Number.isNaN()`
    
    인수로 전달된 값이 **NaN인지 판별한 후 `boolean` 값으로 반환. isNaN과 다르게 ~~암묵적 타입 변환~~을 하지 않는다.**
    
- `Number.isSafeInteger()`
    
    **안전한 정수인지 검사**하여 `**boolean` 값을 반환.**
    

### ∙`prototype`

- `Number.prototype.toExponential()`
    
    **숫자를 지수 표기법으로 변환**하여 `**stirng` 값을 반환.** **그룹 연산자(`().toExponential()`)** 사용을 권한다. 
    
- `Number.prototype.toFixed()`
    
    소수점 이하 자릿수(0~20) 사이의 정수값을 인수로 전달하여, **반올림한 숫자**를 `**string**` **값으로 반환.**
    
- `Number.prototype.toPrecision()`
    
    전체 자릿수(0~21)까지 유효하도록 **나머지 자릿수를 반올림해서 `string`으로 반환.**
    
- `Number.prototype.toString()`
    
    **숫자를 `string` 값으로 반환.** 2~36 사이의 정수값을 인수로 전달 가능.