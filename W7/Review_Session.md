https://www.udemy.com/course/beginning-c-plus-plus-programming/learn/lecture/9535596#questions/8327306


Q1. True or False: You must declare all private members of a class before the public members.

Q2. Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. Which of the following
shows the correct use of the scope resolution operator in the member function definition?

A) `RetailItem::void setPrice(double p)`

B) `void RetailItem::setPrice(double p)`

Q3. An object’s private member variables are accessed from outside the object by

A) public member functions

B) any function

C) the dot operator

D) the scope resolution operator

Q4.  Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. If `soap` is an
instance of the RetailItem class, which of the following statements properly uses the soap object to call the setPrice member function?

A) `RetailItem::setPrice(1.49);`

B) `soap::setPrice(1.49);`

C) `soap.setPrice(1.49);`

D) `soap:setPrice(1.49);`

Q5. Complete the following code skeleton to declare a class named `Date` . The class should contain variables and functions to store and retrieve a date in the form
4/2/2014.
``` cpp
class Date
{
private:
public:
}
```

Q6. Briefly describe the purpose of a constructor.

Q7. Briefly describe the purpose of a destructor.

Q8. A member function that is never declared with a return data type, but that may have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

Q9. A member function that is never declared with a return data type and can never have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

Q10. Destructor function names always start with

A) A number

B) Tilde character ( ~ )

C) A data type name

D) None of the above

Q11. A constructor that requires no arguments is called

A) A default constructor

B) An overloaded constructor

C) A null constructor

D) None of the above

Q12. TRUE or FALSE: Constructors are never declared with a return data type.

Q13. TRUE or FALSE: Destructors are never declared with a return type.

Q14. TRUE or FALSE: Destructors may take any number of arguments.

Q15. What will the following program display on the screen?
``` cpp
#include <iostream>
using namespace std;
class Tank
{
private:
  int gallons;
public:
  Tank()
    { gallons = 50; }
  Tank(int gal)
    { gallons = gal; }
   int getGallons()
    { return gallons; }
};
int main()
{
  Tank storage[3] = { 10, 20 };
  for (int index = 0; index < 3; index++)
  cout << storage[index].getGallons() << endl;
  return 0;
}
```


Q16. What will the following program display on the screen?
``` cpp
#include <iostream>
using namespace std;
class Package
{
  private:
    int value;
  public:
    Package()
    { value = 7; cout << value << endl; }
    Package(int v)
    { value = v; cout << value << endl; }
    ~Package()
    { cout << value << endl; }
  };
int main()
{
  Package obj1(4);
  Package obj2();
  Package obj3(2);
  return 0;
}
```
Q17. In your answer for Q16. indicate for each line of output whether the line is displayed by constructor #1, constructor #2, or the destructor.

Q18. Why would a member function be declared private?

Q19. Define an array of three InventoryItem objects.

Q20. Complete the following program so it defines an array of `Yard` objects. The program should use a loop to ask the user for the length and width of each `Yard` .
``` cpp
#include <iostream>
using namespace std;
class Yard
{
private:
int length, width;
public:
Yard()
{ length = 0; width = 0; }
setLength(int len)
{ length = len; }
setWidth(int w)
{ width = w; }
};
int main()
{
// Finish this program
}
 
```

Q21. What is the difference between an instance member variable and a static member variable?

Q22. Static member variables are declared inside the class declaration. Where are static member variables defined?

Q23. Does a static member variable come into existence in memory before, at the same time as, or after any instances of its class?

Q24. What limitation does a static member function have?

Q25. What action is possible with a static member function that isn’t possible with an instance member function?

Q26. If class X declares function f as a friend, does function f become a member of class X ?

Q27. Class Y is a friend of class X , which means the member functions of class Y have access to the private members of class X . Does the friend keyword appear in
class Y ’s declaration or in class X ’s declaration?

Q28. Briefly describe what is meant by memberwise assignment.

Q29. Describe two instances when memberwise assignment occurs.

Q30. Describe a situation in which memberwise assignment should not be used.

Q31. When is a copy constructor called?

Q32. How does the compiler know that a member function is a copy constructor?

Q33. What action is performed by a class’s default copy constructor?
  
  
