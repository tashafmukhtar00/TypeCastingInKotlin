# TypeCasing in kotlin

In this article, you will learn about type conversion; how to convert a variable of one type to another with the help of example.

In Kotlin, a numeric value of one type is not automatically converted to another type even when the other type is larger.


    val number1: Int = 55
    val number2: Long = number1   // Error: type mismatch.      

Instead, you need to use toLong() explicitly (to convert to type Long). Kotlin does it for type safety to avoid surprises.

    val number1: Int = 55
    val number2: Long = number1.toLong()



Here's a list of functions in Kotlin used for type conversion:

    toByte() 
    toShort()
    toInt()
    toLong()
    toFloat()
    toDouble()
    toChar()
Note, there is no conversion for Boolean types.

### Conversion from Larger to Smaller Type

The functions mentioned above can be used in both directions (conversion from larger to smaller type and conversion from smaller to larger type).

However, conversion from larger to smaller type may truncate the value. For example,



    fun main(args : Array<String>) {
         val number1: Int = 545344
         val number2: Byte = number1.toByte()
         println("number1 = $number1")
         println("number2 = $number2")
}


When you run the program, the output will be:

    number1 = 545344
    number2 = 64