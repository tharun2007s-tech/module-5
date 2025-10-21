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
    int length, breadth, area;
    int *pLength, *pBreadth;

    scanf("%d %d", &length, &breadth);

    pLength = &length;
    pBreadth = &breadth;

    area = (*pLength) * (*pBreadth);

    printf("Area of rectangle = %d\n", area);

    return 0;
}
```
## OUTPUT
		       	
![alt text](<Screenshot (72).png>)

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

int main() {
    char *ptr;

    ptr = (char *)malloc(8 * sizeof(char));

    if (ptr != NULL) {
        ptr[0] = 'W';
        ptr[1] = 'E';
        ptr[2] = 'L';
        ptr[3] = 'C';
        ptr[4] = 'O';
        ptr[5] = 'M';
        ptr[6] = 'E';
        ptr[7] = '\0';

        printf("%s\n", ptr);

        free(ptr);
    }

    return 0;
}
```
## OUTPUT

![alt text](<Screenshot (73).png>)

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
    char name[20];
    long int rollNumber;
    float marks;
};

int main() {
    struct Student s;

    fgets(s.name, sizeof(s.name), stdin);
    scanf("%li", &s.rollNumber);
    scanf("%f", &s.marks);
    printf("\n");
    printf("Name: %s", s.name);
    printf("Roll Number: %li\n", s.rollNumber);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```

## OUTPUT

![alt text](<Screenshot (74).png>)
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
    char name[20];
    int id;
    float basic, hra, da, gross;
};

int main() {
    struct Employee e[3];
    int i;

    for (i = 0; i < 3; i++) {
        scanf("%s", e[i].name);
        scanf("%d", &e[i].id);
        scanf("%f %f %f", &e[i].basic, &e[i].hra, &e[i].da);

        e[i].gross = e[i].basic + e[i].hra + e[i].da;
    }

    for (i = 0; i < 3; i++) {
        printf("Employee %d: %s, ID: %d, Gross Salary: %.2f\n", i + 1, e[i].name, e[i].id, e[i].gross);
    }

    return 0;
}
```

 ## OUTPUT

 ![alt text](<Screenshot (75).png>)

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

struct Student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct Student s[2];
    int i, j;

    for (i = 0; i < 2; i++) {
        scanf("%d", &s[i].rollno);

        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }

        s[i].total = 0;

        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    for (i = 0; i < 2; i++) {
        printf("Total marks of student %d: %d\n", i + 1, s[i].total);
        printf("Average: %.2f\n", s[i].total / 5.0);
    }

    return 0;
}
```

## OUTPUT

 ![alt text](<Screenshot (76).png>)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


