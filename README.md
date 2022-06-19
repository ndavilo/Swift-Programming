# Swift-Programming
Swift Programming notes
Variables =>
		var str = “hello world”
		var a =2
Constant => 	let str = “hello world”
Constant cannot be reassigned but variables can.

Data Types:
String, Int, Float, Double, Bool.

var a:Int =2
converting data type => str = String(29) or str = String(a)

If statement =>
let a = 10
if a < 4 {
	print(‘a is less than 10)
}
else if a >4{
	code
}
else{
}

|| or 
&& and 

switch statement
repeat -while loop

Basic Function syntax:

func name(){
	some code 
}

func addme() -> Int{
    let c = 3
    return c
} 

For a single argument: 

func name(argumentLebal parameterName:Datatype){

}

func addme(arg a:Int) -> Int{
    let c = a
    return c
}
print(addme(arg: 4))

For multiple  argument: 

func name(argumentLebal parameterName:Datatype, argumentLebal parameterName:Datatype){

}

func addme(arg a:Int, arg b:Int) -> Int{
    let c = a + b
    return c
}
print(addme(arg: 4, arg: 5))

func addme(a:Int, b:Int) -> Int{
    let c = a + b
    return c
}
print(addme(a:4, b:5))

Class:
class name{

}

class Message{
    var user = ""
    var value = ""
    var date = ""
    var room = ""
}

let Message1 = Message()
Message1.user = "David"
Message1.value = "How are you doing?"
Message1.date = "16/May/2022"
Message1.room = "room1"
print(Message1.user)

let Message2 = Message()
Message2.user = "Adaugo"
Message2.value = "I am good and you?"
Message2.date = "17/May/2022"
Message2.room = "room1"
print(Message2.user)
print(Message2.room)

Inheritance:
import UIKit

class Car {
    var topspeed = 200
    
    func drive(){
        print("Driving at \(topspeed)")
    }
}

class Futurecar : Car {
    func fly() {
        print("Fly")
    }
}

var oldcar = Car()
oldcar.topspeed
oldcar.drive()

var newcar = Futurecar()
newcar.topspeed
newcar.drive()
newcar.fly()

Initializers:

import UIKit

class Person {
    var name = ""
    var age = 0
    
    init(n:String, a:Int) {
        name = n
        age = a
    }
}

var person1 = Person(n: "David", a: 30)
person1.name
person1.age

or

import UIKit

class Person {
    var name = ""
    var age = 0
    
    init(_ n:String, _ a:Int) {
        name = n
        age = a
    }
}

var person1 = Person("David", 30)
person1.name
person1.age

or

import UIKit

class Person {
    var name = ""
    var age = 0
    
    init(_ name:String, _ age:Int) {
        self.name = name
        self.age = age
    }
}

var person1 = Person("David", 30)
person1.name
person1.age

how to declare a variable without assigning values to it:
var title:String?
var day:Int?

title = "Hello"
day = 4

Arrays:
import UIKit

var animals = ["dog", "cat", "goat", "cow"]

animals[0]

for animal in animals {
    print("my " + animal)
}
How to create empty array: var birds = [String]()
How to add: 
birds = birds + ["chicken"]		
output ["chicken"]
animals += ["bird"]		
output  ["dog", "cat", "goat", "cow", "bird"]
or 
animals.append("sheep")	
output  ["dog", "cat", "goat", "cow", "bird", "sheep"]
or 
birds.append(contentsOf: animals)		
output ["chicken", "dog", "cat", "goat", "cow", "bird", "sheep"]

Removing index : birds.remove(at: 3)
Remove all: birds.removeAll()
animals.count
animals.sort()

Dictionaries:
Empty: var carDB = Dictionary<String, String>()
Or var carDB2 = [String:String]()

Adding values:
var animalsName = [String:String]()
animalsName["Dog"] = "Jack"
animalsName["Cat"] = "lucy"

animalsName 	output => ["Dog": "Jack", "Cat": "lucy"]

animalsName["Cat"] output => "lucy"

animalsName.count
animalsName.keys
