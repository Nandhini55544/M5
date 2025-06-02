EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
 #include <stdio.h>
 int main() {
 double num = 23.65; 
double *ptr = &num; 
*ptr = 25.0;
 printf("Modified value: %.2f\n", num);
 return 0;
 }
 ```
## OUTPUT:
 	
![image](https://github.com/user-attachments/assets/8dcfadff-fb1d-473e-8067-a33fddfef413)











## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
 #include <stdio.h>
 unsigned long long calculateProduct(int n) {
 if (n == 1) {
 return 1;
 }
  return n * calculateProduct(n - 1); 
}
 int main() {
 int n = 12; 
unsigned long long product;
 product = calculateProduct(n);
 printf("The product of first %d natural numbers is: %llu\n", n, product);
 return 0;
 }
 ```
## OUTPUT:

![image](https://github.com/user-attachments/assets/5da75e38-8a6e-4364-a753-68899c84bd6a)

## RESULT:

Thus the program has been executed successfully.
 
 


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
 int main() {
    int rows, cols;
    printf("Enter number of rows and columns: ");
    scanf("%d %d", &rows, &cols);
    int matrix[rows][cols];
    printf("Enter matrix elements:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }
    printf("Sum of each row:\n");
    for (int i = 0; i < rows; i++) {
        int rowSum = 0;
        for (int j = 0; j < cols; j++) {
            rowSum += matrix[i][j]; 
        }
 printf("Row %d sum: %d\n", i + 1, rowSum);
    }
 return 0;
 }
```
## OUTPUT

![image](https://github.com/user-attachments/assets/ecad5202-790c-44e9-9d2b-c7ef4a15d3ca)

 
 

 ## RESULT
 
Thus the program to find Sum of each row of a Matrix has been executed successfully.

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
    scanf("%s", str);
    int num_rows;
   // printf("Enter number of rows: ");
   // scanf("%d", &num_rows);

   // int len = strlen(str);
    int sp = 10;
    int k = 0;
    int y = 0;

    for (int i = 1; i <= 5; i++) {
        for (int space = 1; space <= sp; space++) {
            printf(" ");
        }

        for (int j = 0; j <= y; j++) {
            printf("%c", str[k]);
            k++;
            if (str[k] == '\0')
                k = 0;
        }

        printf("\n");
        sp -= 1;
        y += 2;
    }

    return 0;
}


 ```
 ## OUTPUT

![image](https://github.com/user-attachments/assets/cc41b3af-ff8d-492b-a443-b19bca71d583)



## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
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

## PROGRAM
```
 #include <stdio.h>
 int main() {
    int arr[6]; 
    int *parr = arr;
    printf("Enter 6 integer elements:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", (parr + i)); 
    }
    printf("Array elements are:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(parr + i)); 
    }
    printf("\n");
     return 0;
 }
 ```
## OUTPUT

 ![image](https://github.com/user-attachments/assets/0598699e-b19a-439b-9de7-a9bdaa27d1f5)


## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


