**1).Examination**

    #include <iostream>

    using namespace std;

    class A{ 
    public:
      int x;
    };

    class B:public A{ 
    public:
    B()
    {
        cin >> x;
    }
    };
    class C{
    public:
      int y;
      C(){
        cin >> y;
    }
    };
    class D:public B,public C
    {
      public:
        void sum()
        {
          int sum;
          sum=x+y;
           cout << "Sum= " << sum << endl;
        }
    };

    int main() {
       D obj;
       obj.sum();
       return 0;
     }
**2).Payroll**

    #include <iostream>
    using namespace std;
    class SingleInheritance{
    public:
        string name, gender;
        int salary, age;
        void getDetails(){
        cin >> name >> gender >> age >> salary;
        }
        };

        class inheritedclass:public SingleInheritance{
        public:
        void display(){
            cout << "Name=" << name << "\nGender=" << gender << "\nAge=" << age << "\nSalary=" << salary << endl;
        }
      };

    int main() {
    inheritedclass tc;
      tc.getDetails();
      tc.display();
    return 0;
    }
**3).Counselling**

    #include <iostream>

    using namespace std;

    class Student{
       public:
      virtual void getDetails()=0;
      virtual void displayDetails()=0;
      };

      class StudentDetails:public Student{
      string fname, mname;
      float num;
      public:
     void getDetails(){
         cin >> fname >> mname >> num;
      }
      void displayDetails(){
          cout << fname << endl << mname << endl << num << endl;
      }
    };

    int main() {
      StudentDetails sd;
      sd.getDetails();
      sd.displayDetails();
 
      return 0;
    }
**4).Rectangle**

    #include <iostream>
    using namespace std;
    class Area
    {
      public:
      int getArea(int length, int berth)
      {
        return length*berth;
      }
      };
      class Perimeter
      {
      public:
      int getPerimeter(int length, int berth)
      {
      return length+length+berth+berth;
      }
      };
      class Rectangle:public Area,public Perimeter
      {

      };
      int main() {
      Rectangle rt;
      int l,b;
        cin>>l>>b;
        cout<<rt.getArea(l,b)<<endl;
        cout<<rt.getPerimeter(l,b)<<endl;
      return 0;
      }
**5).Student and Sports**

    #include <iostream>

    using namespace std;
    class student
    {
        public:
        int roll_no,mark_1,mark_2;
        void get()
        {
          cin>>roll_no;
          cin>>mark_1;
          cin>>mark_2;
        }
      };
      class sports
      {public:
      int sport_mark;
      void getsm()
      {
          cin>>sport_mark;
      }
      };
      class statement:public student,public sports
      {
      public:
      int total,average;
      void display()
      {
        total=mark_1+mark_2+sport_mark;
        average=(mark_1+mark_2+sport_mark)/3;
        cout<<roll_no<<endl;
        cout<<total<<endl;
        cout<<average;
        }
        };
        int main()
        {
            statement obj;
            obj.get();
            obj.getsm();
            obj.display();
            return 0;
        }
**6).Single Level Inheritance - Rectangle**

    #include <iostream>

    using namespace std;
    class A
    {
        public:
        int a;
        void getxval()
        {
          cin>>a;
        }
    };
    class B
    {
        public:
        int b;
        void getyval()
        {cin>>b;
        }
        };
        class C:public A,public B
        {
      int c;
      public:
      void sum()
      {
        c=a+b;
        cout<<"Sum = "<<c;
      }
      void mul()
      {
        c=a*b;
        cout<<"\nProduct="<<c;
      }
      };
      int main()
      {
         C obj;
        obj.getxval();
        obj.getyval();
        obj.sum();
        obj.mul();
        return 0;
      }
**7).Payslip Generation**

    #include<iostream>

    using namespace std;
    class c1
    {
      public:
      int length, breadth;
      c1()
      {
        cin>>length>>breadth;
      }

      };
      class c2:public c1
      {
      public:
        void area(int length,int breadth)
        {
          cout<<2*(length+breadth);
        }
        };
        int main() {
        c2 one;
          one.area(one.length,one.breadth);

        return 0;
        }
**8).Square and cube**

    #include <iostream>

    using namespace std;
    class Number
    {
      public:
      int n;
      void getNumber()
      {
          cin>>n;
      }
      void getSquare()
      {
          cout<<n*n<<endl;
      }
      void getCube()
      {
          cout<<n*n*n<<endl;
      }
      };
      class Square:public Number
      {
          public:
          Square()
          {
            getNumber();
            getSquare();
          }
      };
      class Cube:public Number
    {
      public:
      Cube()
      {
        getNumber();
         getCube();
       }
    };
    int main()
    {
      Square objS;
      Cube objC;
      return 0;
    }
 **9).Cost of Pen**
 
    #include <iostream>
    using namespace std;

    class A{protected:int a;
    public:void display(){cin>>a;}
    };
    class B{protected:int b;
    public:void display(){cin>>b;}
    };
    class C:public A,public B{public:
    void display(){}
    void show(){cout<display();
    B *bb;
    bb=&sample;
    bb->display();
    sample.display();
    sample.show();
    return 0;}
**10).Programmer Information**

      #include <iostream>
      using namespace std;
      class person
      {
        public:
          int age;
          char name[20];
          char gender[10];
 
          void getdata()
          {
              cin>>name;
               cin>>age;
              cin>>gender;
          }
          void display()
          {
              cout<<"Name: "<<name<<endl;
              cout<<"Age: "<<age<<endl;
              cout<<"Gender: "<<gender<<endl;
          }
          };
        class employee:public person
        {
        public:
          char n[10];
          int salary;

          void getdata()
          {
            cin>>n;
            cin>>salary;
          }

        void display()
        {
          cout<<"Name of Company: "<<n<<endl;
          cout<<"Salary: Rs."<<salary<<endl;
        }
        };

        class programmer:public employee
        {
        public:
        int pl;
        void getdata()
        {
          cin>>pl;
        }

        void display()
        {
            cout<<"Number of programming language known: "<<pl<<endl;
        }
        };
        int main()
        {
            person obj1;
            employee obj2;
            programmer obj3;
            obj1.getdata();
            obj1.display();
            obj2.getdata();
            obj2.display();
            obj3.getdata();
            obj3.display();
            return 0;
       }
**11).Percentage of Student**

      #include <iostream>

      using namespace std;
      class AddData
      {
         public:
         int mark1,mark2;
          void accept_details()
          {
               cin>>mark1>>mark2;
           }
      };
      class sports
      {
        public:
          int mark3;
          void get()
          {
            cin>>mark3;
           }
          };
      class Total : public AddData,public sports
      {
        public:
          int d;
          void total_of_three_subjects()
          {
              d=(mark1+mark2+mark3)/3;
          }
       
        };
        class Percentage : public Total
        {
        public:
          int e;
          void calculate_percentage()
          {
            e=(mark1+mark2+mark3)/3;
          }
          void show_result()
          {
              cout<<e;
          }
        };
        int main()
        {   
             Percentage p;
             p.accept_details();
             p.get();
             p.total_of_three_subjects();
             p.calculate_percentage();
             p.show_result();
             return 0;
      }
**12).Bio**

      #include <iostream>

      using namespace std;
      class student
      {
        public:
        int roll_no,mark1,mark2;
        void get()
        {
            cin>>roll_no>>mark1>>mark2;
        }
        };
      class sports
      {
          public:
          int mark3;
          void getagain()
          {
            cin>>mark3;
          }
     };
      class statement : public student, public sports
      {
        public:
        void display()
        {
             cout<<"Roll No:"<<roll_no<<endl;
             cout<<"Total:"<<mark1+mark2+mark3<<endl;
             cout<<"Average:"<<(mark1+mark2+mark3)/3<<endl;
         }
        };
      int main()
      {
        statement obj;
        obj.get();
        obj.getagain();
        obj.display();
        return 0;
      }
**13).Interface for Rectangle**

      #include <iostream>

      #include <iomanip>
      using namespace std;
      class Area
      {
          public:
         float getArea(float l,float h);
      };

      float Area::getArea(float l,float h)
      {
        return l*h;
      }

      class Perimeter
      {
        public:
          float getPerimeter(float x,float y)
          {
              return (float)2*(x+y);
           }
      };

      class Rectangle:public Area,public Perimeter
      {
   
      };
    int main()
    {
        float l,b;
        Rectangle rt;
        cin>>l>>b;
        cout<<rt.getArea(l,b)<<endl;
        cout<< std::fixed << setprecision(2) << rt.getPerimeter(l,b);
        return 0;
    }
    
**14).Bank**

    #include <iostream>
    #include <math.h>
    using namespace std;

    class Customer {

    public:
    char s[100];
    public:
    void display()
    {
    cin>>s;
    }
    };

    class Bank{
    public:
    long num1, num2, num3;
    void display()
    {
    cin>>num1>>num2>>num3;
    }
    };

    class Account:public Customer,public Bank
    {
    public:
    char s[100];
    long num1,num2,num3;
    void display()
    {
    cin>>s;
    cin>>num1>>num2>>num3;
    cout<<"Customer Name="<<s<<endl;
    cout<<"Customer Id="<<num1<<endl;
    cout<<"Account No="<<num2<<endl;
    cout<<"Account Balance="<<num3<<endl;
    //Interest Calc

    double y = num3;
    y = floor((y * 100) + 0.5)/100;
    y = y*12*3;
    int interest = (int)y;
    printf("Interest=%d", interest/100);
    }
    };

    int main() {


    Account user;
    user.display();
    }
    
