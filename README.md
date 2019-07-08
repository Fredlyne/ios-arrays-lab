# Arrays lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`.

```
var array = ["orange", "red", "yellow", "turquoise", "lavender"]
var string = ("\(array[0]), \(array[2]), and \(array[3]) are some of my favorite colors")
print(string)

```

## Question 2

Remove "Illinois" and "Kansas" from the array below.

```var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]

westernStates.remove(at: 5)
westernStates.remove(at: 4)
print(westernStates)
```


## Question 3

Iterate through the array below. For each state, print out the name of the state, a colon, and whether it is or is not **in the continental United States.**

```let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]

for i in moreStates {
if i != "Hawaii"{
print( i + ": in continental US")
} else {
print( i + ": not in continental US" )
}
}
```


## Question 4

Print out how many non-whitespace characters are in `myString`:

```let myString = "This is good practice with Strings!"

var myString = "This is good practice with Strings!"

var new = myString.replacingOccurrences(of: " ", with: "")
print(new.count)
```

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

```let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]

for i in myFavoriteQuotes  {
print(i.replacingOccurrences(of: " ", with: "").count)
}
```

"
## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()


for i in garden where i == "\u{1f337}" {
basket.append(i)
}
print(garden.joined(separator: " ").replacingOccurrences(of: "\u{1f337}", with: "dirt").components(separatedBy: " "))
print("\(basket), \(basket.count) flowers are in my basket.")


```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

```var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]
battingLineup.append("Suzuki") //Add "Suzuki" to the end of your lineup.
battingLineup.remove(at: 1)//Change "Jeter" to "Tejada".
battingLineup.insert("Tejada", at: 1)
battingLineup.insert("Guerrerero", at: 5 )//Change "Thomas" for "Guerrero"
battingLineup.remove(at: 6)
battingLineup.append("Reyes") //Put "Reyes" to bat 8th instead.
print(battingLineup.dropFirst())
```


## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)


```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

var targetAppears = 0

for i in numbers {
if i == target {
targetAppears  += 1
}
}
if targetAppears > 0 {
print(true)
} else {
print(false)
}

//true
```

Ex. 2

```swift
let numbersTwo = [32459,2,4,5,1,4,2,1]
var targetTwo = 3
var targetTwoAppears = 0
for i in numbersTwo {
if i == targetTwo {
targetTwoAppears += 1
}
}
if targetTwoAppears > 0 {
print(true)
} else {
print(false)
}

//false
```


## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.

print(arrayOfNumbers.sorted().last!)
```


## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
print(arrayOfNumbers.sorted().first!)

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
```


## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

```var secondListOfNumbers = [19,13,14,19,101,10000,141,404]
var odd = secondListOfNumbers.filter { $0 % 2 != 0 }
print(odd)
```


## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

```
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = 0

for i in thirdListOfNumbers {
sum += i
}
print(sum)
```
## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

```
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var even = thirdListOfNumbers.filter( { $0 % 2 == 0} ).reduce(0, +)
print(even)
```
## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
sharedElements.append(contentsOf: listOne)
sharedElements.append(contentsOf: listTwo)
print("\(sharedElements.count) Ints are shared" )

```


## Question 14

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var noDupeList: [Int] = []

for i in dupeFriendlyList {
if !noDupeList.contains(i) {
noDupeList.append(i)
}
}
print(noDupeList)


```

## Question 15

Find the second smallest number in an Array of Ints

```let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var sorted = arrayOfNumbers.sorted()
print(sorted[1])
```


## Question 16

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.

```var range = 1...1000
print(range.filter {$0 % 3 == 0 || $0 % 5 == 0})
```

## Question 17

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
var noRepeats = [Int]()
var firstRepeat = [Int]()
var secondRepeats = [Int]()

for i in someRepeatsAgain {
if !noRepeats.contains(i) {
noRepeats.append(i)
continue
} else {
if !firstRepeat.contains(i) {
firstRepeat.append(i)
} else {
secondRepeats.append(i)
}
}
}

print(secondRepeats)
```

## Question 18

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

`var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]`


## Question 19

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`


## Question 20

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]`


## Question 21

Given an Array of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`


## Question 22

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`


## Question 23

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`


## Question 24

Given an array of Characters, create a String ignoring and uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`


## Question 25

Print out each element in `myMatrix`

```
var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]
//3 different ways
print(Array(myMatrix.joined()))
print(myMatrix.flatMap{$0})
print(myMatrix.reduce([], +))
```

## Question 26

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`


## Question 27

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)
