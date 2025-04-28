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
int main() 
{ 
    int length, breadth, area; 
    int *ptrLength, *ptrBreadth; 
    scanf("%d", &length); 
    scanf("%d", &breadth); 
    ptrLength = &length; 
    ptrBreadth = &breadth; 
    area = (*ptrLength) * (*ptrBreadth); 
    printf("The area of the rectangle is: %d\n", area); 
    return 0; 
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/39a31dd0-a27d-4985-a0a3-1ce01b3130d9)

		       	


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
int main() 
{ 
    char *str; 
    str = (char *)malloc(8 * sizeof(char)); 
    if (str == NULL) 
    { 
        printf("Memory allocation failed.\n"); 
        return 1; 
    } 
    sprintf(str, "SAVEETHA"); 
    printf("The string is: %s\n", str); 
    free(str); 
    return 0; 
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/1dedb6e2-93b1-43ca-a7e2-5b8fa9a90012)




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
struct Student 
{ 
    char name [50]; 
    int rollNumber; 
    float marks; 
}; 
int main() 
{ 
    struct Student student; 
    fgets(student.name, sizeof(student.name), stdin); 
    scanf("%d", &student.rollNumber); 
    scanf("%f", &student.marks); 
    printf("\nStudent Information:\n"); 
    printf("Name: %s", student.name); 
    printf("Roll Number: %d\n", student.rollNumber); 
    printf("Marks: %.2f\n", student.marks); 
    return 0; 
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/b394af2a-7072-4577-bccd-2c19f730e3f2)



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
    char name [50]; 
    int id; 
    float basicSalary; 
    float grossSalary; 
}; 
int main() { 
    struct Employee employees [3]; 
    int i; 
    for (i = 0; i < 3; i++) 
    { 
    fgets(employees[i].name, sizeof(employees[i].name), stdin); 
    scanf("%d", &employees[i].id); 
    scanf("%f", &employees[i].basicSalary); 
    employees[i].grossSalary = employees[i].basicSalary + (0.20* employees[i] .basicSalary) + (0.10 * employees[i].basicSalary);
    getchar(); 
    } 
    printf("\nEmployee Details and Gross Salary:\n"); 
    for (i = 0; i < 3; i++) { 
    printf("\nEmployee %d\n", i + 1); 
    printf("Name: %s", employees[i].name); 
    printf("ID: %d\n", employees[i].id); 
    printf("Basic Salary: %.2f\n", employees[i].basicSalary); 
    printf("Gross Salary: %.2f\n", employees[i].grossSalary); 
    } 
    return 0; 
}
```

 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/57979d9a-e06d-49c9-ad84-ce600d4d4e9f)


 

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
};

int main() {
    struct student s[2];
    int i, j;

    for (i = 0; i < 2; i++) {
        printf("Enter name and roll number for student %d:\n", i + 1);
        scanf("%s", s[i].name);
        scanf("%d", &s[i].rollno);

        printf("Enter marks for 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    for (i = 0; i < 2; i++) {
        printf("\nStudent Name: %s\n", s[i].name);
        printf("Roll Number: %d\n", s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].total / 5.0);
    }

    return 0;
}

```


## OUTPUT
![image](https://github.com/user-attachments/assets/3b7ff221-76b4-48fb-a420-52d5101d2a4b)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


