---
layout: post
title: Learning Kotlin Basics - Part 2 (Basic Data Types)
---

In this post, we will explore how to take input from the user in the console and get an overview of the basic data types in Kotlin including numbers, strings, and booleans. We will also look at common operations on these data types and how to perform them.

## Taking User Input

The readln() function reads from the standard input. This function reads the entire line the user enters as a string.

```
// Prints a message to request input
println("Enter any word: ")

// Reads and stores the user input. For example: Happiness
val yourWord = readln()

// Prints a message with the input
print("You entered the word: ")
print(yourWord)
// You entered the word: Happiness
```

## Basic Data Types

### Numbers

Kotlin supports different number types, such as Int, Long, Double, and Float. As with other languages, Kotlin uses +, -, *, /, and % for addition, subtraction, multiplication, division, and remainder, respectively. Int and Float are 32 bits in size, while Long and Double are 64 bits, allowing for a larger range of values.

Division between integers always returns an integer. Any fractional part is discarded.

```
val x = 5/2 
println(x)
```
To return a floating-point type, at least one of the arguments needs to be a floating-point.

### String

Strings in Kotlin are similar to strings in other programming languages. Use " for strings and ' for single characters. Concatenate strings with the + operator. You can create string templates by combining them with values; the $variableName is replaced with the text representing the value. This is called variable interpolation.

### Booleans

The Boolean type represents boolean objects that can have two values: true and false. Built-in operations on booleans include:

- || – disjunction (logical OR)
- && – conjunction (logical AND)
- ! – negation (logical NOT)

```
val myTrue: Boolean = true
val myFalse: Boolean = false
val boolNull: Boolean? = null

println(myTrue || myFalse)
// true
println(myTrue && myFalse)
// false
println(!myTrue)
// false
println(boolNull)
// null
```

### Arrays

An array is a data structure that holds a fixed number of values of the same type or its subtypes. In Kotlin, arrays are immutable, which means once you create an array, the size is fixed. You can't add or remove elements, except by copying to a new array.

## Type Check and Cast

In Kotlin, you can perform type checks to determine the type of an object at runtime. Type casts enable you to convert objects to a different type. In most cases, you don't need to use explicit cast operators because the compiler automatically casts objects for you. However, be careful with implicit casts, as they are not always available. Numbers are not implicitly converted to larger types and require explicit conversion.

```
val number: Any = 42

if (number is Int) {
    println(number + 1) // Output: 43
}

val doubleNumber = number as? Double
println(doubleNumber) // Output: null
```



