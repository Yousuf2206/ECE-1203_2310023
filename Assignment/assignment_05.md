## **Assignment 05:**

<div align="justify">

</div>

## **Problem 1 : Square a Number Using a Class and Pass-by-Value in C++**

## **Code 1 :**
```C++
#include <iostream>
using namespace std;

class samp
{
    int i;

public:
    samp(int n) { i = n; }
    int get_i() { return i; }
};

int sqr_it(samp o)
{
    return o.get_i() * o.get_i();
}

int main()
{
    samp a(10), b(2);
    cout << sqr_it(a) << "\n";
    cout << sqr_it(b) << "\n";
    return 0;
}

```

## **Output :**
<p align="center">
<img width="847" height="330" alt="Image" src="https://github.com/user-attachments/assets/64e4f83c-99de-4a7f-84ed-5f7762598853" />
    
</p>

## **Discussion:**
In this program, the function sqr_it() is written outside the class samp and is not a friend of the class. So, it can’t directly use the private variable i. But the class has a public function get_i() that gives the value of i. When sqr_it() is called, it gets a copy of the object, not the original one. This means any changes inside the function don’t change the original object. Inside sqr_it(), the function uses get_i() to get the value of i and then returns its square (the number multiplied by itself). Since sqr_it() is not part of the class, it can only use the public functions to get information. This shows how private data is kept safe and only accessed through public functions.

## **Problem 2 : Demonstrating Pass-by-Value Using a Class in C++**

## **Code 2 :**
```C++
#include <iostream>
using namespace std;

class samp
{
    int i;

public:
    samp(int n) { i = n; }
    void set_i(int n) { i = n; }
    int get_i() { return i; }
};

void sqr_it(samp o)
{
    o.set_i(o.get_i() * o.get_i());
    cout << "Copy of a has i value of " << o.get_i() << endl;
}

int main()
{
    samp a(10);
    sqr_it(a);
    cout << "But, a.i is unchanged in main: ";
    cout << a.get_i() << endl;
    return 0;
}



```

## **Output :**
<p align="center">
<img width="832" height="344" alt="Image" src="https://github.com/user-attachments/assets/4dd006cb-4e02-4c80-ba74-c3f7ef95167a" />


</p>

## **Discussion:**
In this program, the function sqr_it() is written outside the class samp and is not a special friend of the class. So, it cannot directly access the private variable i. But the class has public functions get_i() and set_i() that let it read and change i. When we call sqr_it(), it gets a copy of the object, not the original one. This means any changes made inside sqr_it() only affect the copy, not the original object in main(). Inside sqr_it(), it gets the value of i, squares it, and sets this new value inside the copy. It also prints the new value. But when we go back to main(), the original object still has the old value because it wasn’t changed. This program shows how private data is kept safe by using public functions to access it, and how passing a copy to a function means the original object stays the same even if the copy changes.

## **Problem 3 : Modifying Object Data Using Pointers in C++**

## **Code 3 :**
```C++
#include <iostream>
using namespace std;

class samp
{
    int i;

public:
    samp(int n) { i = n; }
    void set_i(int n) { i = n; }
    int get_i() { return i; }
};

void sqr_it(samp *o)
{
    o->set_i(o->get_i() * o->get_i());
    cout << "Copy of a has i value of " << o->get_i() << "\n";
}

int main()
{
    samp a(10);
    sqr_it(&a);
    cout << "Now, a in main() has been changed: ";
    cout << a.get_i();
    return 0;
}



```

## **Output :**
<p align="center">
<img width="840" height="340" alt="Image" src="https://github.com/user-attachments/assets/5ea7225e-5d26-4774-a47e-f2eef0976fd5" />

</p>

## **Discussion:**
In this program, the function sqr_it() is written outside the class samp and is not a friend of the class. So, it cannot directly access the private variable i. But the class has public functions get_i() and set_i() to read and change i. Instead of passing the object itself, this program passes the address of the object to the function using a pointer. This means the function works with the original object, not a copy. Inside sqr_it(), the pointer is used to get the value of i, square it, and then save the new value back to the same object. Because the function changes the actual object, the change is seen when we check the value in main(). This program shows how we keep data safe by using public functions to access private data, and how passing by pointer lets a function change the original object directly.


## **Problem 4 : Creating and Using Objects with Constructor and Destructor in C++**

## **Code 4 :**
```C++
#include <iostream>
using namespace std;

class samp
{
    int i;

public:
    samp(int n)
    {
        i = n;
        cout << "Constructing \n";
    }
    ~samp() { cout << "Destructing \n"; }
    int get_i() { return i; }
};

int sqr_it(samp o)
{
    return o.get_i() * o.get_i();
}

int main()
{
    samp a(10);
    cout << sqr_it(a) << "\n";
    return 0;
}

```

## **Output :**
<p align="center">
<img width="835" height="393" alt="Image" src="https://github.com/user-attachments/assets/68bfd86c-5921-4496-9b4e-41095c36fafe" />

</p>

## **Discussion:**
In this program, the function sqr_it() is written outside the class and is not a friend, so it can’t directly use the private variable i. But the class has a public function get_i() to get the value of i. When we call sqr_it(), it gets a copy of the object, not the original one. So, any changes inside sqr_it() only affect the copy, not the original object. Inside sqr_it(), it gets the value of i and returns its square (the number times itself). The original object stays the same. You also see the constructor message when the object is made, and the destructor message when the copy inside sqr_it() is destroyed. This program shows how private data is kept safe by only letting functions access it, and how passing a copy means the original object doesn’t change.
