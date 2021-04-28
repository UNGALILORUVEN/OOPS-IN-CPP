**1.)Smart Appraisal System**

    #include <iostream>
    #include <string.h>
    using namespace std;
    class TestClass
    {
      public:
    class Appraisal
    {
      int sal;
      public:
      void in()
      {
        cin>>sal;
      }
      void out()
      {
        cout<<"\nNew Salary:"<<sal;
      }
      Appraisal()
      {
        sal=30000;
        cout<<"Old Salary:"<<sal;

      }
    };
    };
    int main() {

     TestClass::Appraisal myobj;
      TestClass::Appraisal myobj2();
      myobj.in();
      myobj.out();
     return 0;
    }

**2.)STORE KEEPER**

    #include <iostream>
    using namespace std;
    class Store
    {
      public:
      int itemcount(int id)
      {
        cout<<id;
      }
      int itemcount(int totalavl,int remaining)
      {
        int a;
        a=totalavl-remaining;
          cout<<"\n"<<a;
      }
    };
    int main()
    {
      int a,b,id;
      cin>>id>>a>>b;
      Store ob;
      ob.itemcount(id);
      ob.itemcount(a,b);
     return 0;
    }

**3.)DHONI THE CEO**

    #include <iostream>
    using namespace std;
    class TestClass
    {
      public:
    class Salary
    {
      public:
      Salary()
      {
        int deftsalary;
        deftsalary=10000;
        cout<<deftsalary<<endl;
      }
      Salary(int ExpectedSalary)
      {
        cin>>ExpectedSalary;
        cout<<ExpectedSalary<<endl;
      }
    };
    };
    int main()
    {
      TestClass::Salary myobj;
      int ExpectedSalary;
      cin>>ExpectedSalary;
      TestClass::Salary myobj2(ExpectedSalary);
      return 0;
    }   

**4.CUB**
 
     #include <bits/stdc++.h>
    using namespace std;
    class AccBalance
    {
      public:
      AccBalance()
      {
        cout<<"Zero Balance";
      }
      AccBalance(float bal)
      {
        if(bal>0)
          cout<<"\nPositive";
        else if(bal<0)
          cout<<"\nNegative";
        else
          cout<<"\nZero";
      }
    };
    int main()
    {
      float amount;
      cin>>amount;
      AccBalance defltBal;
      AccBalance currBal(amount);
      return 0;
    }

**5.)DATABASE ADMINISTRTATOR**

     #include <iostream>
    #include<string.h>
    using namespace std;

    class StudentData
    {char stuName[50];
      public:
     StudentData()
      { cout<<"Student Name is: New Student"<<endl;}
     StudentData(char *n)
     { strcpy(stuName,n);
      cout<<"Student Name is: "<<stuName;}
    };

      class TestClass
    { char n[50];
     public:
     TestClass()
     {StudentData myobj;
      cin>>n;
      StudentData myobj2(n);}
    };

    int main() {
     TestClass t;
     return 0;
    }

**6.)FILL WATER** 

    #include <iostream>
    using namespace std;
    class Box
    {
    double width, height, depth;

    public:
    Box()
    {
    width = 0;
    height = 0;
    depth = 0;
    }
    Box(double samevalue)
    {
    width = samevalue;
    height = samevalue;
    depth = samevalue;
    }
    double volume()
    {
    return width * height * depth;
    }
    };
    int main()
    {
    Box mybox1;
    double a, vol;
    cout << mybox1.volume() << endl;
    cin >> a;
    Box mybox2(a);
    vol = mybox2.volume();
    cout << vol;
    return 0;
    }

**7.)SRM ADMISSION**
 
     #include <iostream>
    #include <string.h>

    using namespace std;

    class Student{
      public:
      void Identity(int id,char name[100]);
      void Identity(char name[100],int id);
      void Identity(char name[100],char id[100]){
        char temp[100];
        if(isdigit(name[0])) { 
          strcpy(temp,name);
          strcpy(name,id);
          strcpy(id,temp);
        }
        cout<<name<<" "<<id<<endl;
      }
    };

    int main() {
      Student s1;
      char name[100],id[100];
      cin>>name;
      cin>>id;
      s1.Identity(name,id);
      cin>>name;
      cin>>id;
      s1.Identity(name,id);
    }
 
**8.)BUSINESS MAN**   

    #include <iostream>
    using namespace std;
    class TestClass
    {
      public:
    class profit
    {
      int Income=0,Expenses;
     public:
      void in()
      {
        cin>>Income>>Expenses;
      }
      void out()
      {
        cout<<Income-Expenses;
      }
      profit()
      {
        Income=0;
        Expenses=0;
      }
      profit(int income,int expenses)
      {
        Income=income;
        Expenses=expenses;
      }
    };
    };
    int main() {
     TestClass :: profit s1(0,0);
      s1.in();
      s1.out();
     return 0;
    }

**9.)EFFICIENCY OF CAR** 

    #include <iostream>
    using namespace std;
    class Car
    {
      public:
      float startMiles, endMiles, litres;
      int perlitre;
      void initializeData(float s,float e,float l)
      {
        cin>>startMiles>>endMiles>>litres;
      }
      float getstartMiles()
      {
        return startMiles;
      }
      float getEndMiles()
      {
        return endMiles;
      }
      float getLitres()
      {
        return litres;
      }
      double calculateMPL()
      {
        perlitre = (endMiles-startMiles)/litres;
        return perlitre;
      }
      string isEconomycar()
      {
        if(perlitre>18)
          return "true";
        else if(perlitre<18)
          return "false";
        else
          return "Improper readings";
      }
    };
    int main()
    {
        Car obj;
        float a, b, c;
        obj.startMiles;
        obj.endMiles;
        obj.litres;
        obj.perlitre;
       obj.initializeData(a, b, c);
        if(obj.calculateMPL()>=0)
        {
          cout<<obj.getstartMiles()<<endl;
          cout<<obj.getEndMiles()<<endl;
          cout<<obj.calculateMPL()<<endl;
          cout<<obj.getLitres()<<endl;
          cout<<obj.isEconomycar()<<endl;
        }
        else
          cout<<"Improper readings"<<endl;
        return 0;
    }
**10.)HOSPITAL BILL** 

    #include  <iostream>
    using namespace std;
    class Hospital
    {
    public:
    float bill(float medicines, float days)
    {
    float sum = medicines * days;
    return sum;
    }
    int bill(int room, int days)
    {
    int sum = room * days;
    return sum;
    }
    };

    int main()
    {
    Hospital ob;
    float a, b;
    cin >> a >> b;
    float sum1 = ob.bill(a, b);
    cout << sum1 << endl;
    cin >> a >> b;
    float sum2 = ob.bill(a, b);
    cout << sum2 << endl;
    return 0;
    }
**11).Anti-Proxy Attendance**

        #include <iostream>
        #include <string.h>
        using namespace std;
        class Student
        {
            char stuname[20];
            public:
            Student()
            {
            cout<<"No Attendance";
            }
        Student(char name[])
        {
            strcpy(stuname,name);
        }
        void display()
        {
            cout<<"\nHello "<<stuname<<endl;
        }
        };
        int main()
        {
            Student stdabs;
            char name[20];
            cin>>name;
            Student stdpst(name);
            stdpst.display();
            return 0;
        }
**12).Olympic Gold for India**

        #include <iostream>
        using namespace std;
        class Olympic
        {public:
        int distance(int D1,int D2)
        {return D1+D2;}
        int distance(int D3,int D4,int D5)
        {return D3+D4+D5;}
        };
        int main() {
        Olympic ob;
            int D1,D2,D3,D4,D5;
            cin>>D1>>D2>>D3>>D4>>D5;
            cout<<ob.distance(D1,D2)<<" meters"<<endl;
            cout<<ob.distance(D3,D4,D5)<<" meters"<<endl;
 
        return 0;
        }
**13).Limka Book of Records**

        #include <iostream>
        using namespace std;
        class Welcomemsg
        {
        public:
        char msg(char fstname[100])
        {
            cout<<"Hi "<<fstname<<endl;
            return 0;
        }
        char msg(char fstname[100],char lstname[100])
        {
        cout<<"Welcome "<<fstname<<" "<<lstname<<endl;
        return 0;
        }
        };

        int main()
        {
            Welcomemsg ob;
            char first_name1[100], first_name2[100], last_name2[100];
            cin>>first_name1>>first_name2>>last_name2;
            ob.msg(first_name1);
            ob.msg(first_name2,last_name2);
            return 0;
        }
 **14).Saravana Stores**
 
        #include <iostream>
        using namespace std;
        class Salary
        {
        public:
        int Increment(int currsal)
        {
             return currsal;
        }
        int Increment(int currsal,int bonus)
        {
        int c;
        c = currsal+bonus;
        return c;
        }
        };
        int main()
        {
        int currsal,bonus;
        cin>>currsal>>bonus;
        Salary ob;

        //cout<<currsal<<endl<<(currsal+bonus);
        cout<<ob.Increment(currsal)<<endl;
        // cout<<x<<endl;
        cout<<ob.Increment(currsal,bonus)<<endl;
        return 0;

        }
**15).Profit of the Day**

    #include <iostream>

    #include<iomanip>
    using namespace std;
    class profit
    {
        public:
        float p;
        profit()
        {
             p=0;
        }
         profit(int income,int expenses)
        {
            p=((float(income)/float(expenses))*100)-100;
            cout<<fixed<<setprecision(2)<<p<<"%";
        }
    };
    int main() {
    int i,n;
    cin>>i>>n;
    profit share(i,n);
 
    return 0;
    }
**16).BCD Game**

        #include <iostream>
        using namespace std;

        class Code
        {
        int number;

        public:
        void initializeData(int n)
        {
            number = n;
        }
        int convertToStraightBinary()
        {
        int binaryNum[12];
        int i = 0;
        while (number > 0)
        {
        binaryNum[i] = number % 2;
        number = number / 2;
        i++;
        }
        FILL:
        if (i < 12)
        {
            binaryNum[i] = 0;
            i++;
            goto FILL;
        }
        for (int j = i - 1; j >= 0; j--)
        cout << binaryNum[j];
        }
        };

        int main()
        {
        Code obj;
        int n;
        cin >> n;
        obj.initializeData(n);
        obj.convertToStraightBinary();
        return 0;
        }


