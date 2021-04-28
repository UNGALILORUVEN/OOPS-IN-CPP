**1).IOST1**

    #include<iostream>
    #include<string>
    #include<sstream>
    using namespace std;

    int main() {
    string a;
    getline(cin,a,':');
    float f;
    cin >> f;
    stringstream my_stream(ios::in|ios::out);
    my_stream << a;
    my_stream.seekg(-7,ios::end);
    std::string dat(a);
    cout << "I have a double : " << f*f;
    return 0;
    }
**2).IOST2**

    #include <iostream>

    #include <iomanip>
    using namespace std;
    int main() {
       int n;
      cin>>n;
      cout<<"0123456789"<<endl;
      cout<<setw(10)<<n<<endl;
      cout<<setw(10)<<setfill('0')<<n<<endl;
    cout<<setw(10)<<setfill('.')<<n<<endl;
    return 0;
    }
**3).IOST3**

    #include <iostream>
    using namespace std; 
    int main () { 
    long int a,b;
    cin>>a;
    cin>>std::hex>>b;
    cout<<"You have entered integer: "<<a<<"\n";
    cout<<"Equivalent value of given hexadecimal number is: "<<b<<endl;
    return 0; 
    }
 **4).IOST4**
 
      #include <iostream>
      #include <bits/stdc++.h>
      using namespace std;
      int main() {
      char x[500];
      cin.get(x,30);
      for(int i=0;x[i]!='\0';i++)
      {
        if (cin.peek()=='#')
        cin.ignore();
        else if (x[i]!='#')
        cout<<x[i];
        }
        return 0;

        }
 **5).IOST5**
 
 
    #include <iostream>
    using namespace std;
    int main()
    {
    char a[100];
    cin.get(a,100);
    int x=0;
    for(int i=0;a[i]!='\0';i++)
    {
      if(a[i]=='s')
      {
        cout<<"sS";
      }
      else
      {
          cout<<a[i];
      }
      }
      if(x==1)
      {
          cout<<"std::cin.putback('S')";
          cout<<"cout.put";
      }
      return 0;
      }
**6).IOST6**


    #include <iostream>
    using namespace std;
    int main()
    {
    char str[50];
    std::cin.getline(str,50);
    std::cout<<"the number of characters extracted are:"<<std::cin.gcount();
    return 0;
    }
**7).IOST7**


    #include<iostream>
    using namespace std;
    int main()
    {
        char ch;
        while ( cin.get(ch) )
        {
            if (ch == ' ')
              cin.putback('.');
           else
              cout << ch;
          while (cin.peek() == '#')
              cin.ignore(1,'#');
       }
        return 0;
    }
 **8).IOST 8**
 
 
    #include <iostream>
    using namespace std;

    class demo {
    public:
    int dx, dy;

    friend void operator >>(demo& d, istream& mycin)
    {
    mycin >> d.dx >> d.dy;
    }
    };

    int main()
    {
      demo d;
      operator >> (d,cin);
        cout << "dx=" << d.dx << " dy="<< d.dy;
    }
**9).IOST9**


    #include <iostream>
    #include <string.h>
    using namespace std;
    int main() {
    char a[500],b;
      cin.getline(a,30);
       b=strlen(a);
            cout<<"Your string is :";
            cout.write(a,b);
            cout<<endl;
            cout.write(a,10);
            cout<<endl;
            cout.write(a,b);
        return 0;
      }
**10).IOST10**


      #include <iostream>
      #include<string.h>
      using namespace std;
      int main() {
      char x[100];
      int a,j;
      // scanf("%[^\n]s",x);
      //int k=;
      cin.getline(x,30);
      cout<<"Your string is :";
      puts(x);
      // cout.write(x,10);
      for(a=0;a<=strlen(x);a++)
      {
        for(j=0;j<a;j++)
        {
        printf("%c",x[j]);
        cout.write(x,0);
        }
        cout<<endl;
      }
      return 0;
    }
**11).IOST11**


    #include <iostream>
    #include <stdio.h>
    using namespace std;
    int main() {
    int t=2;
    while(t)
    { char b[100];
    int i=0;
    cin.getline(b,30);
    cout.write(b,5);
    cout<<endl;
    t–;
    }
    return 0;
    }

**13).IOST13**


    #include <iostream>
    #include <string.h>
    using namespace std;
    int main() {
      int c,d;
    char a[100],b[100];
      cin>>a;
      cout.width(20);cout.fill('*');
        cout<<a<<endl;

      cin>>b;
      cout.width(20);cout.fill('-');
        cout<<b<<endl<<endl<<"WEL DONE";//cout.fill,cout.width(20)
      return 0;
    }
**14).IOST14**


    #include <iostream>
    using namespace std;

    int main()
    {
      float n;
      float pi;
      cin >> n;
      int i = 0;
      int n1 = n;
      while (n > 0)
      {
        pi=(float)22/7;
        cout.precision(n);
        cout << pi;
        while (i)
        {
          cout << '*';
          i–;
        }
      i = n1 – n + 1;
      n–;
      cout << endl;
    }
    cout << "3" << endl
    << "Fill Setting:*";

    return 0;
    }
    void d()
    {
      cout.fill('a');
      cout.width(10);
    }
**15).IOST15**


**16).IOST16**


    #include <iostream>
    using namespace std;
    int main() {
    int a;
    double b=22/7;
    cin>>a;
    cout.fill('*');
    cout.setf(ios::internal,ios::floatfield);
    cout.setf(ios::internal,ios::scientific);
    cout.width(a);
    cout<<"3.141000e+00";

    return 0;
    }
**17).IOST17**


    #include <iostream>
    using namespace std; 
    int main () { 
      long int a;
        cin>>a;
        cout.setf(ios::hex,ios::basefield );
        cout<<"Hexadecimal is:" <<hex<<a<<"\n";
        cout.setf(ios::oct,ios::basefield );
        cout<<"Octal is:"<<oct<<a<<"\n";
        cout.setf(ios::dec,ios::basefield );
        cout<<"Decimal is:"<<dec<<a;
        return 0; 
    } 
**18).IOST18**


    #include <iostream>
    #include <iomanip>
    using namespace std; 
    int main () { 
      double a,b;
      int c,d;
        cin>>a>>b>>c>>d;
        cout.setf(ios::showpos);
        cout<<"SHOWPOS : "<<showpos<<a<<"\n";
        cout.setf(ios::showpoint);
        cout<<"Showpoint : "<<setprecision(6)<<showpoint<<b<<"\n";
        cout.setf(ios::hex);
        cout<<hex<<"Hexadecimal is : " <<c<<"\n";
        cout.setf(ios::uppercase);
        cout<<"UPPER CASE : "<<uppercase<<d;
        return 0; 
    }
**19).IOST19**


    #include<iostream>
    using namespace std;
    int main()
    {
      int n,i,c=1;
      long double ans,s=1;
        cin>>n;
      for(i=1;i<=n;i++)
      {
        ans=s*c;
        cout.width(n);
        cout.setf(ios::fixed);
        cout.precision(0);
        cout<<ans<<"\n";
        s=ans;
      c++;
      }
    return 0;
  }
  
