## *Assignment No : 03*

## *Assignment Name : Practice code on Constructors, Friend Functions/classes & Inheritance.*


----------
# *Constructor*
-----------
## *Example 1 :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;

class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:

    // Default Constructor
    Cars(){
        companyName = "Toyota";
    }

    // Parameterized Constructor
    Cars(string modelName, string fuelType, float mileage, double price){
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    // For displayig Data
    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << " Price : " << price << endl << endl;
    }

};

int main(){
    
    // Creating Objects
    Cars car1, car2("Fortuner", "Diesel", 10 , 350000);
    car1.getData();
    car2.getData();
    return 0;
}
```

## *Output :*
<p align="center">

<img width="388" height="235" alt="Image" src="https://github.com/user-attachments/assets/460f4ee3-3682-4998-8149-78ba83b37057" />

</p>

## *Discussion :*
<p >
 Here constructor use. It has two types. Car1 use normal constructor, and car2 use parameter one. Data we see by getdata. It show what inside the variable.
</p>




--------
## *Example 2 :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;

class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:

    // Default Constructor
    Cars(){
        companyName = "Toyota";
    }

    // Parameterized Constructor
    Cars(string modelName, string fuelType, float mileage, double price){
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    // For Setting Data
    void setData(string companyName,string modelName, string fuelType, float mileage, double price){
        this -> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    // For displayig Data
    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << "Price : " << price << endl << endl;
    }

};

int main(){
    
    // Creating Objects
    Cars car1, car2("Fortuner", "Diesel", 10 , 350000);
    car1.setData("TOYOTA", "Atlis", "Diesel", 12, 400000);
    car1.getData();
    car2.getData();
    return 0;
}
```

## *Output :*
<p align="center">

<img width="388" height="235" alt="Image" src="https://github.com/user-attachments/assets/8a31ccdf-0d88-4094-bc7c-e1177638f190" />


</p>

## *Discussion :*
<p >
 In this code we are using constructor. Two constructor is made, one normal and one with values. For car1 the simple constructor run, and for car2 the one with value is use. Then we use getdata to show info. Also setdata is use to put value inside car1 later.
</p>

--------

## *Example 3 :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;

class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:

    // Default Constructor
    Cars(){
        cout << "Default Constructor is invoked!" << endl;
    }

    // Parameterized Constructor
    Cars(string companyName,string modelName, string fuelType, float mileage, double price){
        cout << "Parameterised Constructor is invoked!" << endl;
        this-> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    // Copy Constructor
    Cars(const Cars &obj){
        cout << "Copy Constructor is invoked!" << endl;
        this -> companyName = obj.companyName;
        this -> modelName = obj.modelName;
        this -> fuelType = obj.fuelType;
        this -> mileage = obj.mileage;
        this -> price = obj.price;
    }

    // For Setting Data
    void setData(string companyName,string modelName, string fuelType, float mileage, double price){
        this -> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    // For displayig Data
    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << "Price : " << price << endl << endl;
    }

};

int main(){
   
    // Creating Objects
    Cars car1, car2("Toyota","Fortuner", "Diesel", 10 , 350000);
    car1.setData("TOYOTA", "Atlis", "Diesel", 12, 400000);
    car1.getData();
    car2.getData();
    //Cars car3(car1); // This also works
    Cars car3 = car1;
    car3.getData();
    return 0;
}
```

## *Output :*
<p align="center">

<img width="388" height="422" alt="Image" src="https://github.com/user-attachments/assets/93977d34-f18a-4a66-be12-139836444ccb" />

</p>

## *Discussion :*
<p >
 Constructor is use in this code. Two type of contructor make. Car1 use default one, and car2 take the one with many value. getdata function help to see the output in variable. setdata also use for give value to car1. For car3, it copy from car1 by using copy contructor.
</p>



--------


--------

# *Accessibility in Inheritance*

---------

## *A chart is provided below on Accessibility in Inheritance from different classes -*

## *In public mode :*
| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |    *yes*    |   *yes*  |

-------

## *In protected mode :*

| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |    *yes*    |   *yes*  |

---------

## *In private mode :*

| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |     *no*    |   *no*   |

---------


# *Checking the chart's validity with the help of code :*

--------

## *Example code of Inheritance in public mode :*
## *Code :*
```C
#include<bits/stdc++.h>
using namespace std;

class Base{
    string priv="Private variable of Base";
public:
    string pub="Public variable of Base";
protected:
    string prot="Protected variable of Base";
public:
    void show(){
        cout<<"Base accessing its own variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child1:public Base{
public:
    void show(){
        cout<<"Child1 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child2:public Child1{
public:
    void show(){
        cout<<"Child2 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

int main(){
    Child1 c1;
    c1.show();
    Child2 c2;
    c2.show();
    return 0;
}

```

## *Output :*
<p align="center">



</p>


## *Discussion :*

<p> Base Class's only private variables are not being able to access from Child1 and Child2. Rest of them are accessible from both classes.
    </p>

    
---------




## *Example code of Inheritance in protected mode :*
## *Code :*
```C
#include<bits/stdc++.h>
using namespace std;

class Base{
    string priv="Private variable of Base";
public:
    string pub="Public variable of Base";
protected:
    string prot="Protected variable of Base";
public:
    void show(){
        cout<<"Base accessing its own variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child1:protected Base{
public:
    void show(){
        cout<<"Child1 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child2:protected Child1{
public:
    void show(){
        cout<<"Child2 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

int main(){
    Child1 c1;
    c1.show();
    Child2 c2;
    c2.show();
    return 0;
}

```

## *Output :*
<p align="center">


</p>

## *Discussion :*
<p>
    Base Class's only private variables are not being able to access from Child1 and Child2. Rest of them are accessible from both classes.
    </p>

    

--------

## *Example code of Inheritance in private mode :*
## *Code :*
```C
#include<bits/stdc++.h>
using namespace std;

class Base{
    string priv="Private variable of Base";
public:
    string pub="Public variable of Base";
protected:
    string prot="Protected variable of Base";
public:
    void show(){
        cout<<"Base accessing its own variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child1:private Base{
public:
    void show(){
        cout<<"Child1 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

class Child2:private Child1{
public:
    void show(){
        cout<<"Child2 accessing Base's variables:\n";
        cout<<priv<<endl<<pub<<endl<<prot<<endl<<endl;
    }
};

int main(){
    Child1 c1;
    c1.show();
    Child2 c2;
    c2.show();
    return 0;
}

```

## *Output :*
<p align="center">


</p>

## *Discussion:*
<p>
Child1 can not access private data member and Child2 can not access any data member from Base Class.
</p>


--------

## *Friend Function :*

## *Code :*
```C
#include<bits/stdc++.h>
using namespace std;

double areaCalculator(double,double);

class Rectangle{
    double length,width,area;
public:
    Rectangle(double length,double width){
        this->length=length;
        this->width=width;
    }

    friend double areaCalculator(Rectangle &obj);

    void getArea(){
        cout<<"The area of the Rectangle with length "<<length<<" and width "<<width<<" is : "<<area<<endl<<endl;
    }
};

double areaCalculator(Rectangle &obj){
   
    return obj.area=obj.length*obj.width;
}

int main(){
    Rectangle r1(1,3);
    areaCalculator(r1);
    r1.getArea();
    return 0;
}

```

## *Output :*
<p align="center">

<img width="388" height="47" alt="Image" src="https://github.com/user-attachments/assets/3f1d4e40-5f63-40c5-8587-dc53c926c716" />


</p>

## *Discussion:*
<p>
For find the area of rectangle, I use one friend function name areacalculator(). It give the area and put in area variable. This friend function can see the private variable. We use getdata() to show the area.
</p>


--------


## *Friend Class :*

## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;


class AreaCalculator;

class Rectangle{
    double length;
    double width;
    double area;
public:
    Rectangle(double length, double width){
        this -> length = length;
        this -> width = width; 
    }

    // Friend Declaration
    friend class AreaCalculator;

   void getArea(){

        cout<<"The area of the Rectangle with length "<<length<<" and width "<<width<<" is : "<<area<<endl<<endl;
    }
};

// Friend Class
class AreaCalculator{
public:
    double calculate(Rectangle &obj){
       return obj.area=obj.length*obj.width;
    }
};

int main(){

    Rectangle r(2,3);

    AreaCalculator obj;

    obj.calculate(r);

    r.getArea();

    return 0;
}
```

## *Output :*
<p align="center">

<img width="388" height="47" alt="Image" src="https://github.com/user-attachments/assets/fcc39060-0a8a-4033-9be5-c4e2c35019ed" />
</p>


## *Discussion:*
<p>
For find rectangle area, I use friend class name Areacalculator. this friend help for do area calculate. Object of that class have one function name calculate, it find area of rectangle object and put it in area variable. With getArear() we can see the area.
</p>

--------

