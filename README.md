
# Object Oriented Programming Notes - Last Minute Revision

Here we have last minute revision notes of object oriented programming language. These questions will familiarize you with the most important object-oriented programming concepts and help you ace your job interview.






## Most Asked OOPS Interview Questions

#### 1: What is OBJECT-ORIENTED PROGRAMMING?

**Answer**: Object-oriented programming is a programming paradigm built on the concept of objects.

In Other Words, it is an approach to problem-solving where all computations are carried out using objects.

---

#### 2: Class and Object

**Answer**: 

**Class**: A class is the building block that leads to Object-Oriented programming. It is a user-defined datatype, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class.

**Object**: An Object is an instance of a Class. When a class is defined, no memory is allocated but when it is instantiated (i.e. an object is created) memory is allocated.

```c++
#include <bits/stdc++.h>
using namespace std;
class Person{
	// Access specifier
	public:

	// Data Members
	string name;

	// Member Functions()
	void printname(){
	   cout << "Person name is: " << name;
	}
};

int main() {

	// Declare an object of class Person
	Person obj1;

	// accessing data member
	obj1.name = "Thanos";

	// accessing member function
	obj1.printname();
	return 0;
}

```

---

#### 2: Constructor

**Answer**: 

- Constructors are special class members which are called by the compiler every time an object of that class is instantiated.

- Constructors have the same name as the class and may be defined inside or outside the class definition.

There are 3 types of constructors:

    1. Default constructors
    2. Parameterized constructors
    3. Copy constructors

1. **Default Constructor**: Default constructor is the constructor which doesn’t take any argument. It has no parameters.

2. **Parameterized Constructor**: A constructor is called Parameterized Constructor when it accepts a specific number of parameters.

3. **Copy Constructor**: A copy constructor is a member function which initializes an object using another object of the same class.

**Characteristics of the constructor**:

- Constructor has the same name as the class itself.
- Constructors don’t have a return type.
- A constructor is automatically called when an object is created.
- It must be placed in the public section of class.
- If we do not specify a constructor, C++ compiler generates a default constructor for object (expects no parameters and has an empty body).
- Constructors can be overloaded.
- Constructor cannot be declared virtual.

```C++
#include <bits/stdc++.h>
using namespace std;

class student
{
     string name;
     public:
       int age;
       bool gender;
    
    // Default Constructor
    student(){
      cout<<"Default Constructor"<<endl;
    }
    
    // parameterised constructor
    student(string s, int a, int b)  
    {
       name = s;
       age = a;
       gender = b;
       cout <<"parameterised constructor"<<endl;
    }

    // copy constructor
    student (student &p){              
      name = p.name;
      age = p.age;
      gender = p.gender;
      cout<<"copy constructer"<<endl;
    }

    void printinfo()
    {
        cout << "Name = ";
        cout << name << endl;
        cout << "Age = ";
        cout << age << endl;
        cout << "Gender = ";
        cout << gender << endl;
    }
};

int main()
{
    student w("sumeet", 20, 1);
    student c;
    c = w;
    c.printinfo();
    return 0;
}

```



