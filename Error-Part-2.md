
# Types of Errors in Programming Language - Part 2

## 1. Linker Errors

![Linker Errors](https://www.21kschool.com/sg/wp-content/uploads/sites/3/2025/06/Linker-Errors.png)

Linker errors happen when you have references in your code that can’t be resolved externally. They occur after compilation errors but before a program is run during the linking phase. Most linker errors are old-fashioned addressing errors, but can be resolved by simply making sure we have included all of our libraries and that we have referenced all of our external modules.

**Example:**

```cpp
#include <iostream>
using namespace std;

void greet();   // function declaration

int main() {
    greet();    // function call
    return 0;
}
```

(In this case, the `greet()` function is declared but not defined anywhere, causing a linker error: undefined reference to `greet`.)

## 2. Resource Errors

![Resource Errors](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTkR2Q-sUedJOcB9UtJ8_CRuAeZw16W6jNbJA&s)

Resource errors are due to inadequate system resources such as memory, disk space, and file handles. They lead to performance problems or the failure of programs.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    
    int* arr = new int[1000000000000];  // trying to allocate huge memory

    cout << "Memory allocated";

    delete[] arr;
    return 0;
}
```

(This will typically cause a bad allocation exception or program crash due to insufficient memory.)

## 3. Arithmetic Errors

![Arithmetic Errors](https://i.ytimg.com/vi/sWVgHfl9CwQ/maxresdefault.jpg)

Arithmetic errors occur through erroneous arithmetic or mathematical operations such as division by zero, overflow, underflow, and other errors. They are easily avoidable through validation of input data and safe mathematical operations.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {

    int a = 10;
    int b = 0;

    int result = a / b;   // arithmetic error

    cout << result;

    return 0;
}
```

(This causes a division by zero runtime error.)

## 4. Interface Errors

![Interface Errors](https://www.21kschool.com/sg/wp-content/uploads/sites/3/2025/06/Interface-Errors.png)

Interface errors occur when components or modules of a program communicate incorrectly. These are common in systems where components are connected through Application Programming Interfaces (APIs).

**Example:**

```cpp
#include <iostream>
using namespace std;

void add(int a, int b) {
    cout << a + b;
}

int main() {

    add(5);   // interface error (missing argument)

    return 0;
}
```

**What happens?**

Function `add()` expects 2 parameters.  
But only 1 parameter is passed.

**Error message (compile-time):**  
too few arguments to function 'add'

## 5. Security Errors

![Security Errors](https://www.21kschool.com/in/wp-content/uploads/sites/4/2025/06/Security-Errors.png)

Security errors are vulnerabilities in your code that can be exploited by attackers. This includes, but is not limited to, buffer overflows, code injection attacks, improper access controls, and other anomalies. Security audits, regular code reviews, and ethical programming practices will help eliminate these errors from your code.

**Example:**

```cpp
#include <iostream>
#include <cstring>
using namespace std;

int main() {

    char password[5];

    cout << "Enter password: ";
    cin >> password;   // no size limit

    cout << "Password entered: " << password;

    return 0;
}
```

