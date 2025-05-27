----------
## **Assignment No : 2**

## **Assignment Name : Use of Constractor and Function.**

## **Submission Date : 27 May 2025**

----------

## **Code - 1:**
```C++
//In the name of ALLAH
 
#include<iostream>
using namespace std;

class MyClass {
    public:
    MyClass(){
        cout<< "Hello World !";
    }
};

int main()
{ 
    MyClass myObj;

  return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/98f4dd5a-5e55-4d1f-82cf-5276dba4eec3)

----------

## **Code - 2:**
```C++
//In the name of ALLAH
 
#include<iostream>
using namespace std;

class MyClass {
    private:
        int x;
        int y;
    public:
        MyClass(int p, int q){
            x=p;
            y=q;
        }
    void display(){
        cout<<"Value of x: "<< x << endl;
        cout<<"Value of y: "<< y << endl;
    }
};

int main()
{ 
    MyClass a(4,5);
    a.display();
  return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/a664cd44-ef1a-47cd-b1a7-83360fa4ad33)

----------

## **Code - 3:**
```C++
//In the name of ALLAH
 
#include<iostream>
using namespace std;

class car{
    public:
        string brand;
        string model;
        int year;
    car(string x, string y, int z){
        brand=x;
        model=y;
        year=z;
    }
};

int main()
{ 
    car car1("ABC", "abc", 2005);
    car car2("ACB", "acb", 2008);

    cout<<car1.brand<<" "<<car1.brand<<" "<<car1.year<<endl;
    cout<<car2.brand<<" "<<car2.brand<<" "<<car2.year<<endl;
    
  return 0;
}

```
## **Output :**
![Image](https://github.com/user-attachments/assets/6ad7de57-6e3b-4336-9436-8a341075dd16)

----------

## **Code - 4:**
```C++
#include<bits/stdc++.h>
using namespace std;

class cars {
   private:
        string name;
        string model;
        string fuel_type;
        float milage;
        double price;
    
    public:
        cars(){
            cout<<"default"<<endl;
        }
};

int main(){

    cars c1, c2;


    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/bfd9b3fe-ffe1-4736-bbe0-9e65fb75aa68)

----------

## **Code - 5:**
```C++
#include<bits/stdc++.h>
using namespace std;

class cars {
   private:
        string name;
        string model;
        string fuel_type;
        float milage;
        double price;
    
    public:
        cars(){
            name = "Toyota";
            model = "Altis";
            fuel_type = "Petrol";
            milage = 20;
            price = 2000;
        }
        

        void displayData(){
            cout << "Company name: "<< name << endl;
            cout << "Company name: "<< model << endl;
            cout << "Company name: "<< fuel_type << endl;
            cout << "Company name: "<< milage << endl;
            cout << "Company name: "<< price << endl<<endl;
        }
};

int main(){

    cars c1, c2;

    c1.displayData();
    c2.displayData();


    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/5ab03cb5-7269-41e5-be1c-b7b01bdcf0af)

----------

## **Code - 4:**
```C++
#include<bits/stdc++.h>
using namespace std;

class cars {
   private:
        string name;
        string model;
        string fuel_type;
        float milage;
        double price;
    
    public:
        cars(){
            cout<<"default"<<endl;
        }
};

int main(){

    cars c1, c2;


    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/bfd9b3fe-ffe1-4736-bbe0-9e65fb75aa68)

----------

## **Code - 6:**
```C++
#include <bits/stdc++.h>
using namespace std;

class cars
{
private:
    string name;
    string model;
    string fuel_type;
    float milage;
    double price;

public:
    cars()
    {
        name = "Toyota";
    }
    cars(string cname, string ftype, float m, double p)
    {

        name = cname;
        fuel_type = ftype;
        milage = m;
        price = p;
    }

    void displayData()
    {
        cout << "Company name: " << name << endl;
        cout << "Model name: " << model << endl;
        cout << "Fuel Type: " << fuel_type << endl;
        cout << "Milage: " << milage << endl;
        cout << "Price: " << price << endl
             << endl;
    }
};

int main()
{

    cars c1, c2("Fortuner", "disel", 10, 2000);

    c1.displayData();
    c2.displayData();

    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/a706a4fc-3e85-4350-947f-9f4b92d73634)

----------

## **Code - 7:**
```C++
#include<bits/stdc++.h>
using namespace std;

class cars {
   private:
        string name;
        string model;
        string fuel_type;
        float milage;
        double price;
    
    public:
        cars(){
        }
        void setData(string cname, string mname, string ftype, float m, double p){
            name = cname;
            model = mname;
            fuel_type = ftype;
            milage = m;
            price = p;
        }

        void displayData(){
            cout << "Company name: "<< name << endl;
            cout << "Company name: "<< model << endl;
            cout << "Company name: "<< fuel_type << endl;
            cout << "Company name: "<< milage << endl;
            cout << "Company name: "<< price << endl;
        }
};

int main(){

    cars c1;

    c1.displayData();


    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/90d92380-da18-4a3c-ae40-887d15613b72)

----------

## **Code - 8:**
```C++
#include <iostream>
#include <string> // Include this for using the string class
using namespace std;

class Cars {
private:
    // Data members
    string company_name;
    string model_name;
    string fuel_type;
    float mileage;
    double price;

public:
    // Default constructor
    Cars() {
        cout << "Default constructor called" << endl;
    }

    Cars(string cname, string mname, string ftype, float m, double p) {
        cout << "Parameterized constructor called" << endl;
        company_name = cname;
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    // Copy constructor
    Cars(const Cars &obj) {
        cout << "Copy constructor called" << endl;
        company_name = obj.company_name;
        model_name = obj.model_name;
        fuel_type = obj.fuel_type;
        mileage = obj.mileage;
        price = obj.price;
    }

    void setData(string cname, string mname, string ftype, float m, double p) {
        company_name = cname;
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    void displayData() {
        cout << "Company Name: " << company_name << endl;
        cout << "Model Name: " << model_name << endl;
        cout << "Fuel Type: " << fuel_type << endl;
        cout << "Mileage: " << mileage << endl;
        cout << "Price: " << price << endl << endl;
    }
};

int main() {
    Cars car1, car2("toyota", "fortuner", "diesel", 10, 350000);
    car1.setData("TOYOTA", "altis", "Petrol", 15, 430000);
    car1.displayData();
    car2.displayData();
    Cars car3 = car1; // This line calls the copy constructor
    car3.displayData();
    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/eb050589-9625-4188-9bf1-3818b7a552eb)

----------

## **Code - 9:**
```C++
#include <iostream>
#include <string>
using namespace std;

class Cars {
private:
    // Data members
    string company_name;
    string model_name;
    string fuel_type;
    float mileage;
    double price;
public:
    // Default constructor
    Cars() {
        company_name = "Toyota";
    }
    Cars(string cname, string mname, string ftype, float m, double p) {
        company_name = cname;
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    void setData(string cname, string mname, string ftype, float m, double p) {
        company_name = cname;
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    void displayData() {
        cout << "Company Name: " << company_name << endl;
        cout << "Model Name: " << model_name << endl;
        cout << "Fuel Type: " << fuel_type << endl;
        cout << "Mileage: " << mileage << endl;
        cout << "Price: " << price << endl;
    }
};

int main() {
    Cars car1, car2("toyota", "fortuner", "diesel", 10, 350000);
    car1.setData("TOYOTA", "altis", "Petrol", 15, 430000);
    car1.displayData();
    car2.displayData();
    return 0;
}
```
## **Output :**
![Image](https://github.com/user-attachments/assets/837a0a51-1862-4145-a47d-e10fe9b49d03)
