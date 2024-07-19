---
layout: post
title: Learning Kotlin Basics - Part 2 (Basic Data Types)
---

In this post, we will explore how to take input from the user in the console. We will also explore the basic data types in Kotlin including numbers, strings, booleans and arrays. We will also look at common operations on these data types and how to perform them. This will also include some unique nuances of Kotlin language while dealing with these data types. 

## Taking User Input

The readln() function reads from the standard input. This function reads the entire line the user enters as a string.

```kotlin
    println("Enter something:")

    // Reads and stores the user input. For example: Hello Kotlin
    val yourWord = readln()

    print("You entered: ")
    print(yourWord)
    // Prints You entered: Hello Kotlin
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

Kotlin keeps numbers as primitives, but it lets you call methods on numbers as if they were objects.

```kotlin
    5.times(3)
    6.5.plus(4)
    8.minus(5)
    24.div(6)
```


### String

Strings in Kotlin are similar to strings in other programming languages. Use " for strings and ' for single characters. Concatenate strings with the + operator. 

```kotlin
    val fName: String = "Nirab"
    val lName = "Pudasaini"
    val spaceBar = ' '
    val fullName = fName + spaceBar + lName
    println(fullName) //Nirab Pudasaini
```
You can create string templates by combining them with values; the $variableName is replaced with the text representing the value. This is called variable interpolation. You can also do mathematical operations inside strings using string templates.

```kotlin
    val numberOfApples = 5
    val numberOfMangos = 3
    println("You have $numberOfApples apples and $numberOfMangos mangos.")
    // You have 5 apples and 3 mangos.
    println("You have ${numberOfApples + numberOfMangos} Fruits in total.")
    // You have 8 Fruits in total.

```

Special characters start from an escaping backslash \\. The following escape sequences are supported:

- \t – tab
- \b – backspace
- \n – new line (LF)
- \r – carriage return (CR)
- \\' – single quotation mark
- \\" – double quotation mark
- \\\ – backslash
- \$ – dollar sign


```kotlin
    println('\n') // Prints an extra newline character
    println('\$') // Print the character $
```

Kotlin also supports multiline strings which can contain newlines and arbitrary text. It is delimited by a triple quote (""") and does not require escaping and can contain newlines and any other characters. 

```kotlin
    val text = """
        A quick brown fox
        jumped over a lazy fox
    """
```

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

An array is a data structure that holds a fixed number of values of the same type or its subtypes. You can declare an array using arrayOf() function without a type associated to its elements. You can also declare arrays of integers using intArrayOf(). You can use the joinToString to print out the elements of an array. 

```kotlin
    val momo = arrayOf("steamed", "fried", "kothe", "chilly")
    println(momo.joinToString())

    val sevenDaysOfMomoPlates = intArrayOf(2,0,1,2,2,3,1)
```

In Kotlin, arrays are immutable, which means once you create an array, the size is fixed. You can't add or remove elements, except by copying to a new array which makes it very innefficient. 

```kotlin
    var momo = arrayOf("steamed", "fried", "kothe", "chilly")
    // Using the += assignment operation creates a new array momo,
    // copies over the original elements and adds "jhol"
    momo += "jhol"

    println(momo.joinToString()) // steamed, fried, kothe, chilly, jhol
```

Two arrays can be added with a + operator. Arrays are indexed starting with zero and you can use square bracket with a number to access or modify the nth element.

```kotlin
    val order1 = arrayOf(2, "fried")
    val order2 = arrayOf(1, "kothe")

    val kitchenQueue = order1 + order2
    println(kitchenQueue.joinToString())

    println(kitchenQueue[0]) //2
    println(kitchenQueue[3]) //kothe

    kitchenQueue[1] = "steamed"
```
Array can also be nested to create multidimensional arrays. 

```kotlin
    val order1 = arrayOf(2, "fried")
    val order2 = arrayOf(1, "kothe")
    val kitchenQueue = arrayOf(order1,order2)
    println(kitchenQueue[0].joinToString()) //2, fried
    println(kitchenQueue[0][1]) //fried
```

## Type Check and Cast

In Kotlin, you can perform type checks to determine the type of an object at runtime. Type casts enable you to convert objects to a different type. In most cases, you don't need to use explicit cast operators because the compiler automatically casts objects for you. However, be careful with implicit casts, as they are not always available. For example numbers are not implicitly converted to larger types and require explicit conversion.

```kotlin
    val l = 1L + 3 // Automatic conversion Long + Int => Long

    val i: Int = 2
    val s: String = i.toString() //Explicit conversion to String
    val f: Float = i.toFloat() //Explicit conversion to Float
```



