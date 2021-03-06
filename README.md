<div align="center">
  <img height="60" src="java.png">
  <h1>Java Questions</h1>
  
---

<span>
I will post Java questions from basic to advanced, and may be it'll help you check your knowledge, get prepared for interviews, or whatever you want to use these for. I hope you have fun. </br>
I'll try to update these regularly.  
</span>
Feel free to contact me! <br />
<a href="https://www.instagram.com/oshanoshu"><img height="30" src="instagram.png"></a> <a href="https://www.twitter.com/oshanoshu"><img height="30" src="twitter.png"></a> <a href="https://www.linkedin.com/in/oshanoshu"><img height="30" src="linkedin.png"></a>

| You are free to use these questions in your project! But, I would really appreciate it, if you mention this repo. You can also find this in my [website](https://oshanoshu.github.io).|
|---|

</div>

---

###### 1. Which of the following is not a primitive data type in Java?

- A: `short`
- B: `byte`
- C: `boolean`
- D: `String` 

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D  

There are 8 primitive data types in Java: `byte`, `char`, `short`, `int`, `long`, `float`, `double`, `boolean`.  
Primitive data types are stored in stack.
Primitive data types are the simplest form of data types, and they can't be broken down into other simpler forms. In Java, `String` is an object.

</p>
</details>

---

###### 2. What's the output?

```java
public class IntegerOperations {
    public static void main(String[] args) {
        int a = 0;
        int a = 3;
        System.out.println(a);
    }
}
```

- A: `Compile-time Error`
- B: `0`
- C: `3`
- D: `Run-time Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

Java is a strongly typed language. Variable can be declared only once in Java. You can initialize the value for a variable when you declare it, or you can assign the value later. This would be correct:
```
int a = 0;
a = 3;
System.out.println(a); //prints 3
```
When you declare a variable with the same name twice, this type of error is caught when the program is being compiled. Hence, it falls under compiler-time error.
</p>
</details>

---

###### 3. What's the output?

```java
public class StringOperations {
    public static void main(String[] args) {
        String a = new String("Apple");
        String b = "Apple";
        String c = "Apple";
        
        System.out.print(a==b);
        System.out.print(" and ");
        System.out.print(b==c);
    }
}
```

- A: `true` and `false`
- B: `true` and `true`
- C: `false` and `true`
- D: `false` and `false`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

In Java, you have multiple methods of creating String object. If you explicitly use the word `new` keyword when you create the String, a new String object is created which will point to a distinct memory in heap.  
But, if you create the String object without using `new` keyword `String name = "Oshan"`, then the String is stored in a **String Pool**. To elaborate that, whenever a String object is created this way, Java first checks if that particular value is in the memory (**String Pool**), and if that value already exists, then instead of creating new string object, it simply points to the existing value in memory.   
And, when you are comparing two objects using `==` operator (also known as Reference Equality operator), you are asking Java if they come from the same memory address. Hence, the first print statement outputs false and the second one outputs true.  
</p>
</details>

---

###### 4. What's the output?

```java
public class StringOperations {
    public static void main(String[] args) {
        String a = new String("Apple");
        String b = "Apple";
        String c = "Apple";
        
        System.out.print(a.equals(b));
        System.out.print(" and ");
        System.out.print(b.equals(c));
    }
}
```

- A: `true` and `false`
- B: `true` and `true`
- C: `false` and `true`
- D: `false` and `false`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

In Java, when you are comparing two String objects using `equals()` method, you are checking the equality of values rather than references. Hence, both statements output `true` since the values of all three String objects are same.  
However, it's important to remember that String class in Java overrides the default implementaion of `equals()` method to behave like that. The default implementation by object class is same as `==` operator, but you can always override it to behave the way you like it.  
**REMEMBER**: Overriding methods is one of the way to achieve *Polymorphism* in Java, and it's one of the most important feature while working with objects.
</p>
</details>

---

###### 5. What's the output?

```java
public class IntegerOperations {
    public static void main(String[] args) {
        int c = '4';
        System.out.print(c);
    }
}
```

- A: `Compile-time Error`
- B: `4`
- C: `'4'`
- D: `52`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

**Type casting**, in primitive data type, is the way of assigning value of one primitive type to other primitive type. There are two types of type casting on primitive data types:
1. Narrowing Casting - Conversion of larger data type to smaller data type (Need to be done manually)
2. Widening Casting - Conversion of smaller data type to larger data type (Done automatically)
The ascending order of primitive data types is:  
`byte` >> `char` >> `short` >> `int` >> `long` >> `float` >> `double`  
So, when you initialize the integer value with character literal, type casting is automatically done, and the character literal is converted to integer.  
**REMEMBER**: When you are converting character literal to integer, you convert it into ASCII value. And, the ASCII value of '4' is 52. Hence, the answer is 52, not 4.

</p>
</details>

---

###### 6. What's the output?

```java
public class LoopOperations {
    public static void main(String[] args) {
        for(int i = 0; i < 6; i++)
        {
            if(i == 1)
                continue;
            
            if(i == 4)
                break;
                
            System.out.print(i+" ");
        }
    }
}
```

- A: `0 1 2 3`
- B: `0 2 3 4`
- C: `0 2 3 5`
- D: `0 2 3`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

| `break`     | `continue` |
| ----------- | ----------- |
| `break` statement terminates the loop at the moment it's executed.      | `continue` statement skips the current iteration after it's executed.|
| You can use it with `switch` statement.   | You can only use it in loops: `for`, `while`, `do-while`.|

Now, in our question since there is a `continue` statement when `i == 1`, it skips that loop. So, 1 is not printed. There is a `break` statement when `i == 4`, and that is where the loop terminates. So, it doesn't print anything after 4 (including 4).

</p>
</details>

---

###### 7. What's the output?

```java
public class LoopOperations {
    public static void main(String[] args) {
        int a = 5;
        int b = a/0;
        
        System.out.println(b);
    }
}
```

- A: Program fails during compilation
- B: Program fails during execution
- C: `5`
- D: `infinity`

<details><summary><b>Hint</b></summary>
<p>

Broadly speaking, there are two types of Exception:
1. Checked Exception
2. Unchecked Exception 

| Checked Exceptions | Unchecked Exceptions |  
| ------------------ | -------------------- |  
| These types of exceptions are checked by compiler during compilation process. | These types of exceptions are not checked during compilation process. |  
| Compiler mandates programmer to handle these exceptions either by using `try-catch` blocks or using `throws`.  | It's upto the program to handle these exceptions as they aren't checked by compiler. These generally occur due to programming errors. |  
| Examples: ClassNotFoundException, IOException. | Examples: ArithmeticException, NullPointerException. |

</p>
</details>

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

Since dividing an `integer` by `zero` is a programming error, it's not checked by compiler, and it throws ArithmeticException during execution.  
**What if ArithmeticException was CheckedException?**  
Then, the programmar would be mandated to write `try-catch` blocks or `throws` for every arithmetic operations in Java which would not be suitable as these exceptions are caused only on few extreme conditions. 

</p>
</details>

---

###### 8. What's the output?

```java
public class TryCatchOperations {
    public static void main(String[] args) {
        int a = 5;
        try{
            a = a/0;
            System.out.print("We are in a try block ");
        }
        catch(Exception e)
        {
            System.out.print("We are in a catch block ");
        }

        System.out.print(a);
    }
}
```

- A: `We are in a try block ` and `We are in a catch block` and `5`
- B: `We are in a catch block` and `5`
- C: `5`
- D: `We are in a try block ` and `5`
- E: None of the above

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`try-catch` block is one of the ways to handle exceptions in Java. Whenever an exception occurs inside `try` block, it is caught by `catch` block. Any statements on `try` block after the exception is encountered isn't executed, and the program resumes in the `catch` block and the statements in the `catch` block are executed. Therefore, the print statement inside `catch` is executed.
Since the exception is handled, the program successfully executes. Hence, when you reach the final print statement, `5` is printed as it's the only successful assisgnment of the value that worked. The other one was handled by `try-catch` block.

</p>
</details>

---

###### 9. What's the output?

```java
public class TryCatchOperations {
    public static void main(String[] args) {
        int a = 5;
        try{
            a = a/0;
            System.out.print("We are in a try block ");
        }
        catch (Exception e1)
        {
            try
            {
                a = a/5;
                System.out.print("We are in a nested try block ");
            }
            catch (Exception e2)
            {
                System.out.print("We are in a nested catch block ");
            }
            
            System.out.print(a);
        }
    }
}
```

- A: `We are in a nested try block ` and `We are in a nested catch block` and `5`
- B: `We are in a nested catch block` and `1`
- C: `1`
- D: `We are in a nested try block ` and `5`
- E: `We are in a nested try block ` and `1`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: E

`try-catch` block can be nested. In the first try block, ArithmeticException arises which is caught by `catch` block. At this point the value of `a` is still `5` as the arithmetic operation in first `try` block didn't go through. Then, we divide the current value of `a` by `5` and assign it to `a` which is perfectly okay as there is no exception this time and program continues with remainder of `try-block` statements and skips the `catch` block. So, the only print statements executed are from the nested `try` block and the last print statement from `catch` block. Since, we have changed the value of `a` to `1` using division. The answer is E.

</p>
</details>

---

###### 10. What's the output?

```java
public class TryCatchOperations {
    public static void main(String[] args) {
        int a = 5;
        try{
            a = a/0;
            System.out.print("We are in a try block ");
        }
        catch (Exception e1)
        {
            System.out.print("We are in a catch block ");
        }
        finally
        {
            System.out.print("We are in a finally block ");
        }

    }
}
```

- A: `We are in a try block ` and `We are in a catch block `
- B: `We are in a try block ` and `We are in a finally block `
- C: `We are in a catch block ` and `We are in a finally block `
- D: `We are in a nested catch block `

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

`finally` block is always executed irrespective of the exception raised. It executes after the `try-catch` block.
From [Oracle Documentation](https://docs.oracle.com/javase/tutorial/essential/exceptions/finally.html):     
> Note: If the JVM exits while the try or catch code is being executed, then the finally block may not execute. Likewise, if the thread executing the try or catch code is interrupted or killed, the finally block may not execute even though the application as a whole continues. 

</p>
</details>

---

###### 11. Interface can be declared as private.

- A: `True`
- B: `False`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

In Java, `Interface` is like a contract. It only consists of abstract methods and constants declaration. Interfaces can't be instantiated. The only way interfaces are executed in Java is when a class implements it. And, it does mean that the class needs to execute all the behaviors stated by the interface. So, if you declare `interface` as private, it means it can't be used by any other classes, and it contradicts the sole purpose of interface.    
Classes in Java can implement multiple interfaces. Multiple inheritance in Java is possible only using interfaces.   
**Why doesn't Java have Multiple Inheritance with classes?**  
Let's see what happens if Java allowed Multiple Inheritance.
```java
class A
{
  public void printMethod()
  {
    System.out.println("This is from Class A");
  }
}

class B
{
  public void printMethod()
  {
    System.out.println("This is from Class B");
  }
}

class C extends A, B
{
  public static void main(String args[])
  {
    C c = new C();
    c.printMethod();
  }
}
```
Now, we can see that `printMethod()` in class C will not know which `printMethod()` (From class A or class B) should it execute. To avoid these name conflicts and ambiguity, Multiple Inheritance (with classes) is not allowed in Java.
</p>
</details>

---

###### 12. Will the following program compile?

```java
interface A {
    public void print();
}

class B {

    B()
    {
        System.out.println("I am from class B");
    }
}


class C extends B implements A{
    public static void main (String args[])
    {
        System.out.println("Life is beautiful");
    }
}
```

- A: `Yes`
- B: `No`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

No, the program won't compile. It's because *class C* implements *interface A*, but it doesn't implement the inherited abstract method `A.print()`.   
Whenever any class implements the interface, it needs to provide implementation for all the inherited methods from the interface.  
This would have been correct.   
```java
class C extends B implements A{
  public void print()
  {
     //do something
  }
  
  //Rest of the code
}
```

</p>
</details>

---

###### 13. Will the following program compile?

```java
class Animals {

    String name;
    public Animals(String name)
    {
        this.name = name;
    } 

    public abstract void printName();

}
```

- A: `Yes`
- B: `No`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

No, the program won't compile. It's because *class Animals* has abstract method `printName()`. Only abstract classes or interfaces can have abstract methods. If you want your class to have both non-abstract and abstract methods, you should declare your class as abstract using `abstract` keyword before class. 
*Abstract classes* can be extended by other classes, but the derived class must have their implementation of abstract methods.   

| Abstract Class | Interface |  
| ------------------ | -------------------- |  
| Has both abstract and non-abstract methods. | All methods are implicitly abstract. |  
| Can have constructor which can be invoked by child class. | Can't have constructor. |  
| Child class doesn't need to provide implementation of all the methods. | Classes implementing interface must provide implementation for all the methods. |
| In Java, class can only extend one abstract class. | In Java, class can implements many interfaces. |
| Abstract class can extend other class or implement interfaces. | Interface can only extend other interfaces. |

</p>
</details>

---
###### 14. What is the output?

```java
public class Modifiers {

    private int number = 5;
    
    public static void main(String[] args) {
        number++;
        System.out.println(number);
    }
}
```

- A: Program doesn't compile
- B: `5`
- C: `6`
- D: None of the above

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

Program doesn't compile with an error `Cannot make a static reference to the non-static field number`.
You cannot make reference to the non-static member from the static method. Static members are the properties of class wheras non-static members are the properties of object. Each object has it's own copy of non-static members whereas every object shares the same static members. On the other hand, you can make reference to static members from non-static method.

</p>
</details>

---

###### 15. What is the output?

```java
public class Initializers {
    private static int number;
    
    static {
        number = 5;
    }
    
    public static void main(String[] args) {
        number++;
        System.out.println(number);
    }
}
```

- A: Program doesn't compile
- B: `5`
- C: `6`
- D: None of the above

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

*Static initializers* are the blocks of code written under `static` keyword. They are used to initialize the properties of classes (also called *Class Initializers*). They are executed first before any other code when the class is loaded, in the order they are declared.  
If you do not write `static` keyword, then they are *Instance Initializers* or simply *Initializers* and can't be referenced from static methods. Code in the instance initializers are copied to each constructor by the Java compiler which helps in sharing common code between the constructors.

```java
public class Initializers {
    private int number;
    
    //Initializer (instance)
    {
      number = 1;
    }
    
    Initializers(){
      System.out.prinln(number); //prints 1 whenever the constructor is called
    }
}
```

</p>
</details>

---

###### 16. What is the output?

```java
public class ThreadsOperations{
  
    public static int number = 0;
  
    public static void main(String[] args) {

      Thread thread = new Thread()
      {
          public void run()
          {
              number++;
          }
      };
      thread.start();
      System.out.println(number);
      number++;
      System.out.println(number);

    }

}
```

- A: Program doesn't compile
- B: `0` and `1`
- C: `1` and `2`
- D: `0` and `2`
- E: Values can be arbitrary

<details><summary><b>Answer</b></summary>
<p>

#### Answer: E  

Java is a multi-threaded programming language. In a multi-threaded program, multiple threads are executed concurrently (at the same time). The `main` method is a thread that all Java programs run.  
The above given program is a simple implementation of multi-threaded programming. When multiple threads are executed in a program, they share the variable and we don't know which thread is going to execute first (unless specified by programming constraints). So, we are not sure what value will the variable `number` hold when the print statement is called. Such problems occured due to concurrency is known as concurrency problems. 
Threads can be created by extending Thread class or by implementing Runnable interface. 



</p>
</details>

---

###### 17. How many times will the print statement be executed?

```java
public class ThreadsOperations{
    
    public static void main(String[] args) {

      Thread thread = new Thread()
      {
          public void run()
          {
              System.out.println("Thread is executing..."); //This one
          }
      };
      thread.start();
      thread.start();
    }

}
```
- A: 0
- B: 1
- C: 2
- D: Keeps executing unless told otherwise

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B  

**Threads** in java can only be started once. The program will throw an `IllegalThreadStateException` during runtime if we try to start a thread that has already been started. So, the print statement is only executed once. 

</p>
</details>

---

Influenced by [Javascript Questions](https://github.com/lydiahallie/javascript-questions) repo by @lydiahallie
