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

| You are free to use these questions in your project! But, I would really appreciate it if you mention this repo.|
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
