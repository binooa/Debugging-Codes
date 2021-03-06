# Debugging Codes
 Debugging Codes
 
 **Programming Errors in C**
 
There are mainly five types of errors exist in C programming:

- Syntax error
- Run-time error
- Linker error
- Logical error
- Semantic error
 
## Example code for Syntax Error

```C
#include <stdio.h>  
int main()  
{  
    a = 10;  
    printf("The value of a is : %d", a);  
   return 0;  
}  
```

```C
#include <stdio.h>  
int main()  
{  
  int a=2;  
  if(.)  // syntax error  
  
  printf("a is greater than 1");  
   return 0;  
}  
```

## Example code for Runtime Error

```C
#include <stdio.h>  
int main()  
{  
    int a=2;  
    int b=2/0;  
    printf("The value of b is : %d", b);  
    return 0;  
}  
```

## Example code for Linker Error

```C
#include <stdio.h>  
int Main()  
{  
    int a=78;  
    printf("The value of a is : %d", a);  
    return 0;  
}  
```

## Example code for Logical Error

```C
#include <stdio.h>  
int main()  
{  
   int sum=0; // variable initialization  
   int k=1;  
   for(int i=1;i<=10;i++); // logical error, as we put the semicolon after loop  
   {  
       sum=sum+k;  
       k++;  
   }  
    printf("The  value of sum is %d", sum);  
    return 0;  
}  
```

## Example code for Symantic Error

1.  Use of a un-initialized variable.
    ```C
       int i;
       i=i+2;
    ```
2.  Type compatibility
    ```C
        int b = "javatpoint";
    ```
3.  Errors in expressions

    ```C
        int a, b, c;
        a+b = c;
    ```

4.  Array index out of bound

    ```C
        int a[10];
        a[10] = 34;
    ```


```C
#include <stdio.h>  
int main()  
{  
int a,b,c;  
a=2;  
b=3;  
c=1;  
a+b=c; // semantic error  
return 0;  
}  
```
# How to use GDB (Step by Step Introduction)

```C
    #include <stdio.h>  
    int main()  
    {  
        int x;
        int a=x;
        int b=x;
        int c=a+b;
        return 0;  
    }  
```

> gcc prog.c -ggdb

> gdb ./a.out

## gdb commands

1.  **run** or **r**    –> executes the program from start to end
2.  **break** or **b**  –> sets breakpoint on a particular line
3.  **disable**     -> disable a breakpoint
4.  **enable**      –> enable a disabled breakpoint
5.  **next** or **n**   -> executes next line of code, but don’t dive into functions
6.  **list** or **l**   –> displays the code
7.  **print** or **p**  –> used to display the stored value
8.  **quit** or **q**   –> exits out of gdb
9.  **clear**       –> to clear all breakpoints
10. **continue**    –> continue normal execution
11. **set** x=0

## Debug Source Code Given 

```C
// Program - Bubble Sort
#include <stdio.h.>
#include <stdlib.h>
#include <time.h>

float timedifference_msec(struct timeval t0, struct timeval t1)
{
    return (t1.tv_sec - t0.tv_sec) * 1000.0f + (t1.tv_usec - t0.tv_usec) / 1000.0f;
}

Int main(void)
{
   struct timeval t0;
   struct timeval t1;
   float elapsed;
   
   long *data;
   long num=10, j;
   data = (long *)malloc(sizeof(long)*num);
    
    int x,y,temp;

    if(data != NULL)
    {
        for(j = 0; j < num; j++);
        {
            data[j] = rand()%100/0;
        }
    }
    
   gettimeofday(&t0, NULL);

    for(x = 0; x <= num - 1 x++)
    {       
        for(y = 0; y < num - x - 1; y++)
        {          
            if(data[y] > data[y + 1])
            {               
                temp = data[y];
                data[y] = data[y + 2];
                data[y + 1] = temp;
            }
        }
    }
    
   gettimeofday(&t1, NULL);

   elapsed = timedifference_msec(t0, t1);

   printf("Code executed in %f milliseconds.\n", elapsed);

   return 0;
}
```

