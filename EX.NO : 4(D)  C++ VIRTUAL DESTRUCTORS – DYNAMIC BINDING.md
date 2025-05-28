
# EX.NO : 4(D)  C++ VIRTUAL DESTRUCTORS – DYNAMIC BINDING 

# PROGRAM STATEMENT :  
Write a CPP program to show how the override works using virtual functions and how it works without 
the virtual concept. 

# ALGORITHM:    
1. Start the program.  
2. Define a base class with a virtual print method that outputs "Base class".  
3. Define a derived class that inherits from base and overrides the print method to read and  display a string.  
4. In the main function, create a pointer of type base and an object of type derived.  
5. Assign the address of the derived object to the base pointer and call the print method using the  pointer.  
6. End the program.
 
# PROGRAM:  
```
#include <iostream> 
using namespace std; 
class Base { 
public: 
virtual void show(string input) {  
cout << input << " Base Class Not overridden" << endl; 
} 
virtual ~Base() {}   
}; 
class Derived : public Base { 
public: 
void show(string input) override {  
cout << input << " Derived Class Overridding" << endl;   
} 
}; 
int main() { 
string input; 
cin >> input;  
Base* basePtr = new Derived(); 
basePtr->show(input);   
((Base*)basePtr)->Base::show(input);   
delete basePtr;  
return 0; 
}
```
# output:

![Screenshot 2025-05-27 111013](https://github.com/user-attachments/assets/c34ebf5d-d93a-4672-bd4c-83f322f1d39e)

# Result: 
Thus, the C++ program to show how the override works using virtual functions and how it works  without the virtual concept is created successfully.
