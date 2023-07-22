# 29. Date

**날짜와 시간을 위한 메서드를 제공**하는 **빌트인 객체**이자 **생성자 함수.** 기술적 표기는 UTC, 시스템의 시계에 의해 현재 날짜와 시간이 정해진다. 

## ✔️ 생성자 함수

- `new Date()`
    
    `**Date` 객체를 반환**한다. 날짜/시간을 나타내는 정수값이며, 콘솔 출력시 정보가 나온다.
    
- `new Date(milliseconds)`
    
    밀리초만큼 경과한 날짜/시간을 나타내는 `**Date` 객체를 반환.**
    
- `new Date(dateString)`
    
    인수에 지정된 날짜/시간을 나타낸 **문자열 전달시 `Date` 객체를 반환.**
    
- `new Date(year, month[, daty, hour, minute, second, millisecond])`
    
    지정된 날짜/시간을 나타내는 `**Date` 객체를 반환.** 연, 월은 반드시 지정.
    

## ✔️ 메서드

- `Date.now()`
    
    현재 시간까지 경과한 밀리초를 `number`로 반환.
    
- `Date.parse()`
    
    인수로 전달된 시간까지 밀리초를 `number`로 반환.
    
- `Date.UTC()`
    
    UTC를 기점으로 지정 시간까지 밀리초를 `number` 로 반환
    
- `Date.prototype.**get**FullYear/Month/Date/DayHours/Minutes/Seconds/Milliseconds/Time/TimezoneOffset()`
    
    `Date` 객체의 연도/월/날짜/요일/시간/분/초/밀리초/UTC를 기점으로 경과된 밀리초/UTC와 지정된 로컬 시간과의 차이의 분 단위를 나타내는 정수 반환.
    
- `Date.prototype.**set**FullYear/Month/Date/DayHours/Minutes/Seconds/Milliseconds/Time()`
    
    `Date` 객체의 연도/월/날짜/요일/시간/분/초/밀리초/UTC를 기점으로 경과된 밀리초를 설정한다. 
    
- `Date.prototype.**to**DateString/TimeString/ISOString()`
    
    `Date` 객체 {날짜}/{시간}/{ISO 8601 형식인 날짜와 시간}을 `string` 값으로 반환.
    
- `Date.prototype.**toLocale**String/TimeString()`
    
    인수로 전달된 로컬을 기준으로 `Date` 객체의 {날짜와 시간}/{시간}을 `string` 값으로 반환. 
    
    인수 예: ‘ko-KR’, ‘en-US’, ‘ja-JP’