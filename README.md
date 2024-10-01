<!--
theme: gaia
class:
 - invert
headingDivider: 2
paginate: true
-->

<!--
_class:
 - lead
 - invert
-->

# Java Lambda Expressions

Streamline Your Code: A Guide to Java Lambdas

---

## What is a Lambda?

A **lambda expression** is a short block of code which takes in parameters and returns a value.

- Simplifies code for single-use functions
- Often used in functional programming styles
- Helps eliminate boilerplate code

```java
(parameter1, parameter2) -> expression
```

---

## Why Use Lambdas?

- Makes code **more readable**
- **Reduces verbosity** by eliminating unnecessary classes
- Improves **code reusability**

### Traditional vs Lambda

#### Traditional Approach:
```java
Comparator<Integer> comp = new Comparator<>() {
    public int compare(Integer o1, Integer o2) {
        return o1.compareTo(o2);
    }
};
```

---

#### Using Lambda:

```java
Comparator<Integer> comp = (o1, o2) -> o1.compareTo(o2);
```

Lambda is shorter and easier to read.

---

## Anatomy of a Lambda Expression

A lambda expression is defined by three components:

1. **Parameters**: `(parameter1, parameter2, ...)`
2. **Arrow Operator**: `->`
3. **Body**: `expression` or `{ statements }`

Example:

```java
(int a, int b) -> a + b
```

---

## Functional Interfaces

A lambda can only be used with **functional interfaces**.  
A **functional interface** has **one abstract method**.

```java
@FunctionalInterface
interface MyFunctionalInterface {
    void myMethod();
}
```

#### Example:

```java
Runnable r = () -> System.out.println("Hello Lambda!");
```

---

## Using Lambda in Collections

### Filtering a List:

```java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");

names.stream()
     .filter(name -> name.startsWith("A"))
     .forEach(System.out::println);
```

Output:

```
Alice
```

---

## Method References

Simplify lambdas using **method references**:

```java
list.forEach(s -> System.out.println(s));

// Method Reference
list.forEach(System.out::println);
```

---

## Sorting Example

### Traditional Sorting:

```java
List<String> list = Arrays.asList("D", "B", "A");
Collections.sort(list, new Comparator<>() {
    public int compare(String s1, String s2) {
        return s1.compareTo(s2);
    }
});
```

---

### With Lambdas:

```java
list.sort((s1, s2) -> s1.compareTo(s2));
```

---

### With Method Reference:

```java
list.sort(String::compareTo);
```

---

## Practice Exercise

1. Convert the following code to use a lambda:

```java
ActionListener listener = new ActionListener() {
    public void actionPerformed(ActionEvent e) {
        System.out.println("Button clicked!");
    }
};
```

---

## Resources

- [Java Lambda Basics](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)
- [Streams and Lambdas](https://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html)
- [Common Use Cases](https://www.baeldung.com/java-8-lambda-expressions-tips)

---

# 🎉
### Now You're Ready for Lambdas!
