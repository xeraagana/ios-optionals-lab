# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```

```

var userNameOne: String? = "Test User"
var validUserNameOne: String = "Test User"
//var declarationOfName: String? = "The username"
if let validUserNameOne = userNameOne {
//    let words = declarationOfName {
    print("The user name is \(validUserNameOne)")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).



```swift
var userNameTwo: String? = nil
```
```
var userNameOne: String? = "Test User"
var userNameTwo: String? = nil
//var declarationOfName: String? = "The username"
    print("The user name is \((userNameTwo) ?? "undefined")")
```    

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10

```
```

var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
var area: Double

if let rect1Height = rectOneWidth {
     if let rect1Width = rectOneHeight {
         area = rect1Height * rect1Width
                   print("the area of rectOne is \(area)")
    }
        
}
```
b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
```
```
var area: Double
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
if let rect2Height = rectTwoWidth,
   let rect2Width = rectTwoHeight {
         area = rect2Height * rect2Width
    print("the area of rectOne is \(area)")
     }else{
    print("The are of rectTwo is not able to be calculated")
    }
```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```
```
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70

if let name = userOneName,
    let age = userOneAge,
    let height = userOneHeight {
    let formatedString = String(format: "%.1f", height / 12)
    print("hello \(name)! you are \(age) years old and \(formatedString) feet tall ")
}
```
b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```
```
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil

if let name = userTwoName,
    let age = userTwoAge,
    let height = userTwoHeight {
    print("hello \(name)! you are \(age) years old and \(height) feet tall ")
}else {
    print("Hello \(userTwoName ?? "user"),  You are \( userTwoAge ?? 4) years old and I don't know how tall you are")
}
```
## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
```
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
if let num = favoriteNumber{
print("Your favorite number is \(num)")
}else{
    print("i dont know what your favorite number is")
}
````

## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```
```
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
if let one = numOne,
    let  two = numTwo,
    let three = numThree {
    let variableSum = one + two + three

print("the sum or all numbers is \(variableSum)")
}else{
    print("the sum is Zero")
}
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
