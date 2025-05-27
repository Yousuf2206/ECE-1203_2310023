----------
## **Assignment No : 1**

## **Assignment Name : Inheritance**

## **Submission Date : 26 May 2025**

----------

## **Code :**
```C++
#include<iostream>
using namespace std;

class A {
private:
    int a_private;
public:
    int a_public;
protected:
    int a_protected;

public:
    A() {
        a_private = 10;
        a_public = 20;
        a_protected = 30;
    }

    void display() {
        cout << "A private: " << a_private << endl;
        cout << "A public: " << a_public << endl;
        cout << "A protected: " << a_protected << endl;
    }
};

class B : public A {
private:
    int b_private;
public:
    int b_public;
protected:
    int b_protected;

public:
    B() {
        b_private = 40;
        b_public = 50;
        b_protected = 60;
    }

    void display() {
        cout << "B private: " << b_private << endl;
        cout << "B public: " << b_public << endl;
        cout << "B protected: " << b_protected << endl;
    }
};

class C : public B {
private:
    int c_private;
public:
    int c_public;
protected:
    int c_protected;

public:
    C() {
        c_private = 70;
        c_public = 80;
        c_protected = 90;
    }

    void display() {
        cout << "C private: " << c_private << endl;
        cout << "C public: " << c_public << endl;
        cout << "C protected: " << c_protected << endl;
    }
};

int main() {
    C c_obj;
    cout << "\nAccessing C's object" << endl;
    cout << "C public: " << c_obj.c_public << endl;

    B b_obj;
    cout << "\nAccessing B's object" << endl;
    cout << "B public: " << b_obj.b_public << endl;

    A a_obj;
    cout << "\nAccessing A's object" << endl;
    cout << "A public: " << a_obj.a_public << endl;

    return 0;
}

```
## **Output :**
![Image](https://github.com/user-attachments/assets/f23fce5d-9f38-4f4c-ae59-0693ac231a2f)
