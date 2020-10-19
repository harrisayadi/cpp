https://www.udemy.com/course/beginning-c-plus-plus-programming/learn/lecture/9535596#questions/8327306


Q1. True or False: You must declare all private members of a class before the public members.

<details>

<summary> Click me to show the answer below!</summary>

False. There is no rule requiring you to declare private members before public members. For example, the `Rectangle` class could be declared as follows:
``` cpp
class Rectangle
{
public:
  void setWidth(double);
  void setLength(double);
  double getWidth() const;
  double getLength() const;
  double getArea() const;
private:
  double width;
  double length;
};
```
In addition, it is not required that all members of the same access specification be declared in the same place. Here is yet another declaration of the `Rectangle` class.
``` cpp
class Rectangle
{
private:
  double width;
public:
  void setWidth(double);
  void setLength(double);
  double getWidth() const;
  double getLength() const;
  double getArea() const;
private:
  double length;
};
```
</details>

Q2. Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. Which of the following
shows the correct use of the scope resolution operator in the member function definition?

A) `RetailItem::void setPrice(double p)`

B) `void RetailItem::setPrice(double p)`

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q3. An object’s private member variables are accessed from outside the object by

A) public member functions

B) any function

C) the dot operator

D) the scope resolution operator

<details>

<summary> Click me to show the answer below!</summary>

A) public member functions

</details>


Q4.  Assume that `RetailItem` is the name of a class, and the class has a void member function named `setPrice` , which accepts a `double` argument. If `soap` is an
instance of the `RetailItem` class, which of the following statements properly uses the `soap` object to call the `setPrice` member function?

A) `RetailItem::setPrice(1.49);`

B) `soap::setPrice(1.49);`

C) `soap.setPrice(1.49);`

D) `soap:setPrice(1.49);`

<details>

<summary> Click me to show the answer below!</summary>

C) `soap.setPrice(1.49);`

</details>


Q6. Briefly describe the purpose of a constructor.

<details>

<summary> Click me to show the answer below!</summary>


A constructor is a member function that has the same name as the class. It is automatically called when the object is created in memory, or instantiated. It is helpful to think of constructors as initialization routines. They

</details>


Q7. Briefly describe the purpose of a destructor.

<details>

<summary> Click me to show the answer below!</summary>

Destructors are member functions with the same name as the class, preceded by a tilde character (~). For example, the destructor for the `Rectangle` class would be named `~Rectangle`. Destructors are automatically called when an object is destroyed. In the same way that constructors set things up when an object is created, destructors perform shutdown procedures when the object goes out of existence. For example, a common use of destructors is to free memory that was dynamically allocated by the class object.

In addition to the fact that destructors are automatically called when an object is destroyed, the following points should be mentioned:
- Like constructors, destructors have no return type.
- Destructors cannot accept arguments, so they never have a parameter list.

</details>


Q8. A member function that is never declared with a return data type, but that may have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

<details>

<summary> Click me to show the answer below!</summary>

A)

</details>

Q9. A member function that is never declared with a return data type and can never have arguments is

A) The constructor

B) The destructor

C) Both the constructor and the destructor

D) Neither the constructor nor the destructor

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q10. Destructor function names always start with

A) A number

B) Tilde character ( ~ )

C) A data type name

D) None of the above

<details>

<summary> Click me to show the answer below!</summary>

B)

</details>


Q11. A constructor that requires no arguments is called

A) A default constructor

B) An overloaded constructor

C) A null constructor

D) None of the above


<details>

<summary> Click me to show the answer below!</summary>

A)

When a constructor doesn’t accept arguments, it is known as the `default constructor`. If a constructor has default arguments for all its parameters, it can
be called with no explicit arguments. It then becomes the default constructor. For example, suppose the constructor for the Sale class had been written as the following:
``` cpp
Sale(double cost = 0.0, double rate = 0.05)
{ itemCost = cost;
  taxRate = rate; }
```
This constructor has default arguments for each of its parameters. As a result, the constructor can be called with no arguments, as shown here:
```Sale itemSale;```
This statement defines a `Sale` object. No arguments were passed to the constructor, so the default arguments for both parameters are used. Because this constructor can be called with no arguments, it is the default constructor.

**When all of a class’s constructors require arguments, then the class does not have a default constructor. In such a case you must pass the required arguments to the constructor when creating an object. Otherwise, a compiler error will result.**


</details>



Q12. TRUE or FALSE: Constructors are never declared with a return data type.

<details>

<summary> Click me to show the answer below!</summary>

True

</details>

Q13. TRUE or FALSE: Destructors are never declared with a return type.

<details>

<summary> Click me to show the answer below!</summary>

True

</details>


Q14. TRUE or FALSE: Destructors may take any number of arguments.

<details>

<summary> Click me to show the answer below!</summary>

False

</details>


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
  
  
