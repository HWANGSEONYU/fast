#클로저

```swift
//public func sorted(by areInIncreasingOrder:(Element, Element) ->Bool) -> [Element]

let names:[String] = ["aaa", "bbb", "ccc", "ddd"]

func backwards(first:String, second:String) -> Bool {
    print("\(first) \(second) 비교중")
    return first > second
}

let reversed:[String] = names.sorted(by:backwards)
print(reversed)

let reversed2:[String] = names.sorted(by: { (first:String, second:String) -> Bool in
    return first > second
})
print(reversed2)

//후행 클로저(Trailing Closure) : 맨 마지막 전달인자로 전달되는 클로저에만 해당. 소괄호를 닫은 후 작성해도 됨
let reversed3:[String] = names.sorted(){ (first:String, second:String) -> Bool in
    return first > second
}
//이 메서드 처럼 단 하나의 클로저만 전달인자로 전달하는 경우에는 소괄호도 생략할 수 있음
let reversed4:[String] = names.sorted{ (first:String, second:String) -> Bool in
    return first > second
}

//문맥을 통한 타입유추로 타입을 생략할 수 있음
let reversed5:[String] = names.sorted{ (first, second) in
   return first > second
}

// 단축 인자 이름
let reversed6:[String] = names.sorted {
    return $0 > $1
}
print(reversed6)

//암시적 반환 표현
let reversed7:[String] = names.sorted{ $0 > $1}
print(reversed7)

//연산자는 일종의 함수. 
//연산자 정의
//public func > <T:Comparable>(lhs:T, rhs:T) -> Bool

//클로저로서의 연산자 함수 사용
let reversed8:[String] = names.sorted{by: > }
```

