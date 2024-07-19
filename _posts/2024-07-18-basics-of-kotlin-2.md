---
layout: post
title: Learning Kotlin Basics - Part 2 (Basic Data Types)
---

In this post, we will explore how to take input from the user in the console and get an overview of the basic data types in Kotlin including numbers, strings, and booleans. We will also look at common operations on these data types and how to perform them.

## Taking User Input

The readln() function reads from the standard input. This function reads the entire line the user enters as a string.

```kotlin
// Prints a message to request input
println("Enter any word: ")

// Reads and stores the user input. For example: Happiness
val yourWord = readln()

print("You entered the word: ")
print(yourWord)
// You entered the word: Happiness
```

## Basic Data Types

### Numbers

Kotlin supports different number types, such as Int, Long, Double, and Float. Int and Float are 32 bits in size, while Long and Double are 64 bits, allowing for a larger range of values.

```kotlin
val myInt = 1
val myLong = 10L
val myFloat = 4.20f
val myDouble = 3.14
```

As with other languages, Kotlin uses +, -, *, /, and % for addition, subtraction, multiplication, division, and remainder, respectively. Kotlin allows the use of underscores with the numbers for better redability. 

```kotlin
println(1 + 2)
println(2_500_000_000L - 1L)
println(3.14 * 2.71)
println(10.0 / 3)
```
Division between integers always returns an integer. Any fractional part is discarded. To return a floating-point type, at least one of the arguments needs to be a floating-point.

```kotlin 
val intTwo = 2
val intFive = 5
val floatFive = 5.0
println(intFive/intTwo) // Prints 2
println(floatFive/intTwo) // Prints 2.5
```


### String

Strings in Kotlin are similar to strings in other programming languages. Use " for strings and ' for single characters. Concatenate strings with the + operator. You can create string templates by combining them with values; the $variableName is replaced with the text representing the value. This is called variable interpolation.

### Booleans

The Boolean type represents boolean objects that can have two values: true and false. Built-in operations on booleans include:

- || – disjunction (logical OR)
- && – conjunction (logical AND)
- ! – negation (logical NOT)


```kotlin
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

An array is a data structure that holds a fixed number of values of the same type or its subtypes. In Kotlin, arrays are immutable, which means once you create an array, the size is fixed. You can't add or remove elements, except by copying to a new array. You can declare an array of strings using arrayOf function. Use the java.util.Arrays.toString() array utility to print it out.

```kotlin
val school = arrayOf("shark", "salmon", "minnow")
println(java.util.Arrays.toString(school))

```

## Type Check and Cast

In Kotlin, you can perform type checks to determine the type of an object at runtime. Type casts enable you to convert objects to a different type. In most cases, you don't need to use explicit cast operators because the compiler automatically casts objects for you. However, be careful with implicit casts, as they are not always available. Numbers are not implicitly converted to larger types and require explicit conversion.

```kotlin
val l = 1L + 3 // Automatic conversion Long + Int => Long
```



