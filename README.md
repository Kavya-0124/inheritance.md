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

### WAP in which cuboid class inherit rectangle class and calculate area and volume.
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
 
 ### Constructors and Inheritance
 <details>
  If we don't speify a constructor, then derived class will use appropriate constructor from baseclass.(Applicable only to Default Constructor)
  <summary>Code</summary>
  
  
  ```
  #include<iostream>
  using namespace std;
  
  class base
  {
  public:
  base()
  {
  cout<<"Default of Base Class";
  }
  base(int b){
  cout<<"Parametrized of Base Class";<<b
  }
  };
  
  class derived:public base{
  //Empty
  };
   void main(){
  derived d1;
  derived d2(9);
  }
  
  ```
  NOTE:
  1st Default Constructor of Base class, then Default Constructor of derived class is called.
  <br>
  2nd Parametrized Constructor of base class is not called when Para. Constructor is present in derived class.
  </br>
  
  ```
  
  #include<iostream>
  using namespace std;
  
  class base
  {
  public:
  base()
  {
  cout<<"Default of Base Class";
  }
  base(int b){
  cout<<"Parametrized of Base Class";<<b
  }
  };
  
  class derived:public base{
  public:
  derived()
  {
  cout<<"Default of Derived Class";
  }
  derived(int d)
  cout<<"Parametrized of Derived Class"<<d;
  };
   void main(){
  derived d1;
  derived d2(9);
  }
  
  ```
  
  ```
  #include<iostream>
  using namespace std;
  
  class base
  {
  public:
  base()
  {
  cout<<"Default of Base Class";
  }
  base(int b_arg){
  cout<<"Parametrized of Base Class";<<b
  }
  };
  
  class derived:public base{
  public:
  derived():base(){
  cout<<"Default of derived class";
  }
  derived(int d_arg):base(d_arg)
  {
  cout<<"Para of derived Class";
  }
  };
   void main(){
  derived d1;
  derived d2(9);
  }
  
  ```
  </details>
  
  ### Overriding Member Function
  <details>
   <summary>Answer</summary>
   
   NOTE: Redefining functionality of BASE class into DERIVED class, then if we create OBJECT of   
   DERIVED class. 
   
   ```
   #include<iostream>
   using namespace std;
   
   class base
   {
   public:
   void Msg()
   {
   cout<<"Base Class";
   }
   };
   
   class derived:public base
   {
   public:
   void Msg()
   {
   cout<<"Derived Class";
   }
   };
   
   void main()
   {
   base b;
   b.Msg(): //Base class
   
   derived c;
   c.Msg; //Derived class
   }
   
   ```
   
   NOTE:DERIVED class object would call, function in derived class, if same function exists in both 
   classes.
   
   ```
   
   #include<iostream>
   using namespace std;
   
   class base
   {
   public:
   void Msg()
   {
   cout<<"Base Class";
   }
   };
   
   class derived:public base
   {
   public:
   void Msg()
   {
   cout<<"Derived class";
   }
   };
   
   void main()
   {
   derived c;
   c.Msg():
   }
   
   class base
   {
   public:
   void Msg()
   {
   cout<<"Base Class";
   }
   };
   
   class derived:public base
   {
   public:
   void Msg(){
   cout<<"Derived Class";
   base::Msg();//calling
   }
   };
   
   void main()
   {
   derived c;
   c.Msg();
   }
   
   ```
   
   </details>
   
   ###isA Relationship
   
   <details>
    <summary>Answer</summary>
    
    
    
   
  
  
  
  
  
  


  
