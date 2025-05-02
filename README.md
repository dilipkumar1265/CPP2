# CPP MODULE 2 :
# 2a :
# PROGRAM STATEMENT :
Write A CPP Program to allocate memory dynamically for an float variable. (Note: p_var = new 
typename;)
# ALGORITHM :
1. Declare a pointer of the required type (e.g., float* for an integer).
2. Use the new operator to dynamically allocate memory for the float variable.
3. Store the address of the allocated memory in the pointer variable.
4. Assign a value to the dynamically allocated memory through the pointer.
5. Deallocate the memory using the delete operator after usage.
# PROGRAM :
NAME : DILIP KUMAR R
REG NO : 212222040037
```
#include <iostream>
using namespace std; 
class var_space
{
 public:
 float *p_var; 
 
 void allocateSpace()
 {
 p_var = new float;
 cin>>*p_var;
 cout<<"Float Value is : "<<*p_var;
 
 delete p_var;
 }
};
int main()
{
 var_space obj;
 obj.allocateSpace(); 
}
```
# OUTPUT :
![image](https://github.com/user-attachments/assets/1c24879b-8bf3-47a3-9a93-d95b03033490)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 2b :
# PROGRAM STATEMENT :
Write A CPP Program to create class RectangleBox and calculate the volume of the rectangleBoxe 
use of static member variable in the class RectangleBox.
# ALGORITHM :
1. Define a class RectangleBox with a static member variable length, breadth, and height (since all 
sides are equal).
2. Declare a public static member function to calculate the volume (volume = l * b * h).
3. Define the static member function outside the class using the scope resolution operator.
4. In the main function, set the values of length, breadth, and height using the class and calculate the 
volume.
5. Display the calculated volume and end the program.
# PROGRAM :
```
#include <iostream>
using namespace std;
class RectangleBox
{
private:
 static int count;
 int l,b,h;
public:
 RectangleBox(int x,int y,int z) 
 {
 count++; 
 cout << "Constructor called." << endl;
 l=x;
 b=y;
 h=z;
 }
 void calculateVolume() 
 {
 cout << "Volume :" <<l * b *h << endl;
 }
 static int getCount() 
 {
 return count;
 }
};
int RectangleBox::count = 0;
int main()
{
 int l, b, h;
 
 cin >> l >> b >> h;
 RectangleBox obj1(l,b,h);
 obj1.calculateVolume();
 cin >> l >> b >> h;
 RectangleBox obj2(l,b,h);
 obj2.calculateVolume();
 cout << "Total objects: " << RectangleBox::getCount() << endl;
 return 0;
}
```
# OUTPUT :
![image](https://github.com/user-attachments/assets/fff32fb6-a9f1-4e25-84e1-9b8d27893a53)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 2c :
# PROGRAM STATEMENT :
Write a CPP program to overload a function to print Integer data in one and Floating-Point data in 
another
# ALGORITHM :
1. Read three integer marks mk1, mk2, and mk3 from the user.
2. Use the compute() function to calculate the sum of the marks and store it in tot.
3. Print the total marks.
4. Call the compute() function to calculate the average by dividing the total by 3.
5. Display the percentage to the user.
# PROGRAM :
```
#include <iostream>
using namespace std;
int compute(int m1, int m2, int m3)
{
 int total = m1+m2+m3;
 return total;
}
float compute(float avg)
{
 avg = avg/3;
 return avg;
}
int main()
{
 int mk1, mk2,mk3;
 cin>>mk1>>mk2>>mk3;
 
 float tot = compute(mk1, mk2, mk3);
 cout<<"Total="<<tot<<endl;
 
 float perc= compute(tot);
 cout<<"Percentage="<<perc;
}
```
# OUTPUT :
 ![image](https://github.com/user-attachments/assets/3888f46e-a809-4938-a44b-6963da8b2950)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 2d :
# PROGRAM STATEMENT :
Write a CPP Program to negate the existing value using operator overloading.
# ALGORITHM :
1. Define a class with a private member variable to store a number.
2. Overload the - operator by defining a member function that changes the sign of the number.
3. Define the operator function outside the class using the scope resolution operator.
4. In the main function, create an object, assign a positive value, and apply the overloaded - operator to 
turn it negative.
5. Display the result and end the program.
# PROGRAM :
```
#include <iostream>
using namespace std;
class op_over
{
 public:
 
 int data;
 void operator -- ()
 {
 this->data = -(this->data);
 cout<<data;
 }
};
int main()
{
 op_over op;
 
 cin>>op.data;
 --op;
}
```
# OUTPUT :
![image](https://github.com/user-attachments/assets/bf5d229b-045c-4038-a4a5-d170cc427fb7)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.
