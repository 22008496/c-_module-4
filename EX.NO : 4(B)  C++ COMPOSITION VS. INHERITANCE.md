
# EX.NO : 4(B)  C++ COMPOSITION VS. INHERITANCE 

# PROGRAM STATEMENT :  
To write a CPP program to demonstrate on the object composition (use string data).  

# ALGORITHM:    
1. Start the program.  
2. Define a class A that has a string variable and a constructor to initialize it, along with a method to display its value.  
3. Define a class B that contains an object of class A and uses an initializer list to initialize it through B's constructor. Include a display method to show the value of A's object.  
4. In the main function, read a string input, create an object of class B with this input, and call the displa’y method.  
5. End the program.

# PROGRAM: 
```
#include <iostream>
using namespace std;
class A {
    string data;
public:
    A(string a){
        data=a;
        cout<<"Constructor A(string a) is invoked"<<endl;
        
    }
    string getdata(){
        return data;
    }
};
class B {
    A objA;
    string value;
    public:
    B(string val) : objA(val){
        value=val;
    }
    void display(){
        cout<<"Data in object of class B = "<<value<<endl;
        cout<<"Data in member object of class A in class B = "<<objA.getdata()<<endl;
    }
};
int main()
{
    string x;
    cin>>x;
    B obj(x);
    obj.display();
	
	return 0;
}
```
# output:

![Screenshot 2025-05-27 110612](https://github.com/user-attachments/assets/d60a7a9e-6b9a-49c6-b432-bb8021d48f95)

# Result: 
Thus, the C++ program to demonstrate on the object composition is created successfully. 
