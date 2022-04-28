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