**1).Jaganath and his Juniours**

    #include <iostream>

    using namespace std;

    class Point{
        int px;
    public:
      Point(int px){
        this->px = px;
      }
 
    void show(){
        cout << px << endl;
      }

      friend void operator++(Point &);
    };

    void operator++(Point &p){
      p.px++;
    }

    int main() {
      int px;
      cin >> px;
      Point ob1(px);
      ++ob1;
      ob1.show();
     return 0;
    }
 **2).Polio**
 
    #include <iostream>

    using namespace std;
    class country
    {
        public:
        virtual void getdata() = 0;
        virtual void display() = 0;
    }; 

    class state:public country
    {
        public:
         char a[20];
          int b,c;
          char d[20];
          int e,f;
      void getdata()
        {
          cin>>a>>b>>c>>d>>e>>f;
        }
        void display()
        {
            cout<<"Country Name "<<a;
              cout<<endl<<"Country Polio% "<<b;
              cout<<endl<<"Country Litteracy%"<<c;
              cout<<endl<<"The Measure of Interdependency "<<(float)b/c;
              cout<<endl<<"State Name "<<d;
              cout<<endl<<"%Age of Polio of State "<<e;
              cout<<endl<<"%Age of Literacy of State "<<f;
              cout<<endl<<"The Measure of Interdependency "<<(float)e/f;
       }
      };
      int main() {
        state s;
          s.getdata();
          s.display();
      return 0;
    }
**3).Engineering Counselling**

      #include <iostream>

      using namespace std;

      class Counselling{
      int num, m1, m2, m3;
        string name;
      public:
        void read(){
          cin >> num >> name >> m1 >> m2 >> m3;
        }
 
 
          friend class enggstudent; 
        };

        class enggstudent{
            float co;
             int tot;
      public:
        void cutoff(Counselling c){
          tot = c.m1+c.m2+c.m3;
          co = (tot)/3.0;       
      }
        void display(Counselling c){
            cutoff(c);
            cout << c.num << " " << c.name << " ( " << c.m1 << " " << c.m2 << " " << c.m3 << " ) " << tot << " " << co << endl;
        }
      };

      int main() {
        int n;
       cin >> n;
       Counselling c;
       enggstudent ceg;
        cout << "Number Name Marks Total Cutoff" << endl;
        for(int i=0; i<n; i++){
            c.read();
             ceg.cutoff(c);
            ceg.display(c);
          }
       return 0;
      }
**4).Shape and Measurements**

    #include<iostream>
    using namespace std;
    class Shape {
    public:
    virtual int getPerimeter()=0;
    };

      class Rectangle:public Shape {
      public:
      int getPerimeter()
      {
        int a,b;
        cin>>a>>b;
        return 2*(a+b);
      }
    };

      int main() {
      Shape *ptr = new Rectangle;
      Rectangle r;
      int perimeter;
      perimeter=r.getPerimeter();
      cout<<"Perimeter of Rectangle is: "<<perimeter;
      return 0;
    }
 **5).Numbers**
 
    #include <iostream>

    using namespace std;

    class Super{
    public:
       virtual void nSum()=0;
    };

    class Sub:public Super{
        int n, b, c;
        public:
          void read(){
          cin >> n;
      }
      void nSum(){
          cout << (n*(n-1)/2)+n << endl;
      }
      };

      int main() {
 
      Super *s;
      Sub sb;
      s=&sb;
      sb.read();
      s->nSum();
     return 0;
    }
**6).Difference Problem**

      #include <iostream>

      using namespace std;
      class parent
      {
        public:
        virtual void difference(int a, int b)=0;
      };
      class child:public parent
        {
          public:
          int z;
          void difference(int a, int b)
          {
            z=a-b;
            cout<<"Difference="<<z;
          }
        };
        int main()
        {
           parent *p;
           child c;
           p=&c;
           int a,b;
            cin>>a>>b;
            p->difference(a,b);
            return 0;
        }
**7).Friends in Maths tutuion**

    #include <iostream>
    using namespace std;
    class complex
    {
        public:
        int a,b,c,d;
        friend void sum();
        void input()
        {
          cin>>a>>b>>c>>d;
        }
      void display()
      {
          cout<<a+c<<"+i"<<b+d;
      }
    };
    void sum(complex obj)
    {
      }
      int main()
      {
         complex obj;
         obj.input();
         obj.display();
          return 0;
      }
**8).Measure the Area**

      #include <iostream> 
      using namespace std;
      class Shape
      {
          protected:
          double x, y;
          public:

          void set_dim(double i, double j=0)
          {
              x = i;
              y = j;
          }
        virtual int getArea()=0;
        };

      class Rectangle:public Shape{
      public:

      int getArea() {
          cout <<"Area of Rectangle is:"<< x * y << "\n";
      }
      };

      main(void)
      {
          Shape *p;
          Rectangle r;
          int l,b;
          cin>>l>>b;
          p = &r;
          p->set_dim(l, b);
          p->getArea();
          return 0;
          }
 **9).Multiples**
 
      #include <iostream>

      using namespace std;

      class base{
      public:
      virtual void mTable()=0;
      };

      class derived:public base{
      int i1, i2;
      public:
      void input(){
          cin >> i1;
      }
      void mTable(){
          cout << i1*1 << " " << i1*2 << " " << i1*3 << " " << i1*4 << " " << i1*5 << endl;
      }
      };

      int main() {
 
         base *b;
         derived d;
         b=&d;
         d.input();
         b->mTable();
         return 0;
      }  
**10).Super Market**

    #include <iostream>

    using namespace std;
    class consumer
    {
        public:
        virtual void getdata()=0;
        virtual void display()=0;
    };

    class transaction:public consumer
    {
      public:
          int c,q,p,tp;
          long t;
          char n[100];
          void getdata()
          {
              cin>>n>>c>>t>>q>>p>>tp;
           }
           void display()
          {
                cout<<"Name : "<<n<<endl;
                cout<<"Code : "<<c<<endl;
                 cout<<"Telephone : "<<t<<endl;
                cout<<"Quantity : "<<q<<endl;
                 cout<<"Price : "<<p<<endl;
                tp=q*p;
                cout<<"Total Price : "<<tp<<endl;
        }

        };

        int main()
        {
          consumer *c;
          transaction t;
           c=&t;
          c->getdata();
          c->display();
          return 0;
          }
 **11).Jadeja and Googly**
 
      #include <iostream>

      using namespace std;

      class googly{
       int num;
         public:
        void getballnumber(){
         cin >> num;
        }
        friend int isgoogly(googly);
      };

      int isgoogly(googly g){
      if(g.num%2 == 0){
        cout << "Not a Googly Ball" << endl;
        return 0;
      }
      cout << "Googly Ball" << endl;
       return 1;
      }

    int main() {
        googly e1;
        e1.getballnumber();
        isgoogly(e1);
        return 0;
    }
**12).Kajal and her Shopping**

      #include <iostream>

      using namespace std;
      class Bill
        {
          public:
          int a,b;
          void getamount()
          {
              cin>>a>>b;
          }
          friend float billavg(Bill&,int,int);
          };
          float billavg(Bill& x,int a,int b)
          {
            float y;
            y=(float)(a+b);
            return y/2;
          }
          int main()
          {
          Bill obj;
          obj.getamount();
          cout<<"Average amount spent:"<<billavg(obj,obj.a,obj.b);
        return 0;
        }
 **13).ONGC**
 
    #include<iostream>
    using namespace std;
    class Employee
    {public:
    virtual int getSalary()=0;
    };
    class Developer:public Employee
    {
        public:
        int salary;
        int getSalary()
        {cin>>salary;
      cout<<"Salary of Developer : "<<salary<<endl;
      }};
      class Driver:public Employee
      {public :
    int getSalary()
    {int salary;
    cin>>salary;
    cout<<"Salary of Driver : "<<salary;}};

    int main() {
    Developer d;
    d.getSalary();
    Driver w;
    w.getSalary();
    return 0;
    }
 **14).Varun and his Students**
 
    #include <iostream>
    using namespace std;

    class parent{
    public:
    virtual float average(int a, int b, int c)=0;

    };

    class child:public parent{
    public:
    float average(int a, int b, int c){
    return (a+b+c)/3.0f;
    }
    };

    int main() {

    parent *p;
    child c;
    p=&c;
    int a,b,d;
    cin>>a>>b>>d;
    cout << "Average=" << p->average(a,b,d);
    return 0;
    }
**15).District Sports Meet**

    #include <iostream>

    using namespace std;
    class Sports
    {
      public:
        virtual void getdata();
        virtual void display();
    };
    void Sports::getdata()
    {}
      void Sports::display()
    {}
    class Student:public Sports
     {
      private:
      long roll;
      string name;
      public:
      void getdata()
      {
         cin>>roll>>name;
      }
      void display()
      {
        cout<<"Student Name is: "<<name;
        cout<<"\nStudent Roll no is: "<<roll;
      }
      };
      int main() {

 
            Student o;
   
           o.Student::getdata();
           o.Student::display();
       return 0;
      }
 
