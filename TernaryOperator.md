### **What is an Operator?**

An operator is a symbol that is used to perform an operation on one or more values (called operands).
These operations can be mathematical or logical.

### **What is a Ternary Operator?**

The word ternary means 3.
A ternary operator works on three operands:

1.Condition – something that we check.
2. Value if the condition is true.
3. Value if the condition is false.

It is a short form of if–else.

**### A general template ( syntax):**
datatype variable_that_will_hold_result = (condition_to_check) ? value_if_true : value_if_false;

Example:
```
int a = 10;
int b = 43;

int which_is_bigger = (a > b) ? a : b;
```

**Explanation:**
 Condition: a > b

  If true → store a

  If false → store b

**### Example for real life codebases:**

`string status = (isConnected) ? "Connected" : "Disconnected";
`
What it actually mean ? 

```
bool isConnected;    // variable declaration
string status;       // variable declaration

isConnected = true;  // value assignment

if (isConnected) {
    status = "Connected";
} else {
    status = "Disconnected";
}

cout << status;
```


**Why Do We Use Ternary Operators?**

- To reduce code length
- To make code cleaner and more readable
- When the logic is simple and clear.





