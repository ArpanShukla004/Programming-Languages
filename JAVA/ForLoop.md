## For loop

+ To Execute a block of code repeatedly untill the condition is False 

**SYNTAX**:  


``` 
 for (Initialisation; Condition; Updation)  {  
     //Do SomeThing  
}
```

EXAMPLE:   
```
for(int i=0; i<5; i++){
    System.out.println("HELLO WORLD");
}
```
**EXPLANATION**:  
+ first it stores i=0; then checks the condition i<5 => 0<5 => its true. So, it enters into block of code and it prints "HELLO WORLD" 
+ After printing it goes through Updation part. Here i value increase by '1'(i++). Now, i=1 => 1<5 => its true.So, it enters into block of code and it prints "HELLO WORLD".
+ Similarly, the process is executing untill the condition gets false like when i=5 => 5<5 =>
its false, so it not enters into block of code.

#### OUTPUT PRINTS 4 TIMES (FROM i=0 TO i<5(i=4))

```  
output:

HELLO WORLD
HELLO WORLD
HELLO WORLD
HELLO WORLD
```
 ### PRINT SQUARE PATTERN USING FOR LOOP..

 ```
 for(int lines=1; lines<=4; lines++){
    System.out.println("* * * *");
 }
 
 OUTPUT: 
 
 * * * *
 * * * *
 * * * *
 * * * *
 ```
