---
layout: post
title: Learning Kotlin Basics (Functions) - Part 3
---

Functions are block of code that can be called from other parts in your program. Functions makes code reusable and more readble. In the last two post we have already seen a few functions in action. One of them is the main() function which is automatically started when Kotlin program is started. We also have encountered other utility functions like println() that is used to print string to console, readln() which is used to read input from user and arrayOf() which is used to create an array. In this post we will creat our own functions and understand the different components of functions in Kotlin. Kotlin also has higher order functions and lambda expressions, but we will be looking at the in another post. 

## Creating Custom Functions

A function definition starts with the fun keyword, followed by the name of the function, a set of opening and closing parentheses, and a set of opening and closing curly braces. Contained in curly braces is the code that will run when the function is called.

```kotlin
    fun hello() {
        return println("Hello, world!")
    }

    fun main() {
        hello()
        // Hello, world!
    }
```

## Declaring Parameters

A parameter specifies the name of a variable and a data type that you can pass into a function as data to be accessed inside the function. Parameters are declared within the parentheses after the function name. Each parameter consists of a variable name and data type, separated by a colon and a space. Multiple parameters are separated by a comma. 

```kotlin
    fun hello(name: String, age: Int) {
        println("Hello, $name!, you are $age years old")
    }

    fun main() {
        hello("Nirab",25)
        // Hello, Nirab!, you are 25 years old
    }
```

Parameters in Kotlin are immutable. You cannot reassign the value of a parameter from within the function body.

## Returning Value

Kotlin functions can also send back values which can be stored in a variable that you can use elsewhere in your code. When defining a function, you can specify the data type of the value you want it to return. The return type is specified by placing a colon (:) after the parentheses, and then the name of the type (Int, String, etc). 

```kotlin
    fun multiply(x: Int, y: Int): Int {
        return x + y
    }

    fun main() {
        val result = multiply(10, 5)
        println(result)
        // 50
    }
```

By default, if you don't specify a return type, the default return type is Unit. Unit means the function doesn't return a value. Unit is equivalent to void return type in Java and C; and None in Python.

## Named and Default Arguments

You can name one or more of a function's arguments when calling it. This can be helpful when a function has many arguments or when you dont know the order of the parameters in a function.

```kotlin
    fun hello(name: String, age: Int) {
        println("Hello, $name!, you are $age years old")
    }

    fun main() {
        hello(age=25, name="Nirab") 
        // Order does not matter when you name arguments
    }
```

Function parameters can also specify default arguments. When you call a function, you can choose to omit arguments for which there is a default, in which case, the default is used.

```kotlin
    fun hello(name: String = "Mr X", age: Int = 50) {
        println("Hello, $name!, you are $age years old")
    }

    fun main() {
        hello("Nirab",25)
        // Hello, Nirab!, you are 25 years old

        hello("Nirab")
        // Hello, Nirab!, you are 50 years old
        
        hello(age = 25)
        // Hello, Mr X!, you are 25 years old
        
        hello()
        // Hello, Mr X!, you are 50 years old 
    }
```
