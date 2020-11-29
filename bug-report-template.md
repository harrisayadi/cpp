# Bug 1

1. **The incorrect original code or code snippit that you wrote:**

``` cpp
for(int i=0;i<size;i++)
    
cout<<"Value Entered: "<<unique_ptr[size]<<endl;

return 0;
}

```

2. **What bug does the original code have?**

  When I ran my code, the arrays displays the number 0.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
 A misunderstanding in placing terms inside the bracket []

4. **How to correct the bug?**
inside the bracket [] should be written i instead of size.

5. **The corresponding bug-free code or code snippet is:**

```
for(int i=0;i<size;i++)
    
cout<<"Value Entered: "<<unique_ptr[i]<<endl;

return 0;
}
```

6. **What is the take-away message from this bug?**
Understanding how to properly run the code.

# Bug 2

1. **The incorrect original code or code snippit that you wrote:**

```cpp
  int sum=0,avg=0;
         for(int i=0;i<5;++i){
            
          if(stock[i]<5000 || stock[i]<0)
            throw "Stock price is invalid!";
            
            sum+=stock[i]; 
         }
         avg=sum/5;
         return avg;

```

2. **What bug does the original code have?**

  When i ran my code it's showing a wrong result.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
A lazy mistake where i mistakenly wrote the wrong expression.

4. **How to correct the bug?**
stock[i]<5000  should be stock[i]>5000 
5. **The corresponding bug-free code or code snippet is:**

```cpp

 int sum=0,avg=0;
         for(int i=0;i<5;++i){
            
          if(stock[i]>5000 || stock[i]<0)
            throw "Stock price is invalid!";
            
            sum+=stock[i]; 
         }
         avg=sum/5;
         return avg;
```

6. **What is the take-away message from this bug?**

Paying attention to the simple details on your code.

# Bug 3

1. **The incorrect original code or code snippit that you wrote:**

```cpp
 throw <<"Stock price is invalid!";
            
            sum+=stock[i]; 
         }
         avg=sum/5;
         return avg;
    }

```

2. **What bug does the original code have?**

  expected primary -expression before <<

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
Misunderstading how to properly use the keyword throw.

4. **How to correct the bug?**

get rid of the <<

5. **The corresponding bug-free code or code snippet is:**

```cpp
throw "Stock price is invalid!";
            
            sum+=stock[i]; 
         }
         avg=sum/5;
         return avg;
    }

```

6. **What is the take-away message from this bug?**
Understanding and learning how to properly use the keywords
