변수)
var 변수명:자료형=초기값
var num :Int = 3

var 변수명:자료형? -> nil로 초기화
var num :Int?


상수)
let age = -3


엔터값추가)
print("My name is 반갑습니다.",terminator: "\n");

주석)
//
/**/

세미콜론)
있어도 되고 없어도 됨.

Int : 8byte
UInt : 32bit or 64bit
실수 : float, double

옵셔널타입)
var possibleNumber : Int? = 123
print(possibleNumber! + 10)

리턴타입 있는 함수)
func sayHello(personName : String) -> String {
    let greeting = "Hello, " + personName + "!"
    return greeting
}

print(sayHello("jang"),terminator:"")

외부인자이름 사용 함수)
func halfOpenRangeLength(start start : Int, end: Int) -> Int {
    return end - start
}

print(halfOpenRangeLength(start:5,end:10));

파라미터 없는 함수)
func sayHelloWorld() -> String {
    return "hello, world"
}

리턴타입 없는 함수)
func sayGoodbye(personName: String) {
    print("Goodbye, \(personName)!")
}

sayGoodbye("빅뱅") // Goodbye, 빅뱅! 출력



여러개의 값 리턴 함수)
func minMax(array: [Int]) -> (min: Int, max: Int) {
    
    var currentMin = array[0];
    var currentMax = array[1];
    for value in array[1..<array.count] {
        if value < currentMin {
            currentMin = value
        } else if value > currentMax {
            currentMax = value
        }
    }
    return (currentMin, currentMax)
}

let bounds = minMax([ 8, -6, 2, 109, 3, 71 ])
print("min is \(bounds.min) and max is \(bounds.max)") // min is -6 and max is 109
 
 
실전 앱소스 분석(다운로드 : https://github.com/shu223/iOS-9-Sampler)
 
- 오토레이아웃 설정 : width, height, trailing, leading 등
 
- 버튼과 소스상의 연결(IBOutlet)
 
- 테이블 뷰 구성.
 
- 뷰와 뷰컨트롤러