# MyPlayground

//: Playground - noun: a place where people can play

import UIKit
print("+++++ +++++")
print("+++++ +++++")
print("+++++ +++++")


var list = [1, 9, 4, 10, 5, 3]
list.sort()

var list2 = list.sort({
    (s1: Int, s2: Int) -> Bool in
    return s1 > s2
})
print(list2)

var list3 = list.sort() {$0 < $1}
print(list3)

var list4 = list.sort(<)
print(list4)

let len = {(name : String) -> Int in return name.characters.count}

func len(str: String) -> Int {
    
    return 0
}

let length = {
    (s: String?) -> Int in
    if let s1 = s?.characters.count {
        return s1
    }
    else {
        return 0
    }
}


class Human {
    var name: String?
    var isMan: Bool?
    var job: String?
	
	static var age = 0

	init(name: String, man: Bool) {
		self.name = name
		self.isMan = man
	}
	
	class func desc() {
		print("class func")
	}
}

print(Human.age)
Human.desc()

let h = Human(name: "Alex", man: true)
//let h2 = Human()

struct Animal {
	var type: String?
	var area: String?
}

let cat = Animal(type: "Cat", area: "Africa")

class A {
	var name: String = "Class A"
	init() {
		print("클래스 A가 생성됩니다.")
	}
	func foo() -> String {
		return "This is \(self.name)"
	}
}

class B : A {
	var prop = "Class B"
	override init() {
//		super.init()
		print("클래스 B가 생성됩니다.")
	}
	func boo() -> String {
		return "Class B Function"
	}
	override func foo() -> String {
		return "override \(self.prop)"
	}
}

let b = B()
print(b.foo())
print(b.name)

class Man {
	var birthYear : Int = 1970
	var age: Int {
		get {
			return 2015 - birthYear + 1
		}
	}
}
let m = Man()
print(m.age)

enum Country {
	case KOREA
	case USA
}

func setCountry(name: Country) {
	if name == Country.KOREA {
		print("KOREA")
	}
}


/////////////////////////////////////////////////////
class Person {
	var name : String = "Alex"
	var age : Int?
	var hobby : String?
	var sns : SNS? = SNS()
}
class SNS {
	var fb : FaceBook? = FaceBook()
	var tt : Twitter?
}
class FaceBook {
	var account : String = "sqlpro@naver.com"
}
class Twitter {
	var account : String = ""
}

//let p = Person()
//if let s = p.sns {
//	if let f = s.fb {
//		print("account=\(f.account)")
//	}
//}

//print(p.sns!.fb?.account)
//print(p.sns!.tt?.account)

let p : Person?
p = Person()
print(p?.name)
print(p!.name)

if let str = p?.name {
	print(str)
}

//////////////////





