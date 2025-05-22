EX-21-POINTERS
# AIM:
Write a C program to check whether the number 555 is even number or odd number using pointers. 

## ALGORITHM:
1.Start.
2.Declare an integer variable and assign it the value 555.
3.Declare a pointer and point it to the integer variable.
4.Use the pointer to access the value and check if it is divisible by 2 using modulus operator (% 2).
5.If remainder is 0, it's even; otherwise, it's odd.
6.Display the result.
7.End.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int num;
    scanf("%d",&num);
    int *ptr = &num;
    if (*ptr % 2 == 0) {
        printf("%d is even.\n", *ptr);
    } else {
        printf("%d is odd.\n", *ptr);
    }

    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/b6b4c22a-d21c-4f0d-8656-5aabd2e56d50)
 	
## RESULT:
Thus the program to check whether the number 555 is even number or odd number using pointers has been executed successfully.
 
# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the power for 8,4 using recursion.

## ALGORITHM:
1.Start.
2.Define a recursive function power(base, exponent):
3.If exponent is 0, return 1 (base case).
4.Else, return base * power(base, exponent - 1).
5.In the main() function, set base = 8 and exponent = 4.
6.Call the recursive function and store the result.
7.Display the result.
8.End.

## PROGRAM:
```
#include<stdio.h>
int power(int base, int exponent){
    if(exponent==0)
        return 1;
    else
        return base*power(base,exponent-1);
}
int main()
{
    int base=8;
    int exponent=4;
    int result=power(base,exponent);
    printf("%d^%d = %d",base,exponent,result);
    return 0;
}
```
## OUTPUT:
 ![image](https://github.com/user-attachments/assets/2eef0cf6-9fef-4b4e-9a58-91dbcd234eaf)
        		
## RESULT:
Thus the program to calculate the power for 8,4 using recursion has been executed successfully.
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int rows,cols;
    scanf("%d %d",&rows,&cols);
    int matrix[rows][cols];
    for(int i=0; i<rows;i++){
        for(int j=0;j<cols;j++){
            scanf("%d",&matrix[i][j]);
        }
    }
    for(int i=0;i<rows;i++){
        int rowsum=0;
        for(int j=0;j<cols;j++){
            rowsum+=matrix[i][j];
        }
    printf("The Sum of Elements of a Rows in a Matrix:  %d\n",rowsum);
    }
    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/bb594545-0565-4148-9211-83d3f8f13ac4)

## RESULT
Thus the C program to find Sum of each row of a Matrix has been executed successfully.


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. 
Enter a string: PROGRAM 
Enter number of rows: 5 
      P
     R O
    G R A
   M P R O
  G R A M P
 R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include<stdio.h>
int main()
{
   char str[20];
   int n, a=0;
   scanf("%[^\n]", str);
   scanf("%d", &n);
   for(int i=0;i<=n;i++)
   {
     for(int j=0;j<=n-i;j++) 
     printf(" "); 
     for(int k=0;k<=i;k++)
     {
        printf("%2c", str[a++]);
        if(str[a]=='\0') a=0;
     }
     printf("\n");
   }
   return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/16350927-5d8d-4102-a8a2-bbfbeee78099)

## RESULT

Thus the C program to print the given pyramid pattern has been executed successfully.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 7 integer elements using pointer

## ALGORITHM
```
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.
```
## PROGRAM
```
#include<stdio.h>
int main()
{
    int i,n;
    scanf("%d",&n);
    int a[n];
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    int *p;
    p=a;
    for(i=0;i<n;i++){
        printf("the elements are %d\n",*p);
        p++;
    }
    return 0;
}
## OUTPUT
```

## RESULT

Thus the C program to read and display an array of any 7 integer elements using pointer has been executed


