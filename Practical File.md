# PROGRAMMING FOR PROBLEM SOLVING

## **_ESC-18104/18105_**

###  **_PRACTICAL FILE_**

### **SUBMITTED BY**

#### **NAME:-**_SHIV PRATAP DUBEY_

#### **ROLL NO.:-** _1914105_

#### **DEPARTMENT:-**_CIVIL_

#### **SECTION:-** _B2_

![logo](https://github.com/Shiv2ubey786/PRACTICA-FILE.md/blob/master/logo.jpg)

 # List of programs
### 1.Addition of two integers
### 2.Average of n numbers
### 3.Weekdays
### 4.Finding Even or Odd
### 5.Multiplication Table
### 6.Checking Armstrong number
### 7.Calculator
### 8.Bubble Sorting
### 9.Binary search
### 10.Factorial of a number
### 11.FizzBuzz
### 12.Sum of 1st 100 positive integers
### 13.Greater of two integers
### 14.Greatest of three integers
### 15.GCD of two integers
### 16.Finding a leap year
### 17.Linear search
### 18.Addition of a matrix
### 19.Transpose of a matrix
### 20.Sum of digits of numbers
### 21.Checking Palindrome
### 22.Swaping of numbers through call by value
### 23.Swaping of numbers through call by refernce
### 24.Entering the details of employee using structures
### 25.Finding product of fractions using structures
# PROGRAMS
# 1.Addition of two integers
```
\\Addition of two integers
#include <stdio.h>

int main()
{
int firstNumber, secondNumber, sumOfTwoNumbers;
    printf("Enter two integers: ");
    scanf("%d %d", &firstNumber, &secondNumber);
    sumOfTwoNumbers = firstNumber + secondNumber;
    printf("%d + %d = %d", firstNumber, secondNumber, sumOfTwoNumbers);
return 0;
}
```
## Output:
```
Enter two integers:2
3
2+3=5
```
# 2.Average of n numbers
```
\\Average of n numbers
#include<stdio.h>

int main()
{
    int n, i;
    float sum = 0, x;

    printf("Enter number of elements:  ");
    scanf("%d", &n);
    printf("\n\n\nEnter %d elements\n\n", n);
    for(i = 0; i < n; i++)
    {
        scanf("%f", &x);
        sum += x;
    }
    printf("\n\n\nAverage of the entered numbers is =  %f", (sum/n));
    return 0;
}
```
## Output:
```                                                                                                                                                                                                                                   
Enter number of elements:  4                                                                                                                    
                                                                                                                                                
                                                                                                                                                
                                                                                                                                                
Enter 4 elements                                                                                                                                
                                                                                                                                                
1                                                                                                                                               
2                                                                                                                                               
3                                                                                                                                               
4                                                                                                                                               
                                                                                                                                                
                                                                                                                                                
                                                                                                                                                
Average of the entered numbers is =  2.500000 
```
# 3.Weekdays
```
#include<stdio.h>
int main()
{
int code;
printf("Enter weekdays in number");
scanf("%d",&code);
if(code == 1)
printf("Sunday");
else if(code == 2)
printf("Monday");
else if(code == 3)
printf("Tuesday");
else if(code == 4) 
printf("Wednesday");
else if(code==5)
printf("Thursday");
else if(code==6)
printf("Friday");
else if(code==7)
printf("Saturday");
else
printf("invalid code");
return 0;
}
```
## Output:
```
Enter weekdays in number5                                                                                                                       
Thursday                                                                                                                                        
```    
# 4.Finding Even or Odd
```
#include<stdio.h>
int main()
{
int a;
printf("Enter any value of a:");
scanf("%d",&a);
if(a%2 == 0)
printf("a is even");
else
printf("a is odd");
return 0;
}
```
## Output:
```
Enter any value of a:18                                                                                                                         
a is even                                                                                                                                       
```                    
# 5.Multiplication Table
```
#include <stdio.h>
int main()
{
    int n, i;
    printf("Enter an integer: ");
    scanf("%d",&n);
    for(i=1; i<=10; ++i)
    {
        printf("%d * %d = %d \n", n, i, n*i);
    }
    
    return 0;
}
```
## Output:
```
Enter an integer: 5                                                                                                                             
5 * 1 = 5                                                                                                                                       
5 * 2 = 10                                                                                                                                      
5 * 3 = 15                                                                                                                                      
5 * 4 = 20                                                                                                                                      
5 * 5 = 25                                                                                                                                      
5 * 6 = 30                                                                                                                                      
5 * 7 = 35                                                                                                                                      
5 * 8 = 40                                                                                                                                      
5 * 9 = 45                                                                                                                                      
5 * 10 = 50 
```
# 6.Checking Armstrong number
```
#include <stdio.h>
#include <math.h>
int main()
{
    int number, originalNumber, remainder, result = 0, n = 0 ;
    printf("Enter an integer: ");
    scanf("%d", &number);
     originalNumber = number;
    
    while (originalNumber != 0)
    {
        originalNumber /= 10;
        ++n;
    }
    
    originalNumber = number;
    while (originalNumber != 0)
    {
        remainder = originalNumber%10;
        result += pow(remainder, n);
        originalNumber /= 10;
    }
    if(result == number)
        printf("%d is an Armstrong number.", number);
    else
        printf("%d is not an Armstrong number.", number);
    return 0;
}
```
## Output:
```
Enter an integer: 153                                                                                                                           
153 is an Armstrong number.                                                                                                                     
```
# 7.Calculator
```
// Performs addition, subtraction, multiplication or division depending the input from user
# include <stdio.h>
int main() {
    char operator;
    double firstNumber,secondNumber;
    printf("Enter an operator (+, -, *,): ");
    scanf("%c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf",&firstNumber, &secondNumber);
    switch(operator)
    {
        case '+':
            printf("%.1lf + %.1lf = %.1lf",firstNumber, secondNumber, firstNumber + secondNumber);
            break;
        case '-':
            printf("%.1lf - %.1lf = %.1lf",firstNumber, secondNumber, firstNumber - secondNumber);
            break;
        case '*':
            printf("%.1lf * %.1lf = %.1lf",firstNumber, secondNumber, firstNumber * secondNumber);
            break;
        case '/':
            printf("%.1lf / %.1lf = %.1lf",firstNumber, secondNumber, firstNumber / secondNumber);
            break;
        // operator doesn't match any case constant (+, -, *, /)
        default:
            printf("Error! operator is not correct");
    }
    
    return 0;
}
```
## Output:
```
Enter an operator (+, -, *,): *
Enter two operands: 1.5
4.5
1.5 * 4.5 = 6.8
```
# 8.Bubble Sorting
```
#include <stdio.h>
 
int main()
{
  int array[100], n, c, d, swap;
 
  printf("Enter number of elements\n");
  scanf("%d", &n);
 
  printf("Enter %d integers\n", n);
 
  for (c = 0; c < n; c++)
    scanf("%d", &array[c]);
 
  for (c = 0 ; c < n - 1; c++)
  {
    for (d = 0 ; d < n - c - 1; d++)
    {
      if (array[d] > array[d+1]) /* For decreasing order use < */
      {
        swap       = array[d];
        array[d]   = array[d+1];
        array[d+1] = swap;
      }
    }
  }
 
  printf("Sorted list in ascending order:\n");
 
  for (c = 0; c < n; c++)
     printf("%d\n", array[c]);
 
  return 0;
}
```
## Output:
```
Enter number of elements                                                                                                                        
5                                                                                                                                               
Enter 5 integers                                                                                                                                
59                                                                                                                                              
17                                                                                                                                              
98                                                                                                                                              
456                                                                                                                                             
8                                                                                                                                               
Sorted list in ascending order:                                                                                                                 
8                                                                                                                                               
17                                                                                                                                              
59                                                                                                                                              
98                                                                                                                                              
456   
```
# 9.Binary search
```
#include <stdio.h>
 
int main()
{
   int c, first, last, middle, n, search, array[100];
 
   printf("Enter number of elements\n");
   scanf("%d",&n);
 
   printf("Enter %d integers\n", n);
 
   for (c = 0; c < n; c++)
      scanf("%d",&array[c]);
 
   printf("Enter value to find\n");
   scanf("%d", &search);
 
   first = 0;
   last = n - 1;
   middle = (first+last)/2;
 
   while (first <= last) {
      if (array[middle] < search)
         first = middle + 1;    
      else if (array[middle] == search) {
         printf("%d found at location %d.\n", search, middle+1);
         break;
      }
      else
         last = middle - 1;
 
      middle = (first + last)/2;
   }
   if (first > last)
      printf("Not found! %d isn't present in the list.\n", search);
 
   return 0;  
}
```
## Output:
```
Enter number of elements                                                                                                                        
5                                                                                                                                               
Enter 5 integers                                                                                                                                
15                                                                                                                                              
95                                                                                                                                              
65                                                                                                                                              
555                                                                                                                                             
85                                                                                                                                              
Enter value to find                                                                                                                             
15                                                                                                                                              
15 found at location 1.                                                                                                                         
```     
# 10.Factorial of a number
```
#include <stdio.h>
int main()
{
int c, n, fact = 1;
printf("Enter a number to calculate its factorial\n");
scanf("%d", &n);
for (c = 1; c <= n; c++)
fact = fact * c;
printf("Factorial of %d = %d\n", n, fact);
return 0;
}
```
## Output:
```
Enter a number to calculate its factorial                                                                                                     
9                                                                                                                                             
Factorial of 9 = 362880             
```
# 11.FizzBuzz
```
#include<stdio.h>
int main()
{
int FizzBuzz;
printf("Enter any number");
scanf("%d",&FizzBuzz);
if (FizzBuzz%15 == 0)
printf("FizzBuzz");
else if (FizzBuzz%3 == 0)
printf("Fizz");
else if (FizzBuzz%5 == 0)
printf("Buzz");
return 0;
}   
```
## Output:
```
Enter any number81                                                                                                                            
Fizz                
```
# 12.Sum of 1st 100 positive integers
```
#include<stdio.h>
int main()
{
int Sum=0,number;
number=1;
while(number<=100)
{
Sum+=number;
number++;
}
printf("Sum of first 100 positive integer numbers=%d\n",Sum);
return 0;
}
````
## Output:
```
Sum of first 100 positive integer numbers=5050 
```
# 13.Greater of two integers
```
#include<stdio.h>
int main()
{
int a,b;
printf("Enter any two number");
scanf("%d %d",&a,&b);
if(a>b)
{
printf("a is greater");
}
else
{
printf("b is greater");
}
return 0;
}
```
## Output:
```
Enter any two number5                                                                                                                         
6                                                                                                                                             
6 is greater    
```
# 14.Greatest of three integers
```
#include <stdio.h>
int main()
{
    double n1, n2, n3;
    printf("Enter three different numbers: ");
    scanf("%lf %lf %lf", &n1, &n2, &n3);
    if( n1>=n2 && n1>=n3 )
        printf("%.2f is the largest number.", n1);
    if( n2>=n1 && n2>=n3 )
        printf("%.2f is the largest number.", n2);
    if( n3>=n1 && n3>=n2 )
        printf("%.2f is the largest number.", n3);
    return 0;
}
```
## Output:
```
Enter three different numbers: 10                                                                                                             
15                                                                                                                                            
20                                                                                                                                            
20.00 is the largest number.    
```
# 15.GCD of two integers
```
#include <stdio.h>
int main()
{
    int n1, n2, i, gcd;
    printf("Enter two integers: ");
    scanf("%d %d", &n1, &n2);
    for(i=1; i <= n1 && i <= n2; ++i)
    {
        // Checks if i is factor of both integers
        if(n1%i==0 && n2%i==0)
            gcd = i;
    }
    printf("G.C.D of %d and %d is %d", n1, n2, gcd);
    return 0;
}
```
## Output:
```
Enter two integers: 15                                                                                                                          
45                                                                                                                                              
G.C.D of 15 and 45 is 15 
```
# 16.Finding a leap year
```
#include <stdio.h>
 
int main()
{
  int year;
 
  printf("Enter a year to check if it is a leap year\n");
  scanf("%d", &year);
 
  if (year%400 == 0) // Exactly divisible by 400 e.g. 1600, 2000
    printf("%d is a leap year.\n", year);
  else if (year%100 == 0) // Exactly divisible by 100 and not by 400 e.g. 1900, 2100
    printf("%d isn't a leap year.\n", year);
  else if (year%4 == 0) // Exactly divisible by 4 and neither by 100 nor 400 e.g. 2020
    printf("%d is a leap year.\n", year);
  else // Not divisible by 4 or 100 or 400 e.g. 2017, 2018, 2019
    printf("%d isn't a leap year.\n", year);  
   
  return 0;
}
```
## Output:
```
Enter a year to check if it is a leap year                                                                                                    
2002                                                                                                                                          
2002 isn't a leap year.                   
```
# 17.Linear search
```
#include <stdio.h>
void main()
{
    int a[10], i, item;
    printf("\nEnter SEVEN elements of an array:\n");
    for (i=0; i<=6; i++)
        scanf("%d", &a[i]);
    printf("\nEnter item to search: ");
    scanf("%d", &item);
    for (i=0; i<=9; i++)
        if (item == a[i])
        {
            printf("\nItem found at location %d", i+1);
            break;
        }
    if (i > 9)
        printf("\nItem does not exist.");
    getch();
}
```
## Output:
```
Enter SEVEN elements of an array:                                                                                                               
15                                                                                                                                              
1                                                                                                                                               
89                                                                                                                                              
95                                                                                                                                              
158                                                                                                                                             
45                                                                                                                                              
73                                                                                                                                              
                                                                                                                                                
Enter item to search: 158                                                                                                                       
                                                                                                                                                
Item found at location 5  
```
# 18.Addtion of matrix
```
#include <stdio.h>
int main(){
    int r, c, a[100][100], b[100][100], sum[100][100], i, j;
    printf("Enter number of rows (between 1 and 100): ");
    scanf("%d", &r);
    printf("Enter number of columns (between 1 and 100): ");
    scanf("%d", &c);
    printf("\nEnter elements of 1st matrix:\n");
    for(i=0; i<r; ++i)
        for(j=0; j<c; ++j)
        {
            printf("Enter element a%d%d: ",i+1,j+1);
            scanf("%d",&a[i][j]);
        }
    printf("Enter elements of 2nd matrix:\n");
    for(i=0; i<r; ++i)
        for(j=0; j<c; ++j)
        {
            printf("Enter element a%d%d: ",i+1, j+1);
            scanf("%d", &b[i][j]);
        }
    // Adding Two matrices
    for(i=0;i<r;++i)
        for(j=0;j<c;++j)
        {
            sum[i][j]=a[i][j]+b[i][j];
        }
    // Displaying the result
    printf("\nSum of two matrices: \n");
    for(i=0;i<r;++i)
        for(j=0;j<c;++j)
        {
            printf("%d   ",sum[i][j]);
            if(j==c-1)
            {
                printf("\n\n");
            }
        }
    
    return 0;
}
```
## Output:
```
Enter number of rows (between 1 and 100): 3                                                                                                     
Enter number of columns (between 1 and 100): 3                                                                                                  
                                                                                                                                                
Enter elements of 1st matrix:                                                                                                                   
Enter element a11: 5                                                                                                                            
Enter element a12: -7                                                                                                                           
Enter element a13: 69                                                                                                                           
Enter element a21: -10                                                                                                                          
Enter element a22: -1                                                                                                                           
Enter element a23: 68                                                                                                                           
Enter element a31: -70                                                                                                                          
Enter element a32: -68                                                                                                                          
Enter element a33: 99                                                                                                                           
Enter elements of 2nd matrix:                                                                                                                   
Enter element a11: 65                                                                                                                           
Enter element a12: 58                                                                                                                           
Enter element a13: 12                                                                                                                           
Enter element a21: 35                                                                                                                           
Enter element a22: 94                                                                                                                           
Enter element a23: 76                                                                                                                           
Enter element a31: 150                                                                                                                          
Enter element a32: 68                                                                                                                           
Enter element a33: 16

Sum of two matrices:                                                                                                                            
70   51   81                                                                                                                                    
                                                                                                                                                
25   93   144                                                                                                                                   
                                                                                                                                                
80   0   115    
```
# 19.Transpose of a matrix
```
#include <stdio.h>
int main()
{
    int a[10][10], transpose[10][10], r, c, i, j;
    printf("Enter rows and columns of matrix: ");
    scanf("%d %d", &r, &c);
    // Storing elements of the matrix
    printf("\nEnter elements of matrix:\n");
    for(i=0; i<r; ++i)
        for(j=0; j<c; ++j)
        {
            printf("Enter element a%d%d: ",i+1, j+1);
            scanf("%d", &a[i][j]);
        }
    // Displaying the matrix a[][] */
    printf("\nEntered Matrix: \n");
    for(i=0; i<r; ++i)
        for(j=0; j<c; ++j)
        {
            printf("%d  ", a[i][j]);
            if (j == c-1)
                printf("\n\n");
        }
    // Finding the transpose of matrix a
    for(i=0; i<r; ++i)
        for(j=0; j<c; ++j)
        {
            transpose[j][i] = a[i][j];
        }
    // Displaying the transpose of matrix a
    printf("\nTranspose of Matrix:\n");
    for(i=0; i<c; ++i)
        for(j=0; j<r; ++j)
        {
            printf("%d  ",transpose[i][j]);
            if(j==r-1)
                printf("\n\n");
        }
    return 0;
}
```
## Output:
```
Enter rows and columns of matrix: 2                                                                                                             
2                                                                                                                                               
                                                                                                                                                
Enter elements of matrix:                                                                                                                       
Enter element a11: 15                                                                                                                           
Enter element a12: -15                                                                                                                          
Enter element a21: 11                                                                                                                           
Enter element a22: -11                                                                                                                          
                                                                                                                                                
Entered Matrix:                                                                                                                                 
15  -15                                                                                                                                         
                                                                                                                                                
11  -11                                                                                                                                         
                                                                                                                                                
                                                                                                                                                
Transpose of Matrix:                                                                                                                            
15  11                                                                                                                                          
                                                                                                                                                
-15  -11                                                                                                                                        
```
# 20.Sum of digits of numbers
```
#include<stdio.h>
int main()
{
int Sum=0,digit;
long number,temp;
number=1;
printf("Enter any positive integer");
scanf("%d",&number);
temp=number;
while(temp>0)
{
digit=temp%10;
temp /= 10;
Sum+=digit;
}
printf("\n Sum of digits of %d=%d\n",number,Sum);
return 0;
}

```
## Output:
```
Enter any positive integer1532684                                                                                                             
                                                                                                                                              
 Sum of digits of 1532684=29                                                                                                                  
```
# 21. Checking Palindrome
```
#include <stdio.h>

int main()
{
int n, reverse = 0, temp;

printf("Enter a number to check if it is a palindrome or not\n");
scanf("%d",&n);

temp = n;

while( temp != 0 )
{
reverse = reverse * 10;
reverse = reverse + temp%10;
temp = temp/10;
}
/*Taking reverse of the given no
see reverse no program*/

if ( n == reverse )
/*if reverse is same as n*/
printf("%d is a palindrome number.\n", n);
else
printf("%d is not a palindrome number.\n", n);

return 0;
}
```
## Output:
```
Enter a number to check if it is a palindrome or not                                                                                          
15366351                                                                                                                                      
15366351 is a palindrome number.                                                                                                              
```
# 22.Swaping of numbers through call by value
```
#include <stdio.h>
 
int main()
{
  int x, y, t;
 
  printf("Enter two integers\n");
  scanf("%d%d", &x, &y);
 
  printf("Before Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);
 
  t = x;
  x = y;
  y = t;
 
  printf("After Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);
 
  return 0;
}
```
## Output:
```
Enter two integers                                                                                                                              
69                                                                                                                                              
96                                                                                                                                              
Before Swapping                                                                                                                                 
First integer = 69                                                                                                                              
Second integer = 96                                                                                                                             
After Swapping                                                                                                                                  
First integer = 96                                                                                                                              
Second integer = 69                                                                                                                             
```
# 23.Swaping of numbers through call by refernce
```
#include <stdio.h>

void swap(int * num1, int * num2);

int main()
{
    int num1, num2;

    printf("Enter two numbers: ");
    scanf("%d%d", &num1, &num2);

    printf("Before swapping in main n");
    printf("Value of num1 = %d \n", num1);
    printf("Value of num2 = %d \n\n", num2);

    swap(&num1, &num2);

    printf("After swapping in main n");
    printf("Value of num1 = %d \n", num1);
    printf("Value of num2 = %d \n\n", num2);

    return 0;
}


void swap(int * num1, int * num2)
{
    int temp;

    // Copy the value of num1 to some temp variable
    temp = *num1;

    // Copy the value of num2 to num1
    *num1= *num2;

    // Copy the value of num1 stored in temp to num2
    *num2= temp;

    printf("After swapping in swap function n");
    printf("Value of num1 = %d \n", *num1);
    printf("Value of num2 = %d \n\n", *num2);
}
```
## Output:
```
Enter two numbers: 69                                                                                                                           
96                                                                                                                                              
Before swapping in main nValue of num1 = 69                                                                                                     
Value of num2 = 96                                                                                                                              
                                                                                                                                                
After swapping in swap function nValue of num1 = 96                                                                                             
Value of num2 = 69                                                                                                                              
                                                                                                                                                
After swapping in main nValue of num1 = 96                                                                                                      
Value of num2 = 69                                                                                                                              
```
# 24.Entering the details of employee using structures 
```
#include <stdio.h>
 
/*structure declaration*/
struct employee{
    char    name[30];
    int     empId;
    float   salary;
};
 
int main()
{
    /*declare structure variable*/
    struct employee emp;
     
    /*read employee details*/
    printf("\nEnter details :\n");
    printf("Name ?:");          gets(emp.name);
    printf("ID ?:");            scanf("%d",&emp.empId);
    printf("Salary ?:");        scanf("%f",&emp.salary);
     
    /*print employee details*/
    printf("\nEntered detail is:");
    printf("Name: %s"   ,emp.name);
    printf("Id: %d"     ,emp.empId);
    printf("Salary: %f\n",emp.salary);
    return 0;
}
```
## Output:
```
Enter details :                                                                                                                                 
Name ?:saaho                                                                                                                                    
ID ?:777                                                                                                                                        
Salary ?:30000                                                                                                                         
                                                                                                                                                
Entered detail is:Name:saaho Id:777 Salary: 30000
```
# 25.Finding product of fractions using structures
```
#include<stdio.h>
struct fraction
{
 int num;
 int den;
};
int main()
{
 int rnum,rden;
 struct fraction f1,f2; 
     printf("enter numerator and denominator of first fraction\n");
     scanf("%d%d",&f1.num,&f1.den);
     printf("enter numerator and denominator of second fraction\n");
     scanf("%d%d",&f2.num,&f2.den); 
     rnum=f1.num*f2.num;
     rden=f1.den*f2.den;
 printf("\nproduct is : %d/%d\n",rnum,rden);
}
```
## Output:
```
enter numerator and denominator of first fraction                                                                                               
5                                                                                                                                               
6                                                                                                                                               
enter numerator and denominator of second fraction                                                                                              
6                                                                                                                                               
7                                                                                                                                               
                                                                                                                                                
product is : 30/42                    
```

 
 




