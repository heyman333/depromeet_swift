## DeproMeet Swift study

###WEAK1

디프만 Swift Study를 시작해볼까요?   
디프만? [디프만 홈페이지 바로가기](http://www.depromeet.com/)


Swift만의 기본적이지만 특이한 문법을 조금 알아봅시다

* 자료형 선언 

```swift
var a = 'foo' // 변수를 담을 수 있죠?
let b = 'pee'// 상수만 담을 수 있죠

var a: Int = 100 // 스위프는 자료형을 : 뒤에 명시해 주네요(타입 어노테이션)
let b: String = "constant" // 문자열은 ' '도 되고 " " 도 됩니다. ;은 option!
```
1. 변수는 `var`에다가! 상수는 `let`에다가!   
2. 자료형을 명시해 줄 때는 name 뒤에 : 을 붙이고 명시 해 줍니다   
3. 세미콜론은 ``option``입니다   
4. 타입어노테이션도 사실 ``option``이지만 일치하지 않은 타입을 할당하려고 하는 경우 ``warning``을 준다는 점에서 활용하면 좋을 것 같네요

* 문자열삽입(Interpolate) 

```swift
let name: String = "youngsoo"
let age: Int = 27 // ㅠㅠ
let introduce: String = "\(name) is \(age) years old"
```
이건 뭐 굳이 설명을 적지 않아도... 좋은 기능입니다 ㄷㄷ   

* switch문 

```swift

var statusCode: Int = 404
var errMSG: String = "Calm and Check this errMsg : "

switch statusCode {
case 100, 101:
    errMSG += "Informational, 1.xx"
case 204:
    errMSG += "Successful. but no contents"
case 300...307:
    errMSG += "Redirecton. 3.xx"
case 400...417:
    errMSG += "Client error. 4.xx"
default:
    errMSG = "I don't know why this error comes up :("
}
	
```
1.`case`문 안에서 `...`키워드를 통해 범위를 지정해 줄 수 있네요(Int형)
