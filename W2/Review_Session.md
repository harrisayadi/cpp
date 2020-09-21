
# Review Session for Section 7, 8 and 9 (C76-C81)

## Correction and Clarification
- In Component 55 of Section 7, there is an error in the code. The code examples in this video show the declaration of `days_in_year` as follows: 
```cpp
const double days_in_year {365};
``` 
This is incorrect. The type of `days_in_year` should be `int` since it is being used to declare the size of the array `hi_temperatures`.The correct declaration should be:
```cpp
const int days_in_year {365};
```

- `enum` type is introduced in Component 80 and has not been explained in detail. You can refer to https://www.programiz.com/cpp-programming/enumeration


<!---
- Summary of the process of translating a C++ source file into an executable file 
![alt text](./img/theprocess.PNG "Logo Title Text 1")

-->

## Review Questions
Q1. Assume `value` is an integer variable. If the user enters 3.14 in response to the
following programming statement, what will be stored in value ?

`cin >> value;`

A) 3.14

B) 3

C) 0

D) Nothing. An error message is displayed.

Q2. The following program will run, but the user will have difficulty understanding what to do. How would you improve the program?
``` cpp
// This program multiplies two numbers and displays the result.
#include <iostream>
using namespace std;
int main()
{
double first, second, product;
cin >> first >> second;
product = first * second;
cout << product;
return 0;
}
```

Q3. What's the value of the following expression: `5 + 19 % 3 − 1`

Q4. Complete the following program skeleton so it displays the volume of a cylindrical fuel tank. The formula for the volume of a cylinder is

Volume = π* r^2 *h

where

π is 3.14159

r is the radius of the tank

h is the height of the tank

``` cpp
#include <iostream>
#include <cmath>
using namespace std;
int main()
{
  double volume, radius, height;
  cout << "This program will tell you the volume of\n";
  cout << "a cylinder-shaped fuel tank.\n";
  cout << "How tall is the tank? ";
  cin >> height;
  cout << "What is the radius of the tank? ";
  cin >> radius;
  // You must complete the program.
}

```

Q5. Assume the following variable definitions:
```
int a = 5, b = 12;
double x = 3.4, z = 9.1;
```
What are the values of the following expressions?
``` cpp
A) b / a
B) x * a
C) static_cast<double>(b / a)
D) static_cast<double>(b) / a
E) b / static_cast<double>(a)
F) static_cast<double>(b) / static_cast<double>(a) 
G) b / static_cast<int>(x)
H) static_cast<int>(x) * static_cast<int>(z)
I) static_cast<int>(x * z) 
J) static_cast<double>(static_cast<int>(x) * static_cast<int>(z))
```

Q6. Complete the following program skeleton so it asks the user to enter a character. Store the character in the variable `letter`. Use a type cast expression with the
variable in a cout statement to display the character’s ASCII code on the screen.
``` cpp
#include <iostream>
using namespace std;

int main()
{
char letter;
// Finish this program
// as specified above.
return 0;
}
```
Q7. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
int main()
{
  int integer1, integer2;
  double result;
  integer1 = 19;
  integer2 = 2;
  result = integer1 / integer2;
  cout << result << endl;
  result = static_cast<double>(integer1) / integer2;
  cout << result << endl;
  result = static_cast<double>(integer1 / integer2);
  cout << result << endl;
  return 0;
}
```
 
Q8.Write statements using combined assignment operators to perform the following:
```
A) Add 6 to x .
B) Subtract 4 from amount .
C) Multiply y by 4.
D) Divide total by 27.
E) Store in x the remainder of x divided by 7.
F) Add y * 5 to x .
G) Subtract discount times 4 from total .
H) Multiply increase by salesRep times 5.
I) Divide profit by shares minus 1000.
```
Q9. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
int main ()
{
int a = 0, b = 2, x = 4, y = 0;
cout << (a == b) << endl;
cout << (a != y) << endl;
cout << (b <= x) << endl;
cout << (y > a) << endl;
return 0;
}
```
Q10. Write an if statement that performs the following logic: if the variable `x` is equal to 20, then assign 0 to the variable `y`.

Q11. Write an if statement that performs the following logic: if the variable `sales` is greater than 50,000, then assign 0.25 to the `commissionRate` variable, and
assign 250 to the `bonus` variable.

Q12. The following code segment is syntactically correct, but it appears to contain a logic error. Can you find the error?
``` cpp
if (interestRate > .07)
  cout << "This account earns a $10 bonus.\n";
  balance += 10.0;
```

Q13. TRUE or FALSE: The following if/else statements cause the same output to display.

A) 
``` cpp
if (x > y)
  cout << "x is the greater.\n";
else
  cout << "x is not the greater.\n";
```
B) 
``` cpp
if (y <= x)
  cout << "x is not the greater.\n";
else
  cout << "x is the greater.\n";
```
Q14. The following code is used in a bookstore program to determine how many discount coupons a customer gets. Complete the table that appears after the
program.
``` cpp
int numBooks, numCoupons;
cout << "How many books are being purchased? ";
cin >> numBooks;
if (numBooks < 1)
numCoupons = 0;
else if (numBooks < 3)
numCoupons = 1;
else if (numBooks < 5)
numCoupons = 2;
```

