# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int length, breadth;
    int *ptrLength, *ptrBreadth;

    printf("Enter the length of rectangle: ");
    scanf("%d", &length);
    printf("Enter the breadth of rectangle: ");
    scanf("%d", &breadth);

    ptrLength = &length;
    ptrBreadth = &breadth;

    int area = (*ptrLength) * (*ptrBreadth);
    printf("Area of the rectangle = %d\n", area);

    return 0;
}
```

## OUTPUT
```
Enter the length of rectangle: 5  
Enter the breadth of rectangle: 4  
Area of the rectangle = 20
```
		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str;

    str = (char *)malloc(10 * sizeof(char)); 

    if (str == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }

    strcpy(str, "WELCOME");
    printf("%s\n", str);

    free(str); 
    return 0;
}
```

## OUTPUT
```
WELCOME
```



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Student {
    char name[50];
    int rollNo;
    float marks;
};

int main() {
    struct Student s;

    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.rollNo);
    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll No: %d\n", s.rollNo);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```


## OUTPUT
```
Enter student name: Ravi  
Enter roll number: 101  
Enter marks: 87.5  

Student Information:  
Name: Ravi  
Roll No: 101  
Marks: 87.50
```


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    float basic, da, hra, gross;
};

int main() {
    struct Employee e[3];
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for employee %d:\n", i + 1);
        printf("Name: ");
        scanf("%s", e[i].name);
        printf("ID: ");
        scanf("%d", &e[i].id);
        printf("Basic Salary: ");
        scanf("%f", &e[i].basic);
        printf("DA: ");
        scanf("%f", &e[i].da);
        printf("HRA: ");
        scanf("%f", &e[i].hra);

        e[i].gross = e[i].basic + e[i].da + e[i].hra;
    }

    printf("\nEmployee Details:\n");
    for (int i = 0; i < 3; i++) {
        printf("\nName: %s\nID: %d\nGross Salary: %.2f\n", e[i].name, e[i].id, e[i].gross);
    }

    return 0;
}
```


 ## OUTPUT
```
Enter details for employee 1:  
Name: John  
ID: 101  
Basic Salary: 10000  
DA: 2000  
HRA: 1500  

Enter details for employee 2:  
Name: Mary  
ID: 102  
Basic Salary: 12000  
DA: 2500  
HRA: 1800  

Enter details for employee 3:  
Name: Alan  
ID: 103  
Basic Salary: 11000  
DA: 2100  
HRA: 1700  

Employee Details:  
Name: John  
ID: 101  
Gross Salary: 13500.00  

Name: Mary  
ID: 102  
Gross Salary: 16300.00  

Name: Alan  
ID: 103  
Gross Salary: 14800.00
```
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};

int main() {
    struct student s[2];
    int i, j;

    for (i = 0; i < 2; i++) {
        printf("Enter name for student %d: ", i + 1);
        scanf("%s", s[i].name);
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter marks for 5 subjects:\n");
        s[i].total = 0;

        for (j = 0; j < 5; j++) {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }

        s[i].average = s[i].total / 5.0;
    }

    printf("\nStudent Results:\n");
    for (i = 0; i < 2; i++) {
        printf("Name: %s\n", s[i].name);
        printf("Roll No: %d\n", s[i].rollno);
        printf("Total: %d\n", s[i].total);
        printf("Average: %.2f\n\n", s[i].average);
    }

    return 0;
}
```



## OUTPUT
```
Enter name for student 1: Sam  
Enter roll number: 1  
Enter marks for 5 subjects:  
Subject 1: 75  
Subject 2: 80  
Subject 3: 65  
Subject 4: 70  
Subject 5: 60  

Enter name for student 2: Alex  
Enter roll number: 2  
Enter marks for 5 subjects:  
Subject 1: 85  
Subject 2: 90  
Subject 3: 88  
Subject 4: 92  
Subject 5: 91  

Student Results:  
Name: Sam  
Roll No: 1  
Total: 350  
Average: 70.00  

Name: Alex  
Roll No: 2  
Total: 446  
Average: 89.20

```


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


