<div align="center">
  <img height="60" src="java.png">
  <h1>Java Questions</h1>
  
---

<span>
I will post Java questions from basic to advanced, and may be it'll help you check your knowledge, get prepared for interviews, or whatever you want to use these for. I hope you have fun. </br>
I'll try to update these regularly.  
</span>
Feel free to reach out to me! <br />
<a href="https://www.instagram.com/oshanoshu"><img height="30" src="instagram.png"></a> <a href="https://www.twitter.com/oshanoshu"><img height="30" src="twitter.png"></a> <a href="https://www.linkedin.com/in/oshanoshu"><img height="30" src="linkedin.png"></a>

| You are free to use these questions in your project! But, I would really appreciate it, if you mention this repo.|
|---|

</div>

---

###### 1. What's the output?

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

###### 2. What's the output?

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

###### 3. What's the output?

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

###### 4. What's the output?

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

Influenced by the [Javascript Questions](https://github.com/lydiahallie/javascript-questions) repo by @lydiahallie
