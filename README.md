# FINAL_LAB_SEM6

Object VariableAndStringDemo {
  Def main(args: Array[String]) {
    // Declaring variables using var and val
    Var mutableVariable: Int = 10
    Val immutableVariable: String = “Hello, world!”

    Println(s”Mutable variable value: $mutableVariable”)
    Println(s”Immutable variable value: $immutableVariable”)

    // Changing the value of the mutable variable
    mutableVariable = 20

    println(s”New mutable variable value: $mutableVariable”)

    // String functions
    Val str1: String = “Scala is a functional programming language”
    Val str2: String = “ and it runs on the Java Virtual Machine”

    // String concatenation using ‘+’
    Val str3: String = str1 + str2
    Println(s”Concatenated string: $str3”)

    // String length
    Val strLength: Int = str1.length()
    Println(s”Length of ‘$str1’ is $strLength”)

    // String substring
    Val substring: String = str1.substring(0, 5)
    Println(s”Substring of ‘$str1’ from index 0 to 5 is ‘$substring’”)

    // String replace
    Val replacedString: String = str1.replace(“functional”, “object-oriented”)
    Println(s”Replaced string: $replacedString”)
  }
}




Object ConditionalDemo {
  Def main(args: Array[String]) {
    // If-else statement
    Val number: Int = 5
    If (number > 0) {
      Println(“The number is positive”)
    } else {
      Println(“The number is not positive”)
    }

    // Nested if statement
    Val age: Int = 20
    Val gender: String = “female”
    If (age >= 18) {
      If (gender == “male”) {
        Println(“You are an adult male”)
      } else {
        Println(“You are an adult female”)
      }
    } else {
      Println(“You are not an adult”)
    }

    // Conditional ladder
    Val grade: String = “B+”
    If (grade == “A+”) {
      Println(“You got an A+ grade”)
    } else if (grade == “A”) {
      Println(“You got an A grade”)
    } else if (grade == “B+”) {
      Println(“You got a B+ grade”)
    } else if (grade == “B”) {
      Println(“You got a B grade”)
    } else {
      Println(“You got a grade lower than B”)
    }
  }
}






Object ScalaDemo {
  Def main(args: Array[String]) {
    // For loop to calculate the sum of numbers in a list
    Val nums: List[Int] = List(1, 2, 3, 4, 5)
    Var sum: Int = 0
    For (num <- nums) {
      Sum += num
    }
    Println(s”The sum of numbers in $nums is $sum”)

    // While loop to calculate the factorial of a number
    Val num: Int = 5
    Var factorial: Int = 1
    Var i: Int = 1
    While (I <= num) {
      Factorial *= i
      I += 1
    }
    Println(s”The factorial of $num is $factorial”)

    // Do-while loop to check if a number is prime
    Val n: Int = 7
    Var isPrime: Boolean = true
    Var j: Int = 2
    Do {
      If (n % j == 0) {
        isPrime = false
      }
      J += 1
    } while (j <= n / 2 && isPrime)
    If (isPrime) {
      Println(s”$n is a prime number”)
    } else {
      Println(s”$n is not a prime number”)
    }
  }
}





Object ArrayExample {
  Def main(args: Array[String]): Unit = {
    // Creating an array
    Val numbers = Array(1, 2, 3, 4, 5)

    // Accessing elements
    Println(“First element: “ + numbers(0))

    // Updating elements
    Numbers(0) = 10
    Println(“Updated first element: “ + numbers(0))

    // Finding the length
    Println(“Array length: “ + numbers.length)

    // Using map function to square each element
    Val squaredNumbers = numbers.map(x => x * x)
    Println(“Squared numbers: “ + squaredNumbers.mkString(“, “))

    // Using filter function to get even numbers
    Val evenNumbers = numbers.filter(x => x % 2 == 0)
    Println(“Even numbers: “ + evenNumbers.mkString(“, “))

    // Using reduce function to sum all elements
    Val sum = numbers.reduce((x, y) => x + y)
    Println(“Sum of numbers: “ + sum)

    // Using foreach function to print each element
    Println(“Printing each element using foreach:”)
    Numbers.foreach(println)

    // Creating a multidimensional array using ofDim()
    Val multiArray = Array.ofDim[Int](2, 3)
    multiArray(0)(0) = 1
    multiArray(0)(1) = 2
    multiArray(0)(2) = 3
    multiArray(1)(0) = 4
    multiArray(1)(1) = 5
    multiArray(1)(2) = 6

    // Printing the multidimensional array
    Println(“Multidimensional array:”)
    For (I <- multiArray.indices) {
      For (j <- multiArray(i).indices) {
        Print(multiArray(i)(j) + “ “)
      }
      Println()
    }
  }
}




Object ScalaDemo {
  Def main(args: Array[String]) {
    // Function to calculate the sum of two numbers
    Def sum(a: Int, b: Int): Int = {
      Return a + b
    }
    Val result: Int = sum(5, 3)
    Println(s”The sum of 5 and 3 is $result”)

    // Function to print a message
    Def printMessage(): Unit = {
      Println(“This is a message from a function”)
    }
    printMessage()

    // Function to return a Boolean value
    Def isEven(num: Int): Boolean = {
      Return num % 2 == 0
    }
    Val num: Int = 6
    Val isNumEven: Boolean = isEven(num)
    Println(s”$num is even: $isNumEven”)

    // Function to take another function as an argument
    Def executeFunction(func: (Int, Int) => Int, a: Int, b: Int): Int = {
      Return func(a, b)
    }
    Val res1: Int = executeFunction(sum, 10, 20)
    Val res2: Int = executeFunction((a: Int, b: Int) => a * b, 5, 6)
    Println(s”The result of sum function is $res1”)
    Println(s”The result of a lambda function is $res2”)
  }
}

