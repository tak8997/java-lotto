# 로또
## 요구사항
- 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
- 로또 1장의 가격은 1000원이다.

## 우승조건
|등수|개수(개)|우승금액(원)|
|----|---|-----|
|1등|6|2000000000|
|2등|5|1500000|
|3등|4|50000|
|4등|3|5000|

## 기능정리 
1. 금액을 입력합니다.
2. 금액에 구매할 수 있는 로또 개수를 반환합니다.
3. 입력한 개수만큼의 로또(로또 티켓)을 받습니다.
3-1. 당첨 로또의 번호를 생성합니다. 
4. 로또티켓의 당첨결과를 확인합니다.
---


## 기능정리
- [x] 번호 (Ball)
    - [x] 동등성, 동일성 확인한다.
    - [x] 1보다 작으면 안된다.
    - [x] 45보다 크면 안된다.
- [x] 로또 번호 (Lotto)
    - [x] 6개로 이루어진 로또 번호를 생성한다.
    - [x] 로또 번호가 일치하는 개수를 반환
    - [x] 로또 구매 가능 갯수 반환
- [x] 랭킹 (Rank)
- [x] 로또 티켓 (LottoTicket)
- [x] 로또 생성 (LottoGenerator)
- [x] 로또 판매점 (LottoMachine)
- [x] 돈 (Money)


```
구입금액을 입력해 주세요.
14000
14개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[23, 25, 33, 36, 39, 41]
[1, 3, 5, 14, 22, 45]
[5, 9, 38, 41, 43, 44]
[2, 8, 9, 18, 19, 21]
[13, 14, 18, 21, 23, 35]
[17, 21, 29, 37, 42, 45]
[3, 8, 27, 30, 35, 44]

지난 주 당첨 번호를 입력해 주세요.
1, 2, 3, 4, 5, 6

당첨 통계
---------
3개 일치 (5000원)- 1개
4개 일치 (50000원)- 0개
5개 일치 (1500000원)- 0개
6개 일치 (2000000000원)- 0개
총 수익률은 0.35입니다.(기준이 1이기 때문에 결과적으로 손해라는 의미임)
```

---

# 문자열 덧셈 계산기
## 요구사항 
- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환
(예: “” => 0, "1,2" => 3, "1,2,3" => 6, “1,2:3” => 6)
- 앞의 기본 구분자(쉼표, 콜론)외에 커스텀 구분자를 지정할 수 있다. 
커스텀 구분자는 문자열 앞부분의 “//”와 “\n” 사이에 위치하는 문자를 커스텀 구분자로 사용한다. 
예를 들어 “//;\n1;2;3”과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 문자열 계산기에 숫자 이외의 값 또는 음수를 전달하는 경우 RuntimeException 예외를 throw 한다.
 
- [x] 입력받은 문자열을 분할 한다.  
    - [x] 문자열이 empty 인 경우 0 Return 
    - [x] default : , or : 이다.
    - [x] 커스텀 구분자를 사용하는 경우 (begin://)(end:\n)
- [x] 입력받은 String 의 합계를 구한다.

