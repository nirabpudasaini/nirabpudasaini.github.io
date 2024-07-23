---
layout: post
title: Kotlin Basics - Conditionals
---

Conditionals will let you execute different block of code based on coditions that you define in your program. Like any other language conditions are very important concept in Kotlin as it allows your code to be dynamic, by providing it with abalibility to handle descisions. There are two ways to implement conditions in a Kotlin program. 

## If Condition

If uses locial and comparasion to evaluate an expression and code is executed based on the result of the expression. The result of these expression is a boolean. Boolean data type and logical operators available for them was covered in [part 2 of kotlin basics](/basics-of-kotlin-2). Before getting into the if else expressions, lets look at the logical and comparision operators in Kotlin.

```kotlin
    val x = 3
    val y  = 5
    val z = 8
    println(x == y) //false
    println(x + y == z) //true
    println(x > 5) //false
    println(x < 5) //true
```

An if statement starts with the `if` keyword followed by a condition, which is a boolean expression inside parentheses and a set of curly braces which contains a block of code. The block of code only execute when the condition is met. 

```kotlin
    val x = 10
    if (x % 2 == 0){ // % is used to find remainder
        println("$x is an even number")
    }
```
We can also execute a block of statement if the value is false using the `else` keyword. The `else` branch in an `if/else` conditional only gets executed when all previous branches return false values.

```kotlin
    fun maxOf(a: Int, b: Int): Int {
        if (a > b) {
            return a
        } else {
            return b
        }
    }

    fun main() {
        println("${maxOf(3, 5)}") // 5
        println("${maxOf(8, 6)}") // 8
    }
```
We can also have multiple conditions using the `else if` keyword. Subsequent `else if` branches in an `if/else` conditional will get executed only when previous if or else if branches return false values.

```kotlin
    fun trafficLights(color: String) {
        if (color == "red") {
            println("Stop")
        } else if (color == "yellow") {
            println("Slow")
        } else if (color == "green") {
            println("Go")
        } else {
            println("Invalid Color")
        }
    }

    fun main() {
        trafficLights("red") //Stop
        trafficLights("green") //Go
        trafficLights("black") //Invalid Color
    }

```

### When Condition

If there are a lot of conditions the code might difficult to read and write with the `if/else` condition. It is recommended to use the `when` conditional to replace an `if/else` conditional when there are more than two branches. When is similar to switch statements in other languages. 

```kotlin
    fun printObjectType(myData: Any){
        when(myData) {
            is String -> println("String")
            is Int -> println("Integer")
            is Boolean -> println("Boolean")
            else -> println("Unknown")
        }
    }

    fun main() {
        
    }

```
There are two new things in this example. The `Any` data type and the `is` operator. `Any` data type is a special type in Kotlin from which all other type and object are derived. This means the function `printObjectType` can take anything as an argument. 

The `is` keyword allows to check the type of an object. `When` conditionals also support few other ways to make descisions in the code. You can write more complex conditions in when conditionals with the comma (,), in ranges, and the is keyword.

```kotlin
    val x = 3
    when (x) {
        2, 3, 5, 7 -> println("x is a prime number between 1 and 10.")
        in 1..10 -> println("x is a number between 1 and 10, but not a prime number.")
        else -> println("x isn't a prime number between 1 and 10.")
    }
```