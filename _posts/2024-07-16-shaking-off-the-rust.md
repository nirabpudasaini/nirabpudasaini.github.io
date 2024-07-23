---
layout: post
title: Shaking Off the Rust - Rediscovering Android Programming with Kotlin
---

It has been quite a long time since I last wrote some code. Recently, with some free time on my hands, I started exploring online resources to get back into coding. Having primarily worked as an Android developer, I naturally wanted to shake off the rust and dive back into creating Android apps after more than six years. Unsurprisingly, I found that the Android development ecosystem and the broader mobile development landscape have undergone significant changes during this time. Through this blog, I aim to document my reskilling journey. I hope it serves as a useful resource for others who might be interested in getting into Android development. 

## React Native vs Flutter vs Kotlin: Choosing My Path

When I last wrote Android apps, the primary tools were Java and XML. Kotlin was just beginning to receive support, and cross-platform solutions like React Native and Flutter were in their infancy. Now, the XML and Java approach to building Android apps is somewhat outdated, and the alternatives have matured significantly, offering compelling use cases.

Flutter appears to be a quick way to get started, with user-friendly tooling and cross-platform capabilities, provided you are willing to learn Dart. It has a very active and growing developer community and an impressive portfolio of apps built using it. React Native also offers cross-platform advantages, with the added benefit of allowing you to write code in JavaScript and TypeScript. Here's why I chose Kotlin for my journey back into Android development.

### Exploring Kotlin's Capabalities
One of the main reason is that I would like to learn the Kotlin programming language itself. I am particularly interested in learning Kotlin because of its modern and efficient design. Kotlin offers a concise way to write readable code with significantly less boilerplate compared to Java. An appealing features of Kotlin is its null safety, which helps prevent the common null pointer exceptions prevalent in Java.

Kotlin's language features, such as coroutines and flows, make writing asynchronous code much more manageable and less error-prone. These tools allow for the creation of asynchronous programs that are easy to read and maintain.

Additionally, Kotlin Multiplatform, although still in its early stages, promises to be a powerful tool for developing cross-platform applications. This capability could be highly beneficial in the future, allowing developers to share code across multiple platforms seamlessly.

Moreover, Kotlin’s compatibility with Java means that I can continue to use the Java libraries I am familiar with when needed, ensuring a smooth transition and integration into existing projects.    

### Cross Platform is Not Quite Native
As I embark on my journey to reacquaint myself with Android development, I've decided to focus on native development rather than cross-platform solutions. The advancements in reactive programming, modularization, and architectural design patterns have made native Android development more intuitive and powerful. Tools and frameworks such as Jetpack Compose, ViewModels, and Kotlin Flows have significantly enhanced the development experience, allowing for more efficient and maintainable code.

While cross-platform frameworks like Flutter and React Native offer the allure of writing code once and deploying it on multiple platforms, they come with their own set of trade-offs. The additional tooling, worrying about availability of plugins and larger app sizes associated with cross-platform frameworks do not align with my goals at this stage. However, I plan to update my web development skills in the future, at which point I might explore React Native. 

### The End Goal
One of the main reasons I am choosing to learn Kotlin is my ambition to contribute to the Maplibre Native codebase. In December 2020, a project I frequently used in my previous work switched to a non-open-source license. Maplibre Native, a fork of that project, has continued as an open-source initiative, and I am eager to contribute to its Android development efforts. 

## Learning Roadmap 
From my initial research, I have identified mapped out a learning path that will help me transition back into Android development. I may jump between sections as needed. I will write separate posts for each learning milestone and link them here in this blog. My aim is to be comprehensive enough for these posts to serve as useful resources for anyone starting out in Android development. 

### Learning Basic Kotlin
First, I need to familiarize myself with writing code in Kotlin. I will go through online resources to learn Kotlin syntax and the basic concepts of programming in Kotlin. 

- [Basics of Kotlin - Part 1 : Variables](/basics-of-kotlin-1)
- [Basics of Kotlin - Part 2 : Basic Data Types](/basics-of-kotlin-2)
- [Basics of Kotlin - Part 3 : Functions](/basics-of-kotlin-3)
- [Basics of Kotlin - Part 4 : Conditionals](/basics-of-kotlin-4)

### Learning Jetpack Compose
The traditional method of building Android UIs with XML now has a better alternative. Jetpack Compose is the recommended way to build UIs in Android. I plan to explore Jetpack Compose by building a calculator app. 

### Revising Android Basics
I will revisit Android basics such as activities, fragments, intents, broadcasts, and services. This will help me understand which concepts are still relevant and also get acquainted with newer concepts like ViewModels and the Room library. 

### Kotlin Coroutines and Kotlin Flows
I will dive deep into two powerful Kotlin features. Kotlin Coroutines offer a way to write asynchronous code in a sequential manner, improving code readability and maintenance. Kotlin Flows enable reactive programming with streams of data.

### Build and Publish Three Android Apps
I learn best through project-based work, so I plan to develop several Android apps as I progress through the learning process. Once I cover all the topics, I will write and publish a few apps to consolidate my knowledge. I have not yet decided on the specifics of these apps.

### Contributing to Maplibre Native
Ultimately, my goal is to contribute to the Maplibre Native project. They are migrating their Java codebase to Kotlin, and as someone who has used the library extensively in the past, I am excited to offer my contributions. I aim to make meaningful pull requests to support this migration and help improve the library.


I’m thrilled to embark on this journey of reskilling in Android development. Stay tuned for updates as I navigate through these learning milestones and work towards contributing to the Maplibre Native project.

Feel free to follow along, share your thoughts, and join me in this exciting journey back into Android programming!
