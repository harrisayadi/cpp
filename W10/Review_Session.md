# Review Session for Section 16

## Correction and Clarification

Please read the doc that has been uploaded to Moodle. 

## Review Questions

Q1. Explain the difference between overloading a function and redefining a function.

<details>

<summary> Click me to show the answer below!</summary>


There is a distinction between redefining a function and overloading a function. An overloaded function is one with the same name as one or more other functions, but with a different
parameter list. The compiler uses the arguments passed to the function to tell which version to call. Overloading can take place with regular functions that are not members of a
class. Overloading can also take place inside a class when two or more member functions of the same class have the same name. These member functions must have different parameter
lists for the compiler to tell them apart in function calls.

Redefining happens when a derived class has a function with the same name as a base class function. The parameter lists of the two functions can be the same because the derived class
function is always called by objects of the derived class type.

</details>


Q2. Explain the difference between static binding and dynamic binding.

<details>

<summary> Click me to show the answer below!</summary>

Binding means the process of matching the function call with the correct function. 

The key difference is that 
- static binding is done during compiling time. 
- dynamical binding is done at runtime. 
</details>


Q3.  Are virtual functions statically bound or dynamically bound?

<details>

<summary> Click me to show the answer below!</summary>

Dynamically Bound

</details>



Q4. What will the following program display?
``` cpp
#include <iostream.>
using namespace std;
class First
{
  protected:
    int a;
  public:
    First(int x = 1)
    { a = x; }
    int getVal()
    { return a; }
 };
 
class Second : public First
{
  private:
    int b;
  public:
    Second(int y = 5)
    { b = y; }
    int getVal()
    { return b; }
};

int main()
{
First object1;
Second object2;
cout << object1.getVal() << endl;
cout << object2.getVal() << endl;
return 0;
}
```

<details>

<summary> Click me to show the answer below!</summary>

``` cpp

1
5
```

</details>


Q5. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
class First
{
protected:
  int a;
public:
  First(int x = 1)
  { a = x; }
  void twist()
  { a *= 2; }
  int getVal()
  { twist(); return a; }
};


class Second : public First
{
private:
  int b;
public:
  Second(int y = 5)
  { b = y; }
  void twist()
  { b *= 10; }
};

int main()
{
First object1;
Second object2;
cout << object1.getVal() << endl;
cout << object2.getVal() << endl;
return 0;
}
```

<details>

<summary> Click me to show the answer below!</summary>

``` cpp

2
2
```

</details>

Q6. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
class First
{
protected:
  int a;
public:
  First(int x = 1)
  { a = x; }
  virtual void twist()
  { a *= 2; }
  int getVal()
  { twist(); return a; }
};

class Second : public First
{
private:
  int b;
public:
  Second(int y = 5)
  { b = y; }
  virtual void twist()
  { b *= 10; }
};

int main()
{
First object1;
Second object2;
cout << object1.getVal() << endl;
cout << object2.getVal() << endl;
return 0;
}
```


<details>

<summary> Click me to show the answer below!</summary>

``` cpp

2
1
```

Some Explanation：The reason why 1 is output from `object2.getVal()` is due to the overriden `twist` function in object2. `object2.getVal()` will activate the 

```
  virtual void twist()
  { b *= 10; }
```
, and there is no effect on variable `a`, which means that `a` remains to be 1. 
</details>

Q7. What will the following program display?
``` cpp
#include <iostream>
using namespace std;
class Base
{
protected:
  int baseVar;
public:
  Base(int val = 2)
  { baseVar = val; }
  int getVar()
  { return baseVar; }
};

class Derived : public Base
{
private:
  int derivedVar;
public:
  Derived(int val = 100)
  { derivedVar = val; }
  int getVar()
  { return derivedVar; }
};

int main()
{
Base *optr = nullptr;
Derived object;
optr = &object;
cout << optr->getVar() << endl;
return 0;
}
```

<details>

<summary> Click me to show the answer below!</summary>

``` cpp

2
```

Some Explanation：This is a tricky question. Something we need to pay attention to here:

- `getVar()` member function in the Base class is not a virtual function. In this case, dynamically bounding cannot be conducted. 
- optr is of type `Base`

So the `getVar()` of the Base class will be called, giving us 2 instead of 100. If you add `virtual` keyword to the `getVar()` function in the Base class, you will get 100 instead. 

</details>

# Assignment 

Q8. Design a `Student`class that has the following members:
- A member variable for the name of the student (a string)
- A member variable for the year that the student was enrolled (a string)
- A constructor and appropriate accessors and mutators
- A virtual print function that displays the student's name and the year he/she was enrolled.

Design a `KpuStudent` class that is derived from the `Student` class. The `KpuStudent` class should have the following members:
- A member variable for the campus location (a string, could be "Surrey", "Richmond" or "Langley")
- A constructor and appropriate accessors and mutators
- A print function that overrides the print function in the base class. The `KpuStudent` class’s print function should display only the student's name and his/her campus location.

Design a `HogwartsStudent` class that is derived from the `Student` class. The `HogwartsStudent` class should have the following members:
- A member variable for the house affiliation of the student (a string, could be "Hufflepuff", "Ravenclaw", "Gryffindor" or "Slytherin").
- A constructor and appropriate accessors and mutators.
- A print function that overrides the print function in the base class. The `HogwartsStudent` class’s print function should display only the student’s name and the student's house affiliation. 

Demonstrate the classes in a program that has an array of `Student` pointers. The array elements should be initialized with the addresses of dynamically allocated `Student` ,
`KpuStudent` , and `HogwartsStudent` objects. (See Program 15-14 on Page with Page No. 937  of the uploading reading task , lines 17 through 22, for an
example of how to do this.) The program should then step through the array, calling each object’s print function.



