# EX.NO : 4(A)  C++ CLASS OBJECT CONVERSION 
# PROGRAM STATEMENT :  
To write a CPP Program for Class conversion that can be achieved by conversion function which is  
done by the use of operator overloading 

# ALGORITHM:    
1. Start the program.  
2. Define a class Class_type_one with a private integer variable a to store a integer value. Provide a default constructor to initialize a to 0.0, a parameterized constructor to initialize a with a  specific integer value, a get method to return a, and a display method to print a.  
3. Define another class Class_type_two with a private integer variable b to store the converted  value. Overload the assignment operator (=) to convert an object of Class_type_one to  Class_type_two by assigning a's value to b. Include a display method to print b.  
4. In the main function, read a float input from the user and create an object obj1 of  Class_type_one initialized with this input.  
5. Create an object obj2 of Class_type_two, and use the overloaded assignment operator to assign  obj1 to obj2.  
6. Call the display method for both obj1 and obj2 to display the values stored in Class_type_one  and Class_type_two, respectively.  
7. End the program.

# Program:
```
#include <bits/stdc++.h>
using namespace std;
class Class_type_two;

class Class_type_one {
    int a;

public:
    Class_type_one() {}

    Class_type_one(int x) {
        a = x;
    }
    operator Class_type_two();

    void display() {
        cout << a << endl;
    }

    int getData() {
        return a;
    }
};

class Class_type_two {
    int b;

public:
    Class_type_two() {}

    void setData(int x) {
        b = x;
    }

    void display() {
        cout << b << endl;
    }
    friend class Class_type_one;
};

Class_type_one::operator Class_type_two() {
    Class_type_two obj;
    obj.b = this->a;  
    return obj;
}

int main() {
    int value;
    cin >> value;

    Class_type_one obj1(value);     
    Class_type_two obj2;            

    obj2 = obj1;  

    obj1.display();
    obj2.display();

    return 0;
}
```
# output:

![Screenshot 2025-05-27 105957](https://github.com/user-attachments/assets/1db22d6a-b3b1-4545-b13a-fd98c4969375)

# Result: 
Thus, the C++ program for Class conversion that can be achieved by conversion function, which is done by the use of operator overloading, is created successfully.
