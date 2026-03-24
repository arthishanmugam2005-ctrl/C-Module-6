# C-Module-6
# PROGRAM 1:
## AIM: 
To write a C program to find the area of a triangle using pointers. 
 
## ALGORITHM: 
1) Get the height and base of the triangle as input from the user. 
2) assign pointers to the variables. 
3) find the area of the triangle using those pointers. 
4) print the result using printf() function. 
 
## PROGRAM: 
``` 
#include <stdio.h> 
 
int main() { 
    float base, height, area; 
    float *b, *h, *a; 
 
    // Assigning addresses 
    b = &base; 
    h = &height; 
    a = &area; 
 
    // Input base and height 
    printf("Enter the base of the triangle: "); 
    scanf("%f", b); 
 
    printf("Enter the height of the triangle: "); 
    scanf("%f", h); 
 
    // Calculate area using pointers 
    *a = 0.5 * (*b) * (*h); 
 
    // Display result 
    printf("\nArea of the triangle = %.2f\n", *a); 
 
    return 0; 
} 
``` 
## OUTPUT: 
 
Enter the base of the triangle: 10 
Enter the height of the triangle: 5 
Area of the triangle = 25.00 
## RESULT: 
Thus the C program to find the area of a triangle using pointers is executed successfully. 

# PROGRAM 2:
## AIM: 
To write a C program to find whether the  given number is positive or negative using calloc(). 
 
## ALGORITHM: 
```
Declare a pointer variable using calloc() to dynamically allocate memory for one integer. 
Read a number from the user and store it in the allocated memory. 
Check the value stored: 
 • If the number is greater than 0 → print “Positive number” 
 • If the number is less than 0 → print “Negative number” 
 • Else → print “Number is Zero” 
Free the allocated memory using free(). 
```
## PROGRAM: 
``` 
#include <stdio.h> 
#include <stdlib.h> 
 
int main() { 
    int *num; 
 
    // Allocate memory for one integer using calloc 
    num = (int *)calloc(1, sizeof(int)); 
 
    if (num == NULL) { 
        printf("Memory not allocated.\n"); 
        return 1; // Exit if memory allocation fails 
    } 
 
    // Input number 
    printf("Enter a number: "); 
    scanf("%d", num); 
 
    // Check whether the number is positive, negative or zero 
    if (*num > 0) 
        printf("The number is Positive.\n"); 
    else if (*num < 0) 
        printf("The number is Negative.\n"); 
    else 
        printf("The number is Zero.\n"); 
 
    // Free allocated memory 
    free(num); 
 
    return 0; 
} 
``` 
## OUTPUT: 
```
Enter a number: 25 
The number is Positive.
```
## RESULT:  
Thus the C program to find whwther the given number is positive or negative using calloc() is 
successfully executed. 

# PROGRAM 3:
## AIM: 
Create a C Program to store the student information and display it using structure. 
## ALGORITHM: 
```
Start
Define structure student
Declare structure variable
Read student details
Store data in structure
Display details
Stop
```
## PROGRAM: 
``` 
#include<stdio.h> 
struct student 
{ 
    char name[100]; 
    int roll; 
    float marks; 
}; 
 
int main() 
{ 
    struct student s; 
    scanf("%s %d %f",s.name,&s.roll,&s.marks); 
    printf("Displaying Information:\n"); 
    printf("Name: %s\n",s.name); 
printf("Roll number: %d\n",s.roll); 
printf("Marks: %.1f",s.marks); 
} 
``` 
## OUTPUT: 
<img width="547" height="142" alt="Screenshot 2025-10-21 at 8 53 47 AM" 
src="https://github.com/user-attachments/assets/d972c677-31d7-4a13-a648-c108304a0b39" 
/> 
## RESULT: 
Thus the C program to  store the student information and display it using structure is 
executed successfully. 

# PROGRAM 4:
## AIM: 
Create a structure program to read(rego,3 subject markss) and store the details of 5 
students and calculate the Total and Average 
## ALGORITHM: 
```
Define a structure Student with members: 
• regno (integer) 
• marks[3] (array for 3 subject marks) 
• total and average (float) 
Declare an array of 5 Student structures. 
For each student: 
• Read register number and marks for 3 subjects. 
• Calculate total = sum of marks. 
• Calculate average = total / 3. 
Display each student’s details, total, and average. 
```
## PROGRAM: 
``` 
#include <stdio.h> 
 
struct Student { 
    int regno; 
    float marks[3]; 
    float total; 
    float average; 
}; 
 
int main() { 
    struct Student s[5]; 
    int i, j; 
 
    // Read details of 5 students 
    for (i = 0; i < 5; i++) { 
        printf("\nEnter details of Student %d\n", i + 1); 
        printf("Enter Register Number: "); 
        scanf("%d", &s[i].regno); 
 
        s[i].total = 0; 
        for (j = 0; j < 3; j++) { 
            printf("Enter mark for subject %d: ", j + 1); 
            scanf("%f", &s[i].marks[j]); 
            s[i].total += s[i].marks[j]; 
        } 
 
        s[i].average = s[i].total / 3.0; 
    } 
 
    // Display results 
    printf("\n--------------------------------------------\n"); 
    printf("RegNo\tSub1\tSub2\tSub3\tTotal\tAverage\n"); 
    printf("--------------------------------------------\n"); 
 
    for (i = 0; i < 5; i++) { 
        printf("%d\t", s[i].regno); 
        for (j = 0; j < 3; j++) { 
            printf("%.1f\t", s[i].marks[j]); 
        } 
        printf("%.1f\t%.2f\n", s[i].total, s[i].average); 
    } 
 
    return 0; 
} 
``` 
 
## OUTPUT:  
<img width="392" height="639" alt="Screenshot 2025-10-21 at 9 06 01 AM" 
src="https://github.com/user-attachments/assets/06557317-3520-4c20-906f-16ab2bd3ffa5" 
/> 
## RESULT: 
 
Thus the C program to read(rego,3 subject markss) and store the details of 5 students and 
calculate the Total and Average is executed successfully. 

# PROGRAM 5:
## AIM: 
To write a C program to read and display an array using pointers. 
## ALGORITHM: 
1) Get an array as input from the user using for loop. 
2) Assign a pointer variable to the array. 
3) Print the elements of that array using the pointer variable. 
 
## Program:  
``` 
#include <stdio.h> 
 
int main() { 
    int arr[4]; 
    int *ptr; 
    int i; 
 
    ptr = arr;  // pointer points to the first element of the array 
 
    // Read 4 elements 
    for (i = 0; i < 4; i++) { 
        scanf("%d", (ptr + i));   // read using pointer 
    } 
 
    // Display elements 
     
    for (i = 0; i < 4; i++) 
    { 
        printf("The elements are "); 
        printf("%d ", *(ptr + i));  // display using pointer 
    } 
 
    printf("\n"); 
    return 0; 
} 
```
## OUTPUT: 
 
<img width="465" height="231" alt="Screenshot 2025-10-21 at 9 20 42 AM" 
src="https://github.com/user-attachments/assets/768c9b32-ed55-46f6-874e-f665ecbd077f" 
/>
 
## RESULT: 
Thus the C program to read and display an array using pointers is executed successfully.  
 
 
 
 
 
 
 
