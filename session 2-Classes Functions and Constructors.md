**1).TNEB Billing**

    #include<iostream> 
    using namespace std;
    class Electric
    {
      public:
      float unit;
    char name[20];
    void accept()
    {

      cin>>name;

      cin>>unit;
      }
    void print_bill();
    };
    void Electric::print_bill()
    {
      float bill;
      if(unit>=0 && unit<=100)
      bill=(500+(unit*0.40));
      else if(unit>100 && unit<=300)
      bill=(500+(100*0.40)+((unit-100)*0.50));
      else if(unit>300)
      bill=(500+(100*0.40)+(200*0.50)+((unit-300)*0.60));
      if(bill>250)
        bill=(bill+(bill*(15/100)));
      cout<<"\nConsumer Name:"<<name;
      cout<<"\nConsumed:"<<unit;

      cout<<"\nBill to pay:"<<bill;
    }
    int main ()

    {

    Electric e[10];

    int i,cnt;
    cin>>cnt;
    cout<<"\nNumber of Consumers:"<<cnt;
    for(i=0;i<cnt;i++)
    {
     e[i].accept();
    }
    for(i=0;i<cnt;i++)
    {
      e[i].print_bill();
    }
    return 0;
    }
**2).Student Details**

    #include <iostream>
    using namespace std;
    #include<string>
    class student
    {
      private:
      int roll;
      string name;
      float height;
      float weight;
      public:
     student()
    {
      name="Nikhil";
      roll=20;
      height=165.5;
      weight=58.2;
    }
    void read()
    {
        cin>>name>>roll>>height>>weight;
    }
    void display()
    {
      cout<<name<<" "<<roll<<" "<<height<<" "<<weight<<endl;
   
      }
    };
    int main() {
    student s1,s2;
    s1.read();
    s1.display();
    s2.display();
    return 0;
    }
**3).CRICBUZZ**

    #include <iostream>
    #include<string>
    using namespace std;
    class Cricket
    {public:
    string playername;
    int jerseynum;
    int no_of_innings;
    int counter;
      Cricket(int n,string c,int no)
      {
   
          jerseynum=n;
          no_of_innings=no;
          playername=c;
      }
   
      void show()
      {
   
          cout<<"Jersey Num:"<<jerseynum<<endl;
          cout<<"Name of the Player:"<<playername<<endl;
          cout<<"No of Innings Played:"<<no_of_innings<<endl;
   
      }
      void count()
      {
   
   
          cout<<counter;
   
   
      }
    };

    int main() {
    int a,b,h,d;
    string e,f;
    cin>>a>>e>>b;
    cin>>h>>f>>d;
    Cricket lib1(a,e,b);
    Cricket lib2=Cricket(h,f,d);
    lib1.show();
    lib2.show();
 
    return 0;
    }
 **4).Pamban Bridge**
 
      #include <iostream>
      using namespace std;
      class tollbooth{
      public:
      int carsPassed;
      float tollCollected;
      tollbooth(){
        carsPassed=0;
        tollCollected=0;
      }
      void payingcar(double pay){
        carsPassed++;
        tollCollected+=pay;
      }
      void nonpayingcar(){
      carsPassed++;
      }
      void display(){
        cout << "Total number of cars passed = " << carsPassed << endl;
        cout << "Total amount collected = " << tollCollected << endl;
      }
      };
      int main() {
      tollbooth obj;
        char vehicleNumber[10];
        float payAmount;
        int carsPassed,i;
        cin >> carsPassed;
        for(i=0;i<carsPassed;i++){
         cin >> vehicleNumber >> payAmount;
          if(payAmount>0) obj.payingcar(payAmount);
          else obj.nonpayingcar();
      }
      obj.display();
      return 0;
    }
 **5).Digital Library**
 
      #include <iostream>
      using namespace std;
      class Library
      {
        public:
        string name;
        int r, bc, c = 0;

        Library(int a, string s, int b)
        {
          name = s;
          r = a;
          bc = b;
        }

        void show()
        {
            cout << "Roll No:" << r << endl
              << "Name of the Student:" << name << endl
              << "Code of Book Accessed:" << bc << endl;
        }

        void count()
        {
          c++;
        }
      };

      int main()
      {
          int s, p, q, r;
            string n, m;
          cin >> s >> n >> p >> q >> m >> r;

         Library lib1(s, n, p);
          lib1.show();
         Library lib2(q, m, r);
        lib2.show();
        return 0;
      }
 **6).DATE CLASS**
 
    #include <iostream>
    using namespace std;
    class Date{
      int day,month,year;
      public:
    Date(){
      cin >> day >> month >> year;
    }
      void getDate(){
      switch(month){
          case 1: cout << "January ";
            break;
          case 2: cout << "February ";
            break;
         case 3: cout << "March ";
            break;
         case 4: cout << "April ";
            break;
        case 5: cout << "May ";
            break;
        case 6: cout << "June ";
            break;
        case 7: cout << "July ";
            break;
        case 8: cout << "August ";
            break;
        case 9: cout << "September ";
            break;
        case 10: cout << "October ";
            break;
        case 11: cout << "November ";
            break;
        case 12: cout << "December ";
            break;
      }
      cout << day << " " << year;
    }
    };
    int main() {
        Date D;
        D.getDate();
        return 0;
    }
 **7).Land Survey**
 
      #include<iostream>

    using namespace std;

    class room
    {
      int l,b,h;
        public :
        void getroom()
      {
      cin>>l>>b>>h;
      }
      void putroom()
              {
                cout<<"Length="<<l;
                    cout<<endl;
                cout<<"Breadth="<<b;
                    cout<<endl;
                cout<<"Height="<<h;
                    cout<<endl;
              }
      };
      class address {
      int hno;
      char cty[30];
      char state[30];
        public :
      void getad()
      {
        cin>>hno;
        cin>>cty;
        cin>>state;
      }
      void putad()
     {
          cout<<"House No="<<hno;
                   cout<<endl;
                   cout<<"City="<<cty;
                   cout<<endl;
                   cout<<"State="<<state;
                    cout<<endl;
      }
    };

    class house{
    char housename[30];
    address a;
    room r[10];
    int n;

    public :
      void input();
      void display();
    };
    void house :: input()
    { 
      cin>>housename;
      cout<<"House name="<<housename<<endl;
      a.getad();
      a.putad();
      cin>>n;
 
      for(int i=0;i<n;i++){
 
      r[i].getroom();
     }
      }
      void house :: display()
      { 

      for(int i=0;i<n;i++){
      cout<<"Details of Room "<<i+1<<"\n";
      r[i].putroom();
      }
      }

      int main()
      {
      house x;
      x.input();
      x.display();
      return 0;
      }
 **8).Bhagavan the Inspirational Teacher**
 
       #include <iostream>
       using namespace std;

      class Student{
      public:
    int roll;
    string name;
    float height,weight;
    void readinput();
    void displaydata();
    Student(){
    name = "Bhagavan";
    roll = 1593;
    height = 172.5;
    weight = 60.4;
    }
    };

    void Student::readinput(){
    cin>>name>>roll>>height>>weight;
    }

    void Student::displaydata()
    {
    cout<<name<<" "<<roll<<" "<<height<<" "<<weight;
    }

    int main() {
    Student s1,s2;
    s1.readinput();
    s1.displaydata();
    cout<<endl;
    s2.displaydata();
    return 0;
    }
 **9).Complex Game**
 
        #include <iostream>
        using namespace std;
        class Complex
        {
            public:
            int r1,i1,r2,i2,r,i;
            Complex()
            {
                cin>>r1>>i1>>r2>>i2;
            }
            void addcomplex()
        {
            r=r1+r2;
            i=i1+i2;
        }
        void displaycomplex()
        {
            cout<<r1<<"+"<<i1<<"i";
            cout<<"\n"<<r2<<"+"<<i2<<"i";
            cout<<"\n"<<r<<"+"<<i<<"i";
        }
        };
   
        int main() {
         Complex obj;
        obj.addcomplex();
        obj.displaycomplex();
        return 0;
        }
 **10).Arulmozhivarman and his pets**
 
        #include <iostream>
        using namespace std;

        class catanddog
        {public:
        int c,d,l,t;
        void count()
        {
            cin>>t;
            while(t--){
            cin>>c>>d>>l;
            long int u=l-4*d;
            if(u<0||(u%4!=0)||u>4*c)
                cout<<"no";
                else cout<<"yes";
                cout<<endl;
        }
        }
        }obj;
        int main()
        {
            obj.count();
            return 0;
        }
**11).Find your Partner**

        #include <iostream>

        using namespace std;

        class partner{
        string num;
        string arr[8][2] = {{"3", "6UB"},{"6", "3UB"},{"2", "5MB"},{"5", "2MB"},{"1", "4LB"},{"4", "1LB"},{"7", "8SU"},{"8", "7SL"}};
        public:
        partner(string num){
            this->num = num;
        }
        void findpartner(){
         for(int i=0; i<8; i++){
            if(num == arr[i][0]){
                cout << arr[i][1] << endl;
            break;
        }
        }
        }
        };

        int main() {
 
 
        int n;
        string num;
        cin >> n;
        for(int i=0; i<n; i++){
        cin >> num;
        partner objname(num);
        objname.findpartner();
        }
        return 0;
        }
**12).TRAI**

        #include <iostream>

        using namespace std;
        class Phone{
        public:
        int stdCode,exchangeCode,phoneNumber;
        void change(){
        char inputNumber[13];
        cin >> inputNumber;
        int test[13],i;
        for(i=0;i<13;i++){
            test[i] = inputNumber[i];
            test[i]-=48;
        }
        for(i=0;i<3;i++){
            if(test[i]==0) test[i]=91;
            cout << test[i];
        }
            for(i=3;i<13;i++){
            cout << inputNumber[i];
        }
        }
   
        };
        int main(){
        Phone obj;
        obj.change();
        return 0;
        } 
**13).Athithya Karihalan and his Hobby**

        #include <iostream>
        #include <math.h>
        using namespace std;
        class Building
        {
            private:
            int length, width, ratePerSqFeet;
            public:
            void initializeData(int l, int w, int r)
            {
                length=l;
                width=w;
                ratePerSqFeet=r;
            }
            void getLength(int length, int width, int ratePerSqFeet)
            {
                 cout<<"Length : "<<length<<endl;
            }
        void getWidth()
        {
            cout<<"Width : "<<width<<endl;
        }
        void getRatePerSqFeet()
        {
            cout<<"Rate Per SqFt : "<<ratePerSqFeet<<endl;
        }
        void calculateCost()
        {
            int z;
            z=length*width*ratePerSqFeet;
            cout<<"Cost of the Building : "<<z<<endl;
        }
            void determineSuitability()
        {
            if(length==60)
            {
                if(abs(length-width)>10)
                cout<<"Suitability : Suitable";
            }
                else if(length==width)
                cout<<"Suitability : Suitable";
                else if(abs(length-width)<10)
                {
                    cout<<"Suitability : Suitable"<<endl;
                }
                else
                {
                    cout<<"Suitability : Not Suitable"<<endl;
                }
            }
        }objname;
        int main()
        {
         int l, w, r;
        cin>>l>>w>>r;
        objname.initializeData(l, w, r);
        objname.getLength(l, w, r);
        objname.getWidth();
        objname.getRatePerSqFeet();
        objname.calculateCost();
        objname.determineSuitability();
        return 0;
        }
 **14).RBI**
 
        #include <iostream>

        #include <string.h>
        using namespace std;
        class Bank{ private:
                    char name[50];
                    char accounttype[50];
                    int acc;
                    double balance;
                    public:
                    void initial()
                    { std::cin>>name>>acc>>accounttype>>balance; }
                        void deposit()
                    { float deposit;
                    cin>>deposit;
                    balance+=deposit; }
                    void withdraw() { float withdraw;
                                    cin>>withdraw;
                                            if(withdraw>balance){ cout<<"Insufficient amount\n";}
                                            else balance-=withdraw; }
                    void disp() { cout<<"NAME="<<name<<"\nACCNO="<<acc<<"\nTYPE="<<accounttype<<"\nBALANCEAMOUNT="<<balance<<endl; }
                    };

            int main(){float deposit,withdraw;
                    Bank obj;
                    obj.initial();
                    obj.deposit();
                    obj.withdraw();
                    obj.disp();
                    return 0;
                    }
**15).Lomda**

        #include <iostream>
        using namespace std;
        class partner
        {
        public:
            void findpartner()
            {
                int n = 0, s = 0, i = 0;
                cin >> n;
                    if (1 <= n && n <= 8)
                    {
                        int arr[n];
                        for (i = 0; i < n; i++)
                        {
                            cin >> arr[i];
                            if (arr[i] <= 8)
                            {
                                if (arr[i] == 1)
                                    cout << "4LB\n";
                                else if (arr[i] == 5)
                                        cout << "2MB\n";
                                else if (arr[i] == 3)
                                        cout << "6UB\n";
                                else if (arr[i] == 2)
                                        cout << "5MB\n";
                                else if (arr[i] == 4)
                                        cout << "1LB\n";
                                else if (arr[i] == 6)
                                        cout << "3UB\n";
                                    }
                        }
                }
            }
            };
            int main()
            {
                partner objname;
                objname.findpartner();

                return 0;
            }
   **16).Inner and Outer**
   
        #include <iostream>
        using namespace std;

        class outer
        {
            public:
            int x;
            void get()
            {
                cin>>x;
            }
 
            class inner
            {
                private:
                int y;
                public:
                void get()
                {
                    cin>>y;
                 }
                void sum()
                {
                    outer k;
                    k.get();
                    cout<<k.x+y;
                }
            };
        };
            main()
            {
                outer::inner b;
                b.get();
                b.sum();
       
 
                }
        
