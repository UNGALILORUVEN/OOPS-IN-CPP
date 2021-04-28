**1.)OPERATOR !**

     #include <iostream>
    #include<cstring>
    using namespace std;
    class mystring
    {
      char str[100];
      public:

      void operator !();
      void operator ==(mystring&)
      {
        cout<<str;
      }
      void acccept_string()
      {
        cin>>str;
      }
    };
    void mystring::operator!()
    {
      int in = strlen(str);
      for(int i=0;i<in;i++)
      {
        if(str[i]>='a'&&str[i]<='z')
          str[i]=str[i]-32;
        else if(str[i]>='A'&&str[i]<='Z')
          str[i]=str[i]+32;
      }
    }

    int main()
    {
    mystring s1,s2;
      s1.acccept_string();
      !s1;
      s1 == s2;

     return 0;
    }
    
**2.)TRAVEL**

     #include <iostream>
    using namespace std;

    class Distance {
       public:
          int feet;
          int inches;
       public:

          Distance(){
             feet = 0;
             inches = 0;
          }
          Distance(int f, int i){
             feet = f;
             inches = i;
          }
          // method to display distance
          void displayDistance() {
             cout <<"Feet="<<feet<<" Inches="<<inches<<endl;
          }
          // overloaded minus (-) operator
          Distance operator - () {
             cout<<"Travelling Backwards\n";
             return Distance(-feet, -inches);
          }
          Distance operator + () {
             cout<<"Travelling Forward\n";
             return Distance(feet, inches);
          }

    };

    int main() {
       int m,n;
       cin>>m>>n;
       Distance D1(m,n);
       +D1;
        D1.displayDistance();
       -D1;                   
       D1.displayDistance(); 
       return 0;
    }
    
**3.)SAVINGS**

    #include <iostream>
    using namespace std;
    class Money
    {
    private:a
    int rupees,Paise;
    public:
    Money()
    {
    cin>>rupees>>Paise;
    }
    Money operator +(Money o)
    {
    Money temp;
    temp.rupees=rupees+o.rupees;
    temp.Paise=Paise+o.Paise;
    return temp;
    }
    Money operator -(Money o)
    {
    Money temp;
    temp.rupees=rupees-o.rupees;
    temp.Paise=Paise-o.Paise;
    return temp;
    }
    void display()
    {
    cout<<"Rs="<<rupees<<" and "<<Paise<<" Paise"<<endl;
    }
    };
    int main()
    {
    Money M1,M2,M3,M4,M5;
    M4=M2-M3;
    M5=M1+M4;
    M5.display();
    return 0;
    }

**4.)COPY** 

    #include <iostream>
    #include<string.h>
    using namespace std;
    class mystring
    {
      char a[100];
      public:
      char b[100];
      void getdata()
      {
        cin>>a;
      }
      void operator ==(int c)
      {
        strcpy(b,a);
      }
    };
    int main()
    {
      mystring obj;
      obj.getdata();
      int a=3;
      obj.operator ==(a);
      cout<<"Copied String is:"<<obj.b;
      return 0;
    }
    
**5.)PLAY WITH FRACTION**

     #include <iostream>
    using namespace std;
      class Fraction
      {
        public:
        int numerator,denominator;

        Fraction()
        {
          numerator=0;
          denominator=0;
        }

        void getinput()
        {
          cin>>numerator>>denominator;
        }

        Fraction operator+(Fraction obj)
        {
          Fraction temp;
          temp.numerator=(numerator*obj.denominator)+(denominator*obj.numerator);
          temp.denominator=denominator*+obj.denominator;
          return temp;
        }
      };

       int main()
       {
         Fraction f1,f2,add;
         f1.getinput();
         f2.getinput();
         //+obj;
         add=f1+f2;
         cout<<add.numerator<<"/"<<add.denominator;
       // add.output();

    return 0;
    }

**6.)FIRST DAY OF COLLEGE**

     #include <iostream>
    using namespace std;
    class vector
    {
      private:
      int x,y,z;
      public:
      vector()
      {
        cin>>x>>y>>z;
      }
      vector operator+(vector b)
      {
        vector temp;
        temp.x=x+b.x;
        temp.y=y+b.y;
        temp.z=z+b.z;
        cout<<"Sum="<<temp.x<<"i+"<<temp.y<<"j+"<<temp.z<<"z"<<endl;
      }
    };
    int main()
    {
      vector a,b,c;
      c=a+b;
      return 0;
    }
    
 **7.)UNARY**

    #include <iostream>
    using namespace std;
    class data
    {
    public:
      double x, y;
      double a, b;
      void setdata()
      {
        cin >> x >> y;
        cin >> a >> b;
      }
      void display1()
      {
        cout << x << " " << y;
      }
      void display2()
      {
        cout << a << " " << b;
      }

      data operator*()
      {
        x = -x;
        y = -y;
        a = -a;
        b = -b;
      }
    };
    int main()
    {
      data ob1;
      ob1.setdata();
      *ob1;
      ob1.display1();
      cout << "\n";
      ob1.display2();
      return 0;
    }

**8.)PREFIX INCREMENT**

     #include <iostream>
    using namespace std;
    class increment
    {
      public:
      float a,b,c;
      void getx()
      {
        cin>>a>>b>>c;
      }
      void operator ++();

    };
    void increment::operator ++()
      {
       a=a+1.0;
      b=b+1.0;
      c=c+1.0;
       cout<<a<<" "<<b<<" "<<c;
    }
    int main() {
     increment obj;
      obj.getx();
      obj.operator ++();
     return 0;
    }

**9.)DECIMAL INCREAMENT**

     #include <iostream>
    using namespace std;
    class Decimal
    {
      float a;
      public:
      void in()
      {
        cin>>a;
      }
      void operator ++()
      {
       a=a+0.10;
       cout<<a;
      }
    };
    int main() {
     Decimal obj;
      obj.in();
      obj.operator ++();
     return 0; }
     
**10.)ICE CREAM SELLER**

    #include <iostream>
    using namespace std;
    class matrix
    {
       matrix operator * ()
        {

        }
       void get()
        {
        }
       void put()
        {
        }
    };
    int main()
    {
        double a[10][10], b[10][10], mult[10][10], r1, c1, r2, c2; int i, j, k;
        r1 =2; c1=2;
        r2 =2; c2=1;
        while (c1!=r2)
        {
            cin >> r1 >> c1;
            cin >> r2 >> c2;
        }
        for(i = 0; i < r1; ++i)
            for(j = 0; j < c1; ++j)
            {
                cin >> a[i][j];
            }
        for(i = 0; i < r2; ++i)
            for(j = 0; j < c2; ++j)
            {
                cin >> b[i][j];
            }
        for(i = 0; i < r1; ++i)
            for(j = 0; j < c2; ++j)
            {
                mult[i][j]=0;
            }
        for(i = 0; i < r1; ++i)
            for(j = 0; j < c2; ++j)
                for(k = 0; k < c1; ++k)
                {
                    mult[i][j] += a[i][k] * b[k][j];
                }
        for(i = 0; i < r1; ++i)
        for(j = 0; j < c2; ++j)
        {
            cout << mult[i][j];
            if(j == c2-1)
                cout << endl;
        }
        return 0;
    }
**11).Light House**

     #include <iostream>

     using namespace std;
     class Time
     {
          int hours,mins,secs;
          public:
          void operator >>(int b)
          {
               cin>>hours>>mins>>secs;
          }
          void operator <<(int b)
          {
               cout<<hours<<" Hours "<<mins<<" Mins "<<secs<<" secs";
          }
     };
     int main() {
     Time t;
     int a=3;
          t.operator >>(a);
          t.operator <<(a);
     return 0;
     }
**12).Compare Distance**

     #include<iostream>
     using namespace std;
     class Distance
     {
          public:
          int feet,inches,feet2,inch2;
          void displayDistance()
          {  
               cin>>feet>>inches>>feet2>>inch2;
          }
          void operator <(int b)
          {
               if(feet>feet2)
               cout<<"First One is Greater";
               else if(feet==feet2 && inches>inch2)
                    cout<<"First One is Greater";
               else if(feet<feet2)
                    cout<<"Second One is Greater";
               else if(feet==feet2 && inches<inch2)
                    cout<<"Second One is Greater";
               else
                    cout<<"Both are equal";
          }
          };
          int main()
          {
               Distance d;
               d.displayDistance();
               int a=3;
               d.operator <(a);
               return 0;
          }
**13).Distance**

          #include <iostream>
          using namespace std;
          class Distance
          {
               private:
               int feet,inches;

               public:

               void readDistance(void)
               {
                    cin >>feet;
                    cin >>inches;
               }

               void dispDistance()
               {
                    cout << "Feet:" << feet << " " << "Inches:" << inches << endl;
               }
               Distance operator +(Distance &dist1)
               {
                    Distance tempD;
                    tempD.inches= inches + dist1.inches;
                    tempD.feet = feet + dist1.feet + (tempD.inches/12);
                    tempD.inches=tempD.inches%12;
                    return tempD;
               }
               };
               int main()
               {
               Distance D1,D2,D3;

               D1.readDistance();
               D2.readDistance();
               D3=D1+D2;
               D3.dispDistance();
               return 0;
               }
**14).Concatenate**

          #include <iostream>

          using namespace std;
          class concatenate
          {
               char a[100],b[100];
                public:
                void read()
          {
               cin>>a>>b;
          }
          void operator +()
          {
               cout<<a<<b;
          }
          };
          int main() {
          concatenate obj;
          obj.read();
          obj.operator +();
          return 0;
          }
 **15).Decimal Decrement**
 
          #include <iostream>

          using namespace std;
          class Decimal{
          float a;
               public:
               void in(){
               cin>>a;
               }
          void operator --(){
          a=a-0.10;
          cout<<a;
          }
          };
          int main() {
          Decimal obj;
          obj.in();
          obj.operator --();
          return 0; }
