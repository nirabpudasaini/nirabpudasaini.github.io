---
layout: post
title: Learning Kotlin Basics - Part 1 (Variables)
---

Kotlin is a programming language developed by JetBrains, and it is now the default language for Android app development. Kotlin's syntax is similar to Java, but it is more concise and includes additional features such as type inference, null safety, and class extension. The easiest and fastest way to get started with Kotlin is by installing the [IntelliJ IDEA IDE](https://www.jetbrains.com/help/idea/installation-guide.html). After installing the IDE, you can start a new Kotlin project and run code directly in the editor or the REPL. You can also try Kotlin online in the [playground](https://play.kotlinlang.org/) on the Kotlin official website. You cannot write and compile Kotlin projects in the playground but it allows a quik way to test out and play with Kotlin code.

## Hello World!

Adhering to the tradition of learning a new programming language, lets start our journey into the Kotlin world by writing a simple hello world program. 

```kotlin
fun main() {
    println("Hello world of Kotlin programming")
}
```

Kotlin programs require a main function, which is the entry point where your program starts executing. Everything you write in Kotlin is within this main function or is called from it. The code block has a single statement that prints to the console using the built-in [println](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.io/println.html) function. Running the above code will produce the following output:

```
Hello world of Kotlin programming
```

## Variables

Variables in Kotlin can be defined using either the `val` or `var` keywords. The type of the variable is infered by Kotlin but can also be specified during decleration. 

```kotlin
fun main() {
    val name: String = "Nirab"
    var age = 35
    println("Hello $name, you are $age")
    
    // Assume a year passes
    age = 36
    println("Hello $name, you are now $age")

    /*
    * In Kotlin you will need to explicitly specify if you
    * want to assign null values to any variable or objects
    */

    val nullValue: Int? = null
}
```
Let us unpack the things going on in the above code. As you can see in the code we must declare a variable first before we can use it. In order to declare a variable , start with the val or var keyword. Then specify the variable name, data type, and initial value. For example: ```val count: Int = 2.```


The val keyword is used to define a variable that is read-only and it's value cannot change once it has been assigned. This is what we have done with the *name* vriable. The var keyword to define a variable that is mutable or changeable. In the code the variable *age* has been assigned value of 35 and later updated to 36. In Kotlin, it's preferred to use val over var when possible.

Since Kotlin has type inference, we can omit the data type in the variable declaration if an initial value is provided. In the code above the type of the variable *age* is automatically guessed by the value 36 assigned to it. However to be clear you can specify the data type in variable decleration. Some common basic Kotlin data types include: Int, String, Boolean, Float, and Double.

Additionally, the code has comments which are igonred by the compiler but can be used to provide information to make code more redable. The comment can be single line or multiline. Finally, as stated in the multiline comment, to assign null values to any variable, you need to explicitly specify it with a nullable type (e.g., Int?). Running the above code will produce the following output:

```
Hello Nirab, you are 35
Hello Nirab, you are now 36 
Null value is null
```
You can see that the name and age variable has been replaced by their assigned values in the output. This is called string template and is achived with the *$* sign in front of the variables. 

## Important Kotlin Resources

- [Official Kotlin Documentation](https://kotlinlang.org/docs/home.html)
- [Kotlin Koans - Excersise to Learn Kotlin Idioms](https://play.kotlinlang.org/koans/overview)

