Functions in C
1 Introduction
Functions are one of the most important concepts in the C programming language. They help to:
	•	Reduce code size
	•	Avoid repetition
	•	Improve readability
	•	Make programs easier to maintain

⠀A function allows us to divide a large program into smaller, manageable parts.

2. Application of Functions
Real-Life Scenario
Suppose you are developing software for a company where:
	•	A greeting message is shown at every entry point: ### "Welcome to ABC Company"
	•	An exit message is shown at every exit point: ### "Bye-bye, visit again"

⠀Problems Without Functions
If you write these messages again and again in different places:
1 Repetition – Same code written multiple times.
2 Poor Maintainability – If the message changes, you must update it everywhere.

⠀Solution
Use functions to write the code once and reuse it wherever required.

3. What is a Function?
A function in C is a block of code that performs a specific task. It can be called whenever needed.
General Syntax
return_type function_name(parameters)
{
    // function body
}

4. Example 1: Simple Function Call
Program
 <stdio.h>

void fun(){
    printf("fun() Called\n");
}

int main() 
{
    printf("Before Calling fun()\n");
    fun();
    printf("After Calling fun()");
    return 0;
}
Output
Before Calling fun()
fun() Called
After Calling fun()
Explanation
	•	Execution starts from main().
	•	fun() is called from main().
	•	Since fun() is a void function, it does not return any value.

⠀
5. Example 2: Calling a Function Multiple Times
Program
 <stdio.h>

void fun(){
    printf("fun() Called\n");
}

int main() 
{
    printf("Before Calling fun()\n");
    fun();
    fun();
    printf("After Calling fun()");
    return 0;
}
Output
Before Calling fun()
fun() Called
fun() Called
After Calling fun()
Explanation
	•	The function fun() is called twice.
	•	Each call executes the function body once.

⠀
6. Example 3: Function with Parameters and Return Value
Program
 <stdio.h>

int getMax(int x, int y)
{
    if(x > y)
      return x;
    else
      return y;
}

int main() 
{
    int x = 10, y = 20;
    printf("%d", getMax(x,y));
    return 0;
}
Output
20
Explanation
	•	getMax() takes two parameters: x and y.
	•	It compares them and returns the larger value.
	•	The return statement sends the result back to main().
	•	Variables inside the function are local and separate from main().

⠀
7. Important Terms of a Function
Every function consists of:
1 Function Declaration – Tells compiler about function name and type
2 Function Definition – Actual body of the function
3 Function Call – Invoking the function
4 Parameters – Input values
5 Return Value – Output from the function

⠀
8. Example: Greeting and Exit Messages
Program
 <stdio.h>

void greetMsg()
{
    printf("Hi,\n");
    printf("Welcome to GeeksForGeeks\n");
}

void exitMsg()
{
    printf("By\n");
    printf("Visit Again");
}

int main()
{
    greetMsg();
    printf("Hope you are enjoying\n");
    exitMsg();
    return 0;
}
Output
Hi,
Welcome to GeeksForGeeks
Hope you are enjoying
By
Visit Again
Explanation
	•	greetMsg() prints welcome message.
	•	exitMsg() prints goodbye message.
	•	Both functions are called from main() in sequence.

⠀
9. Advantages of Functions
1 Code Reusability – Write once, use many times
2 Modularity – Large programs broken into small parts
3 Easy Debugging – Errors are easier to locate
4 Better Readability – Program becomes clear and organized
5 Easy Maintenance – Changes made in one place only

⠀
10. Conclusion
Functions are the backbone of structured programming in C. They make programs:
	•	Efficient
	•	Organized
	•	Scalable
	•	Professional

⠀Without functions, large programs become difficult to manage and modify.
