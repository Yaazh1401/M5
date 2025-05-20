# EX-21-POINTERS
## AIM:
Write a C program to convert a floating point number into an integer:


## ALGORITHM:
Start

Declare a variable num of type float

Declare a variable int_num of type int

Read a floating-point number from the user and store it in num

Typecast num to an int and store the result in int_num

Print the original floating-point number (up to 2 decimal places) and its integer equivalent

End



## PROGRAM:
```
#include <stdio.h>

int main() {
    float num;
    int int_num;
    scanf("%f", &num);
    int_num = (int)num;
    printf("the integer equivalent of %.2f =%d\n", num, int_num);

    return 0;
}
```
## OUTPUT:
 	


![image](https://github.com/user-attachments/assets/eeb0d0dd-983f-44fd-be35-b26eda696db8)









## RESULT:
Thus the program to convert a floating point number into an integer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Sum of first n natural numbers using Recursion

## ALGORITHM:
Start

Define a recursive function sumOfNaturalNumbers(n):

If n == 0, return 0 (base case)

Else, return n + sumOfNaturalNumbers(n - 1)

In the main function:

Declare an integer variable num

Read an integer value from the user and store it in num

Call the recursive function sumOfNaturalNumbers(num) and store the result in sum

Print the value of sum

End
## PROGRAM:
```
#include <stdio.h>
int sumOfNaturalNumbers(int n) {
    if (n == 0) {
        return 0;
    }
    else {
        return n + sumOfNaturalNumbers(n - 1);
    }
}

int main() {
    int num;
    scanf("%d", &num);
        int sum = sumOfNaturalNumbers(num);
        printf("Sum = %d\n", sum);
    
    return 0;
}
```
## OUTPUT:
    ![image](https://github.com/user-attachments/assets/436bb78c-f25a-4b26-a95f-d127a0fd626b)
     		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write a C Program to find Sum of Diagonal Elements of a Matrix[3x3]

## ALGORITHM:
Start

Declare a 3x3 matrix (matrix[3][3])

Declare variables i, j, sum (initialize sum = 0)

Read the number of rows and cols from the user

Input matrix elements:

For i from 0 to rows - 1

For j from 0 to cols - 1

Read matrix[i][j]

Compute sum of diagonal elements:

For i from 0 to 2 (fixed for 3x3)

Print matrix[i][i]

Add matrix[i][i] to sum

Print the total sum of diagonal elements

End

## PROGRAM:
```
#include <stdio.h>

int main() {
    int matrix[3][3];
    int i, j, sum = 0;
    int rows, cols;
    scanf("%d %d", &rows, &cols);
    for(i = 0; i < rows; i++) {
        for(j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }
    for(i = 0; i < 3; i++) {
        printf("%d\n", matrix[i][i]);
        sum += matrix[i][i];
    }
    printf("The Sum of Diagonal Elements of a Matrix =  %d\n", sum);

    return 0;
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/5f51e913-bf79-4339-84f9-4c24819f965a)


 
 

 ## RESULT
 Thus the program has been executed successfully.
 
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows, str_len, index = 0;
    scanf("%s", str);
    scanf("%d", &rows);

    str_len = strlen(str);

    for (int i = 1; i <= rows + 1; i++) {
        printf("  ");
        for (int space = 1; space <= rows + 1 - i; space++) {
            printf(" ");
        }
        for (int j = 1; j <= i; j++) {
            printf("%c ", str[index % str_len]);
            index++;
        }

        printf("\n");
    }

    return 0;
}
```

 ## OUTPUT
![image](https://github.com/user-attachments/assets/a1c74952-284e-4607-8340-028b3a82f38e)

 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a C program to print string 'SAVEETHA' using pointer 

## ALGORITHM
Start

Declare a character array str[100] to store the input string

Declare a character pointer ptr

Read the input string from the user and store it in str

Initialize the pointer ptr to point to the beginning of str

Print the message: "The entered string is :: "

While the character pointed to by ptr is not the null character ('\0'):

Print the character using putchar(*ptr)

Move the pointer to the next character (ptr++)

Print a newline character

End

## PROGRAM
```
#include <stdio.h>

int main() {
    char str[100]; 
    char *ptr;  
    scanf("%s", str);
    ptr = str;
    printf("The entered string is :: ");
    while (*ptr != '\0') {
        putchar(*ptr);
        ptr++;
    }
    printf("\n");

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/c58fef4e-00ee-4acb-aec8-1d5e1a50c5a1)

 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


