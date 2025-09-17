# Java 

<div align=center>
    <img src="../extras/death.gif" alt="ghostface killing" width="80%">
</div>

## Content
- [Fundamentals](#fundamentals)
- [Stings](#strings)

## Fundamentals

### Hello.java

```java
public class Hello {
  public static void main(String[] args) {
    System.out.println("Hello, world!");
  }
}
```

#### Breakdown

* **`public class Hello`** → Defines a class named `Hello`. (File must be `Hello.java`)
* **`main(String[] args)`** → Program entry point (code starts here).
* **`System.out.println("text");`** → Prints text to the console with a new line.

> [!IMPORTANT]  
> **Steps to Run** 
> 
> 1. Save as `Hello.java`  
> 2. Compile:  
>    ```bash
>    javac Hello.java
>    ```  
> 3. Run:  
>    ```bash
>    java Hello
>    ```  
> 4. Output:  
>    ```
>    Hello, world!
>    ```


### Variables

```java
int num = 6;
float decimalNum = 7.95f;
char letter = 'J';
boolean bool = true;
String site = "github.com";
```

## Strings

### Basic

```java
String first = "Rashi";
String last = "Chugani";
String name = first + " " + last;
System.out.println(name);
```

```java
String str1 = "value"; 
String str2 = new String("value");
String str3 = String.valueOf(123);
```

#### Breakdown

- **`String str1 = "value";`**

    - Creates a string literal stored in the **String pool**.
    - More memory-efficient (preferred way).

- **`String str2 = new String("value");`**

    - Creates a **new String object** in heap memory.
    - Not recommended unless you specifically need a new object.

- **`String str3 = String.valueOf(123);`**

    - Converts other data types into a `String`.
    - Example: `123` → `"123"`


> [!NOTE]
> - `String` in Java is **immutable** (cannot be changed once created).
> - Always prefer **string literals (`"..."`)** over `new String(...)`.
> - Use `String.valueOf()` to safely convert numbers, booleans, or objects to strings.

### Concatenation

```java
String s = 3 + "str" + 3;     // 3str3
String s = 3 + 3 + "str";     // 6str
String s = "3" + 3 + "str";   // 33str
String s = "3" + "3" + "23";  // 3323
String s = "" + 3 + 3 + "23"; // 3323
String s = 3 + 3 + 23;        // 29
```