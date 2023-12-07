# Kotlin-Cheatsheet
Repository containing Kotlin syntax and best practices as a readme documentation.

# Table of Contents

- [Basics](#basics)
    - [Variables](#variables)
    - [Constants](#constants)
    - [Typing](#typing)
        - [Basic types](#basic-types)
            - [Whole numbers](#whole-numbers)
            - [Floating-point numbers](#floating-point-numbers)
            - [Characters](#characters)
            - [Strings](#strings)
            - [Booleans](#booleans)
        - [Type inference](#type-inference)
        - [Type aliases](#type-aliases)
    - [Operators](#operators)
    - [Comments](#comments)
- [Control Flow](#control-flow)
    - [`If` statement](#if-statement)
    - [`When` expression](#when-expression)
    - [`For` loop](#for-loop)
    - [`While` loop](#while-loop)
    - [`Break` and `continue` statements](#break-and-continue-statements)
- [Functions](#functions)
    - [Function parameters](#function-parameters)
    - [Function overloading](#function-overloading)
    - [Default parameter values](#default-parameter-values)
    - [Single-expression functions](#single-expression-functions)
    - [Infix functions](#infix-functions)
    - [Extension functions](#extension-functions)
    - [Tail-recursive functions](#tail-recursive-functions)
- [Object Oriented Programming](#object-oriented-programming)
    - [Classes](#classes)
    - [Constructors](#constructors)
    - [Init blocks](#init-blocks)
    - [Getters and setters](#getters-and-setters)
    - [Data classes](#data-classes)
    - [Inheritance](#inheritance)
    - [Abstract classes](#abstract-classes)
    - [Sealed classes](#sealed-classes)
    - [Inner classes](#inner-classes)
    - [Nested classes](#nested-classes)
    - [Inline classes](#inline-classes)
    - [Enum classes](#enum-classes)
    - [Object expressions](#object-expressions)
    - [Companion objects](#companion-objects)
    - [Delegation](#delegation)
- [Collections](#collections)
    - [Lists](#lists)
    - [Sets](#sets)
    - [Maps](#maps)
    - [Ranges](#ranges)
- [Functional programming](#functional-programming)
    - [Lambdas](#lambdas)
    - [Higher-order functions](#higher-order-functions)
    - [`forEach()` function](#foreach-function)
    - [`map()` function](#map-function)
    - [`filter()` function](#filter-function)
    - [`reduce()` function](#reduce-function)
    - [`fold()` function](#fold-function)
    - [`take()` function](#take-function)
    - [`takeWhile()` function](#takewhile-function)
    - [`drop()` function](#drop-function)
    - [`dropWhile()` function](#dropwhile-function)
    - [`all()` function](#all-function)
    - [`any()` function](#any-function)
    - [`count()` function](#count-function)
    - [`find()` function](#find-function)
    - [`none()` function](#none-function)
    - [`first()` function](#first-function)
    - [`firstOrNull()` function](#firstornull-function)
    - [`last()` function](#last-function)
    - [`lastOrNull()` function](#lastornull-function)
    - [`max()` function](#max-function)
    - [`min()` function](#min-function)
    - [`maxBy()` function](#maxby-function)
    - [`minBy()` function](#minby-function)
    - [`sum()` function](#sum-function)
    - [`sumBy()` function](#sumby-function)
    - [`groupBy()` function](#groupby-function)
    - [`associate()` function](#associate-function)
    - [`associateBy()` function](#associateby-function)
    - [`partition()` function](#partition-function)
    - [`zip()` function](#zip-function)
    - [`zipWithNext()` function](#zipwithnext-function)
    - [`flatten()` function](#flatten-function)
    - [`flatMap()` function](#flatmap-function)
    - [`distinct()` function](#distinct-function)
    - [`distinctBy()` function](#distinctby-function)
    - [`sorted()` function](#sorted-function)
    - [`sortedBy()` function](#sortedby-function)
    - [`sortedDescending()` function](#sorteddescending-function)
    - [`sortedByDescending()` function](#sortedbydescending-function)
    - [`reversed()` function](#reversed-function)
    - [`chunked()` function](#chunked-function)
    - [`windowed()` function](#windowed-function)
- [Advanced Features](#advanced-features)
    - [Generics](#generics)
    - [Annotations](#annotations)
    - [Null safety](#null-safety)
    - [Exceptions](#exceptions)
    - [`Ternary` operator](#ternary-operator)
    - [`Elvis` operator](#elvis-operator)
    - [`Lazy` initialization](#lazy-initialization)
    <!-- - [Coroutines](#coroutines)
    - [Multiplatform projects](#multiplatform-projects)
    - [Interoperability](#interoperability) -->
    


# Basics

Every program needs main method in order to run

```kotlin
fun main() {
    println("Hello world!")
}
```

## Variables

Keyword `var` allows us to declare a variable

```kotlin
var age
```

## Constants

Keyword `val` is used for declaring constants

```kotlin
val name
```

## Typing

Types in Kotlin are written after the variable name, separated by a colon. There are no primitive types in Kotlin. Everything is an object, which makes Kotlin a pure object-oriented language.

### Basic types

#### Whole numbers

Kotlin supports four types of whole numbers: `Byte` (8 bits), `Short` (16 bits), `Int` (32 bits), and `Long` (64 bits). Each type has a minimum and maximum value.
    
```kotlin
var var1: Byte = 127
var var2: Short = 32767
var var3: Int = 2147483647
var var4: Long = 9223372036854775807
```

#### Floating-point numbers

Kotlin supports two types of floating-point numbers: `Float` (32 bits) and `Double` (64 bits).

```kotlin
var var1: Float = 3.4028235E38
var var2: Double = 1.7976931348623157E308
```

#### Characters

Kotlin has a `Char` type, which represents a single character. Characters are enclosed in single quotes.

```kotlin
var var1: Char = 'a'
var var2: Char = 'A'
```

#### Strings

Kotlin has a `String` type, which represents a sequence of characters. Strings are enclosed in double quotes. Strings are immutable, which means that once you create them, you cannot change them.

```kotlin
var var1: String = "Hello world!"
```

#### Booleans

Kotlin has a `Boolean` type, which has two values: `true` and `false`.

```kotlin
var var1: Boolean = true
var var2: Boolean = false
```

### Type inference

Kotlin is a statically typed language, which means that the type of every expression is known at compile time. However, unlike Java, Kotlin supports type inference, which means that the compiler can often infer the type of an expression automatically.

```kotlin
val name = "John"
```

## Type aliases

Kotlin supports type aliases, which are used to create alternative names for existing types. We can use the `typealias` keyword to create a type alias.

```kotlin
typealias TypeAlias = Type
```

## Operators

### Arithmetic operators

Kotlin supports the following arithmetic operators: addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`), and remainder (`%`).

```kotlin
var1 + var2
var1 - var2
var1 * var2
var1 / var2
var1 % var2
```

### Assignment operators

We can assign a value to a variable using the assignment operator (`=`). We can also use compound assignment operators, which combine the assignment operator with an arithmetic operator (`+=`, `-=`, `*=`, `/=`, and `%=`).

```kotlin
var1 = var2
var1 += var2
var1 -= var2
var1 *= var2
var1 /= var2
var1 %= var2
```

### Comparison operators

To comparison operators we can count equality (`==`), inequality (`!=`), greater than (`>`), less than (`<`), greater than or equal to (`>=`), and less than or equal to (`<=`). 

```kotlin
var1 == var2
var1 != var2
var1 > var2
var1 < var2
var1 >= var2
var1 <= var2
```

Comparison operators return a Boolean value.

### Logical operators

In Kotlin, we can use logical operators to combine Boolean expressions. Kotlin supports the following logical operators: AND (`&&`), OR (`||`), and NOT (`!`).

```kotlin
var1 && var2
var1 || var2
!var1
```

### Increment and decrement operators

Kotlin supports the following increment and decrement operators: increment (`++`) and decrement (`--`). We can use these operators to increase or decrease the value of a variable by 1.

```kotlin
var1++
var1--
```
We can place these operators before or after a variable. If we place them before a variable, the value of the variable is increased or decreased before the expression is evaluated. If we place them after a variable, the value of the variable is increased or decreased after the expression is evaluated.

## Comments


Kotlin supports single-line comments and multi-line comments. Single-line comments start with two forward slashes (`//`). Multi-line comments start with a forward slash followed by an asterisk (`/*`) and end with an asterisk followed by a forward slash (`*/`).

```kotlin
// This is a single-line comment

/*
This is a 
multi-line 
comment
*/
```

## Control flow

### `If` statement

Kotlin supports the `if` statement, which executes a block of code if a condition is true. We can also use the `else` keyword to execute a block of code if the condition is false. We can also use the `else if` keyword to execute a block of code if the condition is false and another condition is true.


```kotlin
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true and condition1 is false
} else {
    // Code to execute if condition1 and condition2 are false
}
```

### `When` expression

Kotlin supports the `when` expression, which is similar to the `switch` statement in Java. The `when` expression executes a block of code depending on the value of a variable. We can also use the `else` keyword to execute a block of code if none of the conditions are true.

```kotlin
when (variable) {
    value1 -> {
        // Code to execute if variable is equal to value1
    }
    value2 -> {
        // Code to execute if variable is equal to value2
    }
    else -> {
        // Code to execute if none of the conditions are true
    }
}
```

Kotlin when expression is more powerful than Java switch statement. It can be used as an expression as well as a statement. It can test values of any types. It can test values using ranges and test expressions.

```kotlin
val x = 5

when (x) {
    1 -> println("x == 1")
    2 -> println("x == 2")
    else -> { // Note the block
        println("x is neither 1 nor 2")
    }
}

when (x) {
    0, 1 -> println("x == 0 or x == 1")
    else -> println("otherwise")
}

when (x) {
    in 1..10 -> println("x is in the range")
    in validNumbers -> println("x is valid")
    !in 10..20 -> println("x is outside the range")
    else -> println("none of the above")
}

```

It can also test values using type checks and smart casts.

```kotlin
fun hasPrefix(x: Any) = when(x) {
    is String -> x.startsWith("prefix")
    else -> false
}
```

### `For` loop

Kotlin supports the `for` loop, which executes a block of code a specified number of times. We can use the `until` keyword to specify the number of times the loop should be executed. We can also use the `step` keyword to specify the number of steps the loop should take. We can also use the `downTo` keyword to specify the number of times the loop should be executed in reverse order.

```kotlin
for (i in 0 until 10) {
    // Code to execute
}

for (i in 0 until 10 step 2) {
    // Code to execute
}

for (i in 10 downTo 0) {
    // Code to execute
}
```

### `While` loop

Kotlin supports the `while` loop, which executes a block of code while a condition is true. We can also use the `do` keyword to execute a block of code while a condition is true. The difference between the `while` loop and the `do` loop is that the `do` loop executes the block of code at least once.

```kotlin
while (condition) {
    // Code to execute while condition is true
}

do {
    // Code to execute while condition is true
} while (condition)
```

### `Break` and `continue` statements

Kotlin supports the `break` statement, which terminates the execution of a loop. We can also use the `continue` statement to skip the current iteration of a loop.

```kotlin
for (i in 0 until 10) {
    if (i == 5) {
        break
    }
    println(i)
} // 0 1 2 3 4

for (i in 0 until 10) {
    if (i == 5) {
        continue
    }
    println(i)
} // 0 1 2 3 4 6 7 8 9
```

## Functions

Kotlin supports functions, which are reusable blocks of code that perform a specific task. Functions can have parameters, which are input values passed into the function. Functions can also have a return type, which is the data type of the value returned by the function. If a function does not return a value, its return type is `Unit`.

```kotlin
fun functionName(parameter1: Type, parameter2: Type): ReturnType {
    // Code to execute
    return value
}
```

### Function parameters

Kotlin supports named parameters, which allow us to specify the name of each parameter when we call a function. Named parameters make our code easier to read and understand.

```kotlin
fun functionName(parameter1: Type, parameter2: Type): ReturnType {
    // Code to execute
    return value
}

functionName(parameter2 = value2, parameter1 = value1)
```


### Function overloading

Kotlin supports function overloading, which means that we can have multiple functions with the same name as long as they have different parameter types or different numbers of parameters.

```kotlin
fun functionName(parameter1: Type, parameter2: Type): ReturnType {
    // Code to execute
    return value
}

fun functionName(parameter1: Type): ReturnType {
    // Code to execute
    return value
}
```

### Default parameter values

Kotlin supports default parameter values, which allow us to specify default values for parameters. If we call a function without passing a value for a parameter, the default value is used.

```kotlin
fun functionName(parameter1: Type = defaultValue1, parameter2: Type = defaultValue2): ReturnType {
    // Code to execute
    return value
}

functionName(parameter2 = value2)
```

### Single-expression functions

Kotlin supports single-expression functions, which means that if a function returns a single expression, we can omit the curly braces and the return keyword.

```kotlin
fun functionName(parameter1: Type, parameter2: Type): ReturnType = value
```

### Infix functions

Kotlin supports infix functions, which means that if a function has only one parameter, we can omit the dot and the parentheses when we call the function.

```kotlin
infix fun functionName(parameter: Type): ReturnType {
    // Code to execute
    return value
}

functionName parameter
```

### Extension functions

Kotlin supports extension functions, which allow us to add new functions to existing classes without having to inherit from them. Extension functions are declared outside of classes.

```kotlin

fun String.functionName(parameter: Type): ReturnType {
    // Code to execute
    return value
}

"Hello world!".functionName(parameter)
```

### Tail-recursive functions

Kotlin supports tail-recursive functions, which means that if a function calls itself as the last operation, the function is compiled to use a loop instead of recursion. To declare a tail-recursive function, we use the `tailrec` keyword.

```kotlin
tailrec fun functionName(parameter: Type): ReturnType {
    // Code to execute
    return functionName(parameter)
}
```

### Scope functions

Kotlin supports scope functions, which are functions that execute a block of code in the context of an object. Kotlin supports the following scope functions: `let`, `run`, `with`, `apply`, and `also`.

```kotlin
object.let {
    // Code to execute
}

object.run {
    // Code to execute
}

with(object) {
    // Code to execute
}

object.apply {
    // Code to execute
}

object.also {
    // Code to execute
}
```

# Object Oriented Programming
<!-- <a id="object-oriented-programming"></a> -->

## Classes

Kotlin supports classes, which are templates for creating objects. Classes can have properties, which are variables that hold data. Classes can also have methods, which are functions that perform a specific task.

```kotlin

class ClassName {
    var property1: Type = value
    var property2: Type = value

    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Constructors

Kotlin supports constructors, which are special methods that are called when an object is created. We can use the `constructor` keyword to declare a constructor.

```kotlin
class ClassName constructor(parameter1: Type, parameter2: Type) {
    var property1: Type = value
    var property2: Type = value

    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Init blocks

Kotlin supports init blocks, which are blocks of code that are executed when an object is created. We can use the `init` keyword to declare an init block.

```kotlin
class ClassName constructor(parameter1: Type, parameter2: Type) {
    var property1: Type = value
    var property2: Type = value

    init {
        // Code to execute
    }

    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Getters and setters

Kotlin supports getters and setters, which are special methods that are used to get and set the values of properties. We can use the `get` keyword to declare a getter. We can also use the `set` keyword to declare a setter.

```kotlin
class ClassName {
    var property1: Type = value
        get() = value
        set(value) {
            field = value
        }
    var property2: Type = value
        get() = value
        set(value) {
            field = value
        }

    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Data classes

Kotlin supports data classes, which are classes that are used to hold data. Data classes are declared using the `data` keyword. Data classes automatically generate getters and setters for their properties. Data classes also automatically generate the `equals()`, `hashCode()`, and `toString()` methods. They work like `record` in Java.

```kotlin
data class ClassName(
    var property1: Type = value,
    var property2: Type = value
)
```

### Inheritance 

Kotlin supports inheritance. Classes are declared using the `class` keyword. Classes can be declared as `open` or `final`. `open` classes can be inherited from, while `final` classes cannot.

```kotlin
open class ClassName(
    var property1: Type = value,
    var property2: Type = value
)

class SubClassName(
    var property3: Type = value,
    var property4: Type = value
) : ClassName(property1, property2)
```

### Abstract classes

Kotlin supports abstract classes, which are classes that cannot be instantiated. Abstract classes are declared using the `abstract` keyword. Abstract classes can have abstract methods, which are methods that do not have a body. Abstract methods are declared using the `abstract` keyword.

```kotlin
abstract class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    abstract fun method1(parameter1: Type, parameter2: Type): ReturnType
    abstract fun method2(parameter1: Type): ReturnType
}
```

### Sealed classes

Kotlin supports sealed classes, which are classes that can only be inherited from within the same file. Sealed classes are declared using the `sealed` keyword.

```kotlin
sealed class ClassName(
    var property1: Type = value,
    var property2: Type = value
)

class SubClassName(
    var property3: Type = value,
    var property4: Type = value
) : ClassName(property1, property2)
```

### Inner classes

Kotlin supports inner classes, which are classes that are nested inside of another class. Inner classes are declared using the `inner` keyword. Inner classes can access the properties and methods of the outer class.


```kotlin
class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    inner class InnerClassName(
        var property3: Type = value,
        var property4: Type = value
    )
}
```

### Nested classes

Kotlin supports nested classes, which are classes that are nested inside of another class. Nested classes are declared using the `nested` keyword. Nested classes cannot access the properties and methods of the outer class.

```kotlin
class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    nested class NestedClassName(
        var property3: Type = value,
        var property4: Type = value
    )
}
```

### Inline classes

Kotlin supports inline classes, which are used to create classes that wrap a single value. We can use the `inline` keyword to create an inline class.

```kotlin
inline class InlineClassName(val value: Type)
```

### Enum classes

Kotlin supports enum classes, which are classes that are used to hold a fixed set of constants. Enum classes are declared using the `enum` keyword.

```kotlin

enum class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    CONSTANT1(value1, value2),
    CONSTANT2(value1, value2)
}
```

### Object expressions

Kotlin supports object expressions, which are expressions that create anonymous objects. Object expressions are declared using the `object` keyword. Object expressions can inherit from classes and interfaces. Object expressions can be used to create singletons or anonymous objects that are used only once.

```kotlin
object {
    var property1: Type = value
    var property2: Type = value

    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Object companions

Kotlin supports object companions, which are objects that are declared inside of a class. Object companions are declared using the `object` keyword. Object companions can be used to create static methods and properties.

```kotlin
class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    object {
        var property3: Type = value
        var property4: Type = value

        fun method1(parameter1: Type, parameter2: Type): ReturnType {
            // Code to execute
            return value
        }

        fun method2(parameter1: Type): ReturnType {
            // Code to execute
            return value
        }
    }
}
```

### Companion objects

Kotlin supports companion objects, which are objects that are declared inside of a class. Companion objects are declared using the `companion` keyword. Companion objects can be used to create static methods and properties.

```kotlin
class ClassName(
    var property1: Type = value,
    var property2: Type = value
) {
    companion object {
        var property3: Type = value
        var property4: Type = value

        fun method1(parameter1: Type, parameter2: Type): ReturnType {
            // Code to execute
            return value
        }

        fun method2(parameter1: Type): ReturnType {
            // Code to execute
            return value
        }
    }
}
```

## Delegation

Kotlin supports delegation, which means that we can delegate the implementation of an interface to another class. We can use the `by` keyword to delegate the implementation of an interface to another class. The class that delegates the implementation of an interface is called the delegate. The class that implements the interface is called the delegatee. The delegatee can access the properties of the delegate.

```kotlin
interface InterfaceName {
    fun method1(parameter1: Type, parameter2: Type): ReturnType
    fun method2(parameter1: Type): ReturnType
}

class ClassName(
    var property1: Type = value,
    var property2: Type = value
) : InterfaceName by OtherClassName(property1, property2)
```

## Collections

Kotlin supports collections, which are used to store groups of related objects. 

### Lists

Kotlin supports lists, which are ordered collections of objects. 

```kotlin
val list = listOf(value1, value2, value3)
```

### Sets

Kotlin supports sets, which are unordered collections of unique objects.

```kotlin
val set = setOf(value1, value2, value3)
```

### Maps

Kotlin supports maps, which are unordered collections of key-value pairs.

```kotlin
val map = mapOf(key1 to value1, key2 to value2, key3 to value3)
```

### Ranges

Kotlin supports ranges, which are used to represent a sequence of values. We can use the `..` operator to create a range. We can use the `in` operator to check if a value is in a range.

```kotlin
val range = 0..10
val value = 5
if (value in range) {
    // Code to execute if value is in range
}
```

## Coroutines

Kotlin supports coroutines, which are used to perform asynchronous operations. We can use the `launch` function to create a coroutine. We can use the `async` function to create a coroutine that returns a value. We can use the `await` function to get the value returned by a coroutine.

```kotlin
launch {
    // Code to execute
}

async {
    // Code to execute
}.await()
```

## Multiplatform projects

Kotlin supports multiplatform projects, which are projects that can be compiled to multiple platforms. We can use the `expect` keyword to declare an expect declaration, which is a declaration that is expected to be implemented in a platform-specific module. We can use the `actual` keyword to declare an actual declaration, which is a declaration that is implemented in a platform-specific module.

```kotlin
expect fun functionName(parameter1: Type, parameter2: Type): ReturnType

actual fun functionName(parameter1: Type, parameter2: Type): ReturnType {
    // Code to execute
    return value
}
```

## Interoperability

Kotlin supports interoperability, which means that we can use Kotlin code in Java and Java code in Kotlin. We can use the `@JvmField` annotation to declare a field that can be accessed from Java. We can use the `@JvmStatic` annotation to declare a static method that can be accessed from Java. We can use the `@JvmOverloads` annotation to declare a method that can be called with fewer arguments from Java.

```kotlin
@JvmField
var property: Type = value

@JvmStatic
fun functionName(parameter1: Type, parameter2: Type): ReturnType {
    // Code to execute
    return value
}

@JvmOverloads
fun functionName(parameter1: Type, parameter2: Type = defaultValue): ReturnType {
    // Code to execute
    return value
}
```

## Functional programming

### Lambdas

Kotlin supports lambdas, which are anonymous functions. We can use the `->` operator to create a lambda. We can use the `it` keyword to refer to the current parameter in a lambda.

```kotlin
val lambda = { parameter1: Type, parameter2: Type -> value }
```

### Higher-order functions

Kotlin supports higher-order functions, which are functions that take other functions as parameters or return other functions. We can use the `::` operator to pass a function as a parameter. We can use the `::` operator to return a function.

```kotlin
fun higherOrderFunction(function: (Type1, Type2) -> ReturnType) {
    // Code to execute
}

fun function(parameter1: Type1, parameter2: Type2): ReturnType {
    // Code to execute
    return value
}

higherOrderFunction(::function)
```

### `forEach()` function

Kotlin supports the `forEach()` function, which is used to iterate over a collection. We can use the `forEach()` function to iterate over a collection and perform a specific task for each element in the collection.

```kotlin
list.forEach {
    // Code to execute
}
```

### `map()` function

Kotlin supports the `map()` function, which is used to iterate over a collection and transform each element in the collection. We can use the `map()` function to iterate over a collection and transform each element in the collection.

```kotlin
list.map {
    // Code to execute
}
```

### `filter()` function

Kotlin supports the `filter()` function, which is used to iterate over a collection and filter the elements in the collection. We can use the `filter()` function to iterate over a collection and filter the elements in the collection.

```kotlin
list.filter {
    // Code to execute
}
```

### `reduce()` function

Kotlin supports the `reduce()` function, which is used to iterate over a collection and reduce the elements in the collection to a single value. We can use the `reduce()` function to iterate over a collection and reduce the elements in the collection to a single value.

```kotlin
list.reduce { accumulator, element ->
    // Code to execute
}
```

### `fold()` function

Kotlin supports the `fold()` function, which is used to iterate over a collection and reduce the elements in the collection to a single value.

```kotlin
list.fold(initialValue) { accumulator, element ->
    // Code to execute
}
```

### `take()` function

Kotlin supports the `take()` function, which is used to iterate over a collection and take a specific number of elements from the collection.

```kotlin
list.take(numberOfElements)
```

### `takeWhile()` function

Kotlin supports the `takeWhile()` function, which is used to iterate over a collection and take elements from the collection while a condition is true.

```kotlin
list.takeWhile {
    // Code to execute
}
```

### `drop()` function

Kotlin supports the `drop()` function, which is used to iterate over a collection and drop a specific number of elements from the collection.

```kotlin
list.drop(numberOfElements)
```

### `dropWhile()` function

Kotlin supports the `dropWhile()` function, which is used to iterate over a collection and drop elements from the collection while a condition is true.

```kotlin
list.dropWhile {
    // Code to execute
}
```

### `all()` function

Kotlin supports the `all()` function, which is used to iterate over a collection and check if all elements in the collection match a condition.

```kotlin
list.all {
    // Code to execute
}
```

### `any()` function

Kotlin supports the `any()` function, which is used to iterate over a collection and check if any element in the collection matches a condition.

```kotlin
list.any {
    // Code to execute
}
```

### `count()` function

Kotlin supports the `count()` function, which is used to iterate over a collection and count the number of elements in the collection that match a condition.

```kotlin
list.count {
    // Code to execute
}
```

### `find()` function

Kotlin supports the `find()` function, which is used to iterate over a collection and find the first element in the collection that matches a condition.

```kotlin
list.find {
    // Code to execute
}
```

### `none()` function

Kotlin supports the `none()` function, which is used to iterate over a collection and check if no elements in the collection match a condition.

```kotlin
list.none {
    // Code to execute
}
```

### `first()` function

Kotlin supports the `first()` function, which is used to iterate over a collection and find the first element in the collection that matches a condition. If no element in the collection matches the condition, the `first()` function throws an exception.

```kotlin
list.first {
    // Code to execute
}
```

### `firstOrNull()` function

Kotlin supports the `firstOrNull()` function, which is used to iterate over a collection and find the first element in the collection that matches a condition. If no element in the collection matches the condition, the `firstOrNull()` function returns `null`.

```kotlin

```kotlin
list.firstOrNull {
    // Code to execute
}
```

### `last()` function

Kotlin supports the `last()` function, which is used to iterate over a collection and find the last element in the collection that matches a condition. If no element in the collection matches the condition, the `last()` function throws an exception.

```kotlin
list.last {
    // Code to execute
}
```

### `lastOrNull()` function

Kotlin supports the `lastOrNull()` function, which is used to iterate over a collection and find the last element in the collection that matches a condition. If no element in the collection matches the condition, the `lastOrNull()` function returns `null`.

```kotlin
list.lastOrNull {
    // Code to execute
}
```

### `max()` function

Kotlin supports the `max()` function, which is used to iterate over a collection and find the largest element in the collection.

```kotlin
list.max()
```

### `min()` function

Kotlin supports the `min()` function, which is used to iterate over a collection and find the smallest element in the collection.

```kotlin
list.min()
```

### `maxBy()` function

Kotlin supports the `maxBy()` function, which is used to iterate over a collection and find the largest element in the collection. The `maxBy()` function takes a lambda expression as a parameter.

```kotlin
list.maxBy {
    // Code to execute
}
```

### `minBy()` function

Kotlin supports the `minBy()` function, which is used to iterate over a collection and find the smallest element in the collection. The `minBy()` function takes a lambda expression as a parameter.

```kotlin
list.minBy {
    // Code to execute
}
```

### `sum()` function

Kotlin supports the `sum()` function, which is used to iterate over a collection and sum the elements in the collection.

```kotlin
list.sum()
```

### `sumBy()` function

Kotlin supports the `sumBy()` function, which is used to iterate over a collection and sum the elements in the collection. The `sumBy()` function takes a lambda expression as a parameter.

```kotlin
list.sumBy {
    // Code to execute
}
```

### `groupBy()` function

Kotlin supports the `groupBy()` function, which is used to iterate over a collection and group the elements in the collection by a key. The `groupBy()` function takes a lambda expression as a parameter. The lambda expression returns the key for each element in the collection. The `groupBy()` function returns a map that maps each key to a list of elements that have that key. 

```kotlin
list.groupBy {
    // Code to execute
}
```

### `associate()` function

Kotlin supports the `associate()` function, which is used to iterate over a collection and create a map that maps each element in the collection to a value. The `associate()` function takes a lambda expression as a parameter. The lambda expression returns a pair that contains the key and the value for each element in the collection. The `associate()` function returns a map that maps each element in the collection to a value.

```kotlin
list.associate {
    // Code to execute
}
```

### `associateBy()` function

Kotlin supports the `associateBy()` function, which is used to iterate over a collection and create a map that maps each element in the collection to a key. The `associateBy()` function takes a lambda expression as a parameter. The lambda expression returns the key for each element in the collection. The `associateBy()` function returns a map that maps each element in the collection to a key.

```kotlin
list.associateBy {
    // Code to execute
}
```

### `partition()` function

Kotlin supports the `partition()` function, which is used to iterate over a collection and partition the elements in the collection into two lists. The `partition()` function takes a lambda expression as a parameter. The lambda expression returns a Boolean value that indicates whether an element should be added to the first list or the second list. The `partition()` function returns a pair that contains the first list and the second list.

```kotlin
list.partition {
    // Code to execute
}
```

### `zip()` function

Kotlin supports the `zip()` function, which is used to iterate over two collections and combine the elements in the collections into pairs. The `zip()` function takes another collection as a parameter. The `zip()` function returns a list of pairs that contains the elements in the first collection and the elements in the second collection.

```kotlin
list1.zip(list2)
```

### `zipWithNext()` function

Kotlin supports the `zipWithNext()` function, which is used to iterate over a collection and combine each element in the collection with the next element in the collection. The `zipWithNext()` function returns a list of pairs that contains each element in the collection and the next element in the collection.

```kotlin
list.zipWithNext()
```

### `flatten()` function

Kotlin supports the `flatten()` function, which is used to iterate over a collection and flatten the elements in the collection. The `flatten()` function returns a list that contains the elements in the collection.

```kotlin
list.flatten()
```

### `flatMap()` function

Kotlin supports the `flatMap()` function, which is used to iterate over a collection and flatten the elements in the collection. The `flatMap()` function takes a lambda expression as a parameter. The lambda expression returns a list for each element in the collection. The `flatMap()` function returns a list that contains the elements in the collection.

```kotlin
list.flatMap {
    // Code to execute
}
```

### `distinct()` function

Kotlin supports the `distinct()` function, which is used to iterate over a collection and remove duplicate elements from the collection. The `distinct()` function returns a list that contains the elements in the collection.

```kotlin
list.distinct()
```

### `distinctBy()` function

Kotlin supports the `distinctBy()` function, which is used to iterate over a collection and remove duplicate elements from the collection. The `distinctBy()` function takes a lambda expression as a parameter. The lambda expression returns a key for each element in the collection. The `distinctBy()` function returns a list that contains the elements in the collection.

```kotlin
list.distinctBy {
    // Code to execute
}
```

### `sorted()` function

Kotlin supports the `sorted()` function, which is used to iterate over a collection and sort the elements in the collection. The `sorted()` function returns a list that contains the elements in the collection.

```kotlin
list.sorted()
```

### `sortedBy()` function

Kotlin supports the `sortedBy()` function, which is used to iterate over a collection and sort the elements in the collection. The `sortedBy()` function takes a lambda expression as a parameter. The lambda expression returns a key for each element in the collection. The `sortedBy()` function returns a list that contains the elements in the collection.

```kotlin
list.sortedBy {
    // Code to execute
}
```

### `sortedDescending()` function

Kotlin supports the `sortedDescending()` function, which is used to iterate over a collection and sort the elements in the collection in descending order. The `sortedDescending()` function returns a list that contains the elements in the collection.

```kotlin
list.sortedDescending()
```

### `sortedByDescending()` function

Kotlin supports the `sortedByDescending()` function, which is used to iterate over a collection and sort the elements in the collection in descending order. The `sortedByDescending()` function takes a lambda expression as a parameter. The lambda expression returns a key for each element in the collection. The `sortedByDescending()` function returns a list that contains the elements in the collection.

```kotlin
list.sortedByDescending {
    // Code to execute
}
```

### `reversed()` function

Kotlin supports the `reversed()` function, which is used to iterate over a collection and reverse the order of the elements in the collection. The `reversed()` function returns a list that contains the elements in the collection.

```kotlin
list.reversed()
```

### `chunked()` function

Kotlin supports the `chunked()` function, which is used to iterate over a collection and split the elements in the collection into chunks. The `chunked()` function takes a size as a parameter. The `chunked()` function returns a list of lists that contains the elements in the collection.

```kotlin
list.chunked(size)
```

### `windowed()` function

Kotlin supports the `windowed()` function, which is used to iterate over a collection and split the elements in the collection into windows. The `windowed()` function takes a size as a parameter. The `windowed()` function returns a list of lists that contains the elements in the collection.

```kotlin
list.windowed(size)
```

## Advanced features

### Generics

Kotlin supports generics, which means that we can create classes and functions that can work with different types of data. We can use the `out` keyword to declare a covariant type parameter, which means that the type parameter can only be used as a return type. We can use the `in` keyword to declare a contravariant type parameter, which means that the type parameter can only be used as a parameter type.

```kotlin
class ClassName<out Type1, in Type2>(
    var property1: Type1 = value,
    var property2: Type2 = value
) {
    fun method1(parameter1: Type1, parameter2: Type2): ReturnType {
        // Code to execute
        return value
    }

    fun method2(parameter1: Type1): ReturnType {
        // Code to execute
        return value
    }
}
```

### Annotations

Kotlin supports annotations, which are used to provide metadata about code. Annotations are declared using the `annotation` keyword. Annotations can be applied to classes, properties, methods, parameters, and expressions.

```kotlin
annotation class AnnotationName(
    var property1: Type = value,
    var property2: Type = value
)

class ClassName {
    @AnnotationName(property1 = value1, property2 = value2)
    var property1: Type = value

    @AnnotationName(property1 = value1, property2 = value2)
    fun method1(parameter1: Type, parameter2: Type): ReturnType {
        // Code to execute
        return value
    }
}
```

### Null safety

Kotlin supports null safety, which means that we can prevent null pointer exceptions. We can use the `?` operator to declare a nullable variable. We can use the `!!` operator to throw a null pointer exception if a variable is null. We can use the `?.` operator to call a method on a nullable variable. We can use the `?:` operator to return a default value if a variable is null.

```kotlin
var var1: Type? = null
var var2: Type = var1!!
var var3: Type = var1?.method()
var var4: Type = var1 ?: defaultValue
```

### Exceptions

Kotlin supports exceptions, which are used to handle errors. We can use the `try` keyword to try a block of code. We can use the `catch` keyword to catch an exception. We can use the `finally` keyword to execute a block of code after the `try` block and the `catch` block.

```kotlin
try {
    // Code to try
} catch (exception: Exception) {
    // Code to execute if an exception is thrown
} finally {
    // Code to execute after the try block and the catch block
}
```

### Ternary operator

Kotlin does not support the ternary operator, which means that we cannot use the ternary operator to assign a value to a variable based on a condition. However, we can use the `if` expression to assign a value to a variable based on a condition.

```kotlin
val variable = if (condition) value1 else value2
```

### Elvis operator

Kotlin supports the Elvis operator, which is used to assign a default value to a variable if the variable is null. We can use the `?:` operator to assign a default value to a variable if the variable is null.

```kotlin
val variable = nullableVariable ?: defaultValue
```

### Lazy initialization

We can use the `lazy()` function to delay the initialization of a variable until it is needed.

```kotlin
val variable: Type by lazy {
    // Code to execute
    return value
}
```

### Casting

Kotlin supports casting, which means that we can convert a value of one type to a value of another type. We can use the `as` operator to cast a value to a type. We can use the `as?` operator to cast a value to a nullable type.

```kotlin
val variable1: Type1 = variable2 as Type1
val variable3: Type3? = variable4 as? Type3
```

### Copying

Kotlin supports copying, which means that we can create a copy of an object. We can use the `copy()` function to create a copy of an object.

```kotlin
val copy = object.copy()
```

### Destructuring

Kotlin supports destructuring, which means that we can extract the properties of an object and assign them to variables. We can use the `val` keyword to declare a variable.

```kotlin
val (property1, property2) = object
```

## String templates

```kotlin
val name = "John"
val age = 25
println("My name is $name and I am $age years old")
```