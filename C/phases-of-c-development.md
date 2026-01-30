# The 6-Phase Journey of C Program Development
Before we get to know how to write our code in C, it is important that we learn how our code will be developed into a fully functioning program. Getting to know the role of CPU and compilers along with other hidden elements will help us grasp what goes on behind the scenes. 

Hence, here are the 6 phases of developing a C program: 
## Phase 1: Editing
Writing the code is what is known as editing. This is the phase where you, the programmer, are directly involved in creating a C program. The code that you write in the C language is known as the source code. It forms the base of your program. Using an editor—ranging from lightweight terminal tools like vi and emacs to massive IDEs like Eclipse or Microsoft Visual Studio—you draft the "source code."

Once you’ve written your source code, you must save it with a .c extension. Saving the file with this extension will allow the compiler to recognize the code as a C code. At this stage, your code is just a text file.

## Phase 2: Preprocessing
Before your program can become something the computer can run, a helper program called the preprocessor steps in. Its job is to handle special instructions in the code called preprocessor directives
-File Expansion (#include): If you use a function like printf, your code doesn't actually know how to talk to the screen yet. The preprocessor finds the header file (like stdio.h) and literally copies its contents into your source file so the compiler has the necessary definitions.
-Constant Substitution (#define): If you’ve defined a value like PI as 3.14, the preprocessor goes through your entire file and swaps every instance of that word with the actual number. This makes the code easier to maintain since you only have to change the value in one place.

Note: # (hash, not hashtag) tells the system to process the preprocessor instructions (include, define) before compilation.

## Phase 3: Compiling
The compiler’s job  is to translate your C instructions into machine language (object code). This is a binary format consisting of 1s and 0s that a specific CPU architecture can interpret.
At this stage, the compiler checks the entire code to ensure that no syntactical errors have been committed for smooth running of the program. If syntax errors are detected, it issues a warning message. 
The syntactically accurate file is then converted into an object file (ending with a .obj or .o). The object file is the file that the computer can understand, written in binary. 

## Phase 4: Linking
In professional software development, programs are rarely contained in a single file. You might have one file for your main logic and another for mathematical calculations. Furthermore, your program relies on standard system libraries.
When the compiler finishes, it leaves "placeholders" for functions it couldn't find in the local file. The Linker steps in to resolve these. It searches through your various object files and library archives, finds the actual memory addresses of the functions you called, and "links" them together. The result is a single, cohesive executable file (like an .exe or an a.out) that contains everything needed to run.

## Phase 5: Loading
Before a program can actually run, it has to be placed into the computer’s memory (RAM). This task is handled by a system component called the loader. The loader takes the executable file produced after linking and moves it from the disk into memory so the CPU can start working on it.
If the program depends on shared libraries—ready-made code that many programs use—the loader brings those into memory as well. It also organizes space for the program’s instructions, variables, and data, making sure everything is in the right place so execution can begin smoothly.

## Phase 6: Execution
This is the part where the program actually runs in a way that we humans can comprehend. The CPU plays a major role in this. It executes the instructions written in the program, while keeping in mind the memory allocations of different variables which had been facilitated by the Loader. Here the machine language is finally converted into Human-understandable language.







