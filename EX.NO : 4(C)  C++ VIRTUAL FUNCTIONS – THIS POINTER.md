
# EX.NO : 4(C)  C++ VIRTUAL FUNCTIONS – THIS POINTER 
# PROGRAM STATEMENT :  
Write a CPP program to demonstrate the concept of virtual functions in Multi-Level Inheritance. 
# ALGORITHM:    
1. Start the program.  
2. Define a base class with a virtual print method that outputs "Base class".  
3. Define a derived class that inherits from base and overrides the print method to read and  display a string.  
4. In the main function, create a pointer of type base and an object of type derived.  
5. Assign the address of the derived object to the base pointer and call the print method using the  pointer.  
6. End the program.
  
# Program: 
```
#include <iostream>
using namespace std;

// Base class
class PC {
public:
    // Virtual function to enable runtime polymorphism
    virtual void get_ram_space() {
        cout << "PC RAM Space" << endl;
    }
};

// Derived class from PC
class PC_XT : public PC {
public:
    void get_ram_space() override {
        cout << "PC_XT has 512 GB RAM Space" << endl;
    }
};

// Derived class from PC_XT (Multi-Level Inheritance)
class PC_AT : public PC_XT {
public:
    void get_ram_space() override {
        cout << "PC_AT has 1 TB RAM Space" << endl;
    }
};

int main() {
    int test;
    cin >> test;

    PC* pcPtr;        // Base class pointer
    PC_AT objAT;      // Most derived class object

    pcPtr = &objAT;   // Assign base class pointer to derived class object

    // Call function using base class pointer
    pcPtr->get_ram_space();  // Demonstrates runtime polymorphism

    return 0;
}
```
# output:

![Screenshot 2025-05-27 111723](https://github.com/user-attachments/assets/d034feed-9d22-47ff-a666-c81e133b6b67)

# Result: 
Thus, the CPP program to demonstrate the concept of virtual functions in Multi-Level Inheritance is executed successfully.
