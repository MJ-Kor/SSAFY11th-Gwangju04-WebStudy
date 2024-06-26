## Functions

> 단일행 함수

- 숫자, 문자, 날짜 ,변환형, NUll 관련..

> 다중행 함수

- 집계 함수
- 윈도우 함수

> 숫자 관련 함수

- ABS(숫자) - 절대값
- CEILING(숫자) - 올림
- FLOOR(숫자) -  내림
- ROUND(숫자, 자릿수) - 숫자를 자릿수까지 반올림
- TRUNCATE(숫자, 자릿수) - 숫자를 자릿수까지 버림
- POW(X, Y) - X의 Y승
- MOD(분자, 분모) - 분자를 분모로 나눈 나머지
- GREATEST(숫자1, 숫자2, 숫자3,  …) - 주어진 수에서 가장 큰 수를 반환
- LEAST(숫자1, 숫자2, 숫자3,  …) - 주어진 수에서 가장 작은 수를 반환

> 문자 관련 함수

- ASCII(문자) - 문자의 아스키 코드 값 리턴
- CONCAT(’문자열1’, ’문자열2’, ’문자열3’, …) - 문자열들을 결합
- INSERT(’문자열’, 시작위치, 길이, ‘새로운 문자열’) - 문자열의 시작위치부터 길이만큼 새로운 문자열로 대치
- REPLACE(’문자열’, ‘기존 문자열’, ‘바뀔 문자열’) - 문자열 중 기존 문자열을 바뀔 문자로 변경
- INSTR(’문자열’, ‘찾는 문자열’) - 문자열 중 찾는 문자열의 위치 값을 리턴
- MID(’문자열’, 시작위치, 개수) - 문자열 중 시작위치부터 개수만큼 리턴
- SUBSTRING(’문자열’, 시작위치, 개수) - 문자열 중 시작위치부터 개수만큼 리턴
- LTRIM(’문자열’) - 문자열 중 왼쪽의 공백을 제거
- RTRIM(’문자열’) - 문자열 중 오른쪽의 공백을 제거
- TRIM(’문자열’) - 양쪽 모두의 공백을 제거
- LCASE(’문자열’) or LOWER(’문자열’) - 모든 문자를 소문자로 변경
- UCASE(’문자열’) or UPPER(’문자열’) - 모든 문자를 대문자로 변경
- LEFT(’문자열’, 개수) - 문자열 중에서 왼쪽에서 개수만큼 추출
- RIGHT(’문자열’, 개수) - 문자열 중에서 오른쪽에서 개수만큼 추출
- REVERSE(’문자열’) - 문자열을 반대로 나열
- LENGTH(’문자열’) - 문자열의 길이

> 날짜 관련 함수

- NOW(), SYSDATE(), CURRENT_TIMESTAMP - 현재 날짜와 시간 리턴
    - now(), current_timestamp() - select가 실행되는 순간
    - sysdate() - 함수가 호출될 때의 시간
- CURDATE() or CURRENT_DATE()  - 현재 날짜 리턴
- CURTIME() or CURRENT_TIME()  - 현재 시간 리턴
- DATE_ADD(날짜, INTERVAL 값 DAY/MONTH/YEAR) - 날짜에서 기준값 만큼 더한다
- DATE_SUB(날짜, INTERVAL 값 DAY/MONTH/YEAR) - 날짜에서 기준값 만큼 뺀다
- YEAR(날짜) - 날짜의 연도 리턴
- MONTH(날짜) - 날짜의 월 리턴
- MONTHNAME(날짜) - 날짜의 월을 영어로 리턴
- DAYNAME(날짜) - 날짜의 요일을 영어로 리턴
- DAYOFMONTH(날짜) - 날짜의 월별 일자 리턴
- DAYOFWEEK(날짜) - 날짜의 주별 일자 리턴 [일요일(1), 월요일(2), … , 토요일(7)]
- WEEKDAY(날짜) - 날짜의 주별 일자 리턴 [월요일(0), … , 토요일(5), 일요일(6)]
- DAYOFYEAR(날짜) - 일년을 기준으로 한 날짜까지의 일 수. (365일중 X일)
- WEEK(날짜) - 일년 중 몇 번째 주
- FROM_DAYS(날수) - 00년 00월 00일부터 날 수 만큼 경과한 날의 날짜 리턴
- TO-DAYS(날짜) - 00년 00월 00일부터 날짜까지의 일자 수 리턴
- DATE_FORMAT(날짜, ‘형식’) - 날짜를 형식에 맞게 리턴

> 날짜 형식

- %Y - 년 - 2020

- %y - 년 - 20

- %b - 월 - Jan, … , Dec

- %M - 월, Januaray, … , December

- %m - 월 - 01, 02, …, 11, 12

- %d - 일 - 00, 01, 02, …, 30, 31

- %e - 일 - 0, 1, 2, …, 30, 31

- %a - 요일 - Sun, …, Sat

- %W - 요일 - Sunday, …, Saturday

- %w - 요일 - 0, 1, 2, …, 6

- %p - AM or PM

- %H - 시간 - 01, 02, …, 22, 23

- %h - 시간 - 01, 02, …, 11, 12

- %l - 시간 - 01, 02, …, 11, 12

- %k - 시간 - 01, 02, …, 22, 23

- %I - 시간 - 1, 2, …, 11, 12

- %T - 시간 - 24-hour ( hh:mm:ss)

- %i - 분 - 00, …, 59

- %S - 초 - 00, …, 59

- %s - 초 - 00, …, 59
- %j - 1년중 x일,001, 002, … 365

> 논리 관련 함수

- IF(논리식, 값1, 값2) - 논리식이 참이면 값1이 리턴, 거짓이면 값2 리턴
- IFNULL(값1, 값2) - 값1이 NULL이면 값2로 대치, NULL이 아니면 값1리턴
- NULLIF(값1 ,값2) - 값1 = 값2이 TRUE이면 NULL, 그렇지 않으면 값1이 리턴