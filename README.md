# Inheritance
 ### What is inheritance?
 <details>
 
  <summary>Answer</summary>
  Inheritance is a mechanism in which one class acquires the property of another class.
  
</details>

### Why Inheritance?
<details>
 <summary>Answer</summary>
 <br>1.Reduce Duplicate Code</br>
 <br>2.Code Reuse</br>
 <br>3.Better Organization of Code</br>
</details>

### Inheritance Example
# WAP in which cuboid class inherit rectangle class and calculate area and volume.
<details>
 <summary>Code</summary>
 
 
 ```
 #include<iostream>
 using namespace std;
 class rectangle
 {
 public:
 int length;
 int breadth;
 
 void show()
 {
 cout<<length;
 cout<<breadth;
 }
 };
 
 void main()
 {
 rectangle r;
 r.length=10;
 r.breadth=20;
 r.show();
 };
 
 class cuboid:public rectangle
 {
 public:
 int height;
 void display()
 {
 cout<<height;
 }
 };
 
 void main(){
 cuboid c;
 c.length=10;
 c.breadth=20;
 c.height=30;
 c.show();
 c.display();
 }
 
 ```
 </details>


  
