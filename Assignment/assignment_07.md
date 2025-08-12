
## **Assignment: 07**
## **Exercise problem of EXCEPTION HANDLING (13.3)**

## **Experiment No: 01**
## **Experiment Name: Basic Exception Handling with int Throw and Catch**
## **Submission Date: August 10, 2025**

## **Code 01:**
```C++
#include <iostream>
using namespace std;

int main()
{
    cout << "Start\n";

    try
    {
        cout << "Inside try block\n";
        throw 10;
        cout << "This will not execute";
    }
    catch (int i)
    {
        cout << "Caught One! Number is: " << i << "\n";
    }

    cout << "End";
    return 0;
}


```

## **Output 01:** 
<p align="center">
<img width="831" height="457" alt="Image" src="https://github.com/user-attachments/assets/b1ff5119-6ba1-4103-80a0-7fa12fc2e536" />
</p>

## **Experiment No: 02**
## **Experiment Name: Exception Handling with Mismatched Catch Type (Does Not Catch)**
## **Submission Date: August 10, 2025**

## **Code 02:**
```C++
#include <iostream>
using namespace std;

int main()
{
    cout << "Start\n";

    try
    {
        cout << "Inside try block\n";
        throw 10;
        cout << "This will not execute";
    }
    catch (double i)
    {
        cout << "Caught One! Number is: " << i << "\n";
    }

    cout << "End";
    return 0;
}


```

## **Output 02:** 
<p align="center">
<img width="852" height="369" alt="Image" src="https://github.com/user-attachments/assets/53681931-ee8c-4bc3-b99d-3401bbae5421" />
</p>

## **Experiment No: 03**
## **Experiment Name: Throwing Exception from a Function Outside the Try Block**
## **Submission Date: August 10, 2025**

## **Code 03:**
```C++
#include <iostream>
using namespace std;

void Xtest(int test)
{
    cout << "Inside Xtest, test is: " << test << "\n";
    if (test)
        throw test;
}

int main()
{
    cout << "start\n";
    try
    {
        Xtest(0);
        Xtest(1);
        Xtest(2);
    }
    catch (int i)
    {
        cout << "Caught One! Number is: " << i << "\n";
    }
    cout << "end";
    return 0;
}


```

## **Output 03:** 
<p align="center">
<img width="846" height="452" alt="Image" src="https://github.com/user-attachments/assets/40d86a18-abf9-4ee4-aef9-90dc9c75a22c" />
</p>

## **Experiment No: 04**
## **Experiment Name: Try-Catch Inside a Function (Local Exception Handling)**
## **Submission Date: August 10, 2025**

## **Code 04:**
```C++
#include <iostream>
using namespace std;

void Xhandler(int test)
{
    try
    {
        if (test)
            throw test;
    }
    catch (int i)
    {
        cout << "Caught One! Ex, #: " << i << '\n';
    }
}

int main()
{
    cout << "start\n";
    Xhandler(1);
    Xhandler(2);
    Xhandler(0);
    Xhandler(3);
    cout << "end";
    return 0;
}


```

## **Output 04:** 
<p align="center">
<img width="839" height="404" alt="Image" src="https://github.com/user-attachments/assets/9466fe19-4dc9-4844-9f39-356c65d5814a" />
</p>

## **Experiment No: 05**
## **Experiment Name: Handling Multiple Exception Types with Multiple Catch Blocks**
## **Submission Date: August 10, 2025**

## **Code 05:**
```C++
#include <iostream>
using namespace std;

void Xhandler(int test)
{
    try
    {
        if (test)
            throw test;
        else
            throw "Value is zero.";
    }
    catch (int i)
    {
        cout << "Caught One! Ex, #: " << i << '\n';
    }
    catch (const char *str)
    {
        cout << "Caught a string: " << str << '\n';
    }
}

int main()
{
    cout << "start\n";
    Xhandler(1);
    Xhandler(2);
    Xhandler(0);
    Xhandler(3);
    cout << "end";
    return 0;
}


```

## **Output 05:** 
<p align="center">
<img width="857" height="503" alt="Image" src="https://github.com/user-attachments/assets/dcd0b8b7-4a04-4701-953f-b0ee2a125fee" />
</p>
