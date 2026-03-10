


# What is an Error?

An error means that a program doesn't work as intended. It is also called a **bug**.

## Types of Errors

### 1. Syntax Errors

![Syntax Error Example](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT2Bdfj83c3STv1zSHleDjaUcoJV0zPENYPRg&s)

Syntax errors occur when the rules of the programming language are not followed, like grammatical mistakes in English. Some common examples are missing semicolons, unmatched brackets, or using incorrect keywords.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main()
{
    int x = 10  // <--- Missing semicolon here
    cout << "The value of x is: " << x << endl;
    
    return 0;
}
```

### 2. Runtime Errors

![Runtime Error Example](https://www.computerhope.com/issues/pictures/runtime-error.png)

Runtime errors appear during the program's execution (at runtime). They can cause the program to crash or behave unpredictably. Common examples include division by zero or accessing invalid memory.

Since runtime errors are only detected when the program runs, it is important to test with many different inputs.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 0;
    
    cout << a / b;  // Runtime Error: division by zero is not possible
    return 0;
}
```

### 3. Logical Errors

![Logical Error Example](https://i.ytimg.com/vi/MSBRGGLVBsQ/maxresdefault.jpg)

Logical errors happen due to incorrect logic or a wrong algorithm. They are the hardest to find because the program runs without crashing, but it gives the wrong results.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int l = 10, b = 5;
    int area;

    area = l + b;   // Logical Error: should be l * b for area
    cout << "Area = " << area;

    return 0;
}
```

### 4. Semantic Errors

![Semantic Error Example](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTeJCcEJEAAJrjNOeecXXzM9Ydprhwy3AR4-g&s)

A semantic error occurs when the syntax is correct, but the code doesn't make sense logically or violates the language's meaning rules. These are usually not caught by the compiler but can cause bugs or compilation issues in stricter checks.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    b = 20;   // Semantic Error: variable 'b' was not declared

    cout << a + b;
    return 0;
}


