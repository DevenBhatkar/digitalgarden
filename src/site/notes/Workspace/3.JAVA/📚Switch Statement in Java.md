---
{"dg-publish":true,"permalink":"/workspace/3-java/switch-statement-in-java/","noteIcon":""}
---

### 📌 What is it?

The `switch` statement is used as an alternative to **multiple `if-else-if` blocks**, especially when you’re checking a **single variable** against **multiple values**.

---

### 🧪 Example :

```java
int day = 3;

switch(day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Invalid day");
}
```
### 🔍 How it works:

- Java checks the value of `day`
    
- Matches it with `case` values
    
- Executes the matching block
    
- `break` is used to **exit** the switch once a match is found
    
- `default` is like `else` — runs if **no case matches**
    

---

### 🧠 Summary:

- Cleaner than long `if-else-if` chains
    
- Works with `int`, `char`, `String`, `enum` (not `float` or `double`)
    
- Use `break` to **prevent fall-through**