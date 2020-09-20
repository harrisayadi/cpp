
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


<!---
- Summary of the process of translating a C++ source file into an executable file 
![alt text](./img/theprocess.PNG "Logo Title Text 1")

-->

## Review Questions
