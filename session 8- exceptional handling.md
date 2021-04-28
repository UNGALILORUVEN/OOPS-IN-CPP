**1.)CALCULATION** 

    #include <iostream>
    #include <math.h>
    using namespace std;
    int main()
    {
    //int a,b,c;
        //cin>>a>>b>>c;
 
        float p,r,n;

    try
        {   
            cin>>p>>r>>n;
            if(cin)
            {
            float amt = p * pow((1+(r/100)),n);
            cout<<"Compound Interest is:"<<amt-p;
            }
       
            else
                {
                throw p;
                }
            }
            catch(float n)
            {
             cout<<"Invalid input. Try again";
            }
        return 0;
        }
**2).Divide by zero exception**

    #include <iostream>

    #include <ctype.h>
    using namespace std;
    int main() {
    int a,b=244;
     cin>>a>>b;
     try
     {
        if( b!=0 && b!=244)
         cout<<"VALID";
   
 
        else
           throw(b);
    }
    catch(int e)
    {
       cout<<"INVALID: Exception: 0";
    }
    return 0;
    }
**3).Checking Valid Data**

    #include <iostream>

    #include <math.h>
    using namespace std;
    int main()
    {
       int a;
      try
       { 
          cin>>a;
          if(cin)
          {
           if (a>0 && a<=100)
          {
           cout<<"Valid Mark";
          }
          else
         {
         cout<<"Invalid Mark";
       }
        }
     
       else
        {
     throw a;
        }
    }
     catch(int a)
      {
         cout<<"Invalid input. Try again";
      }
     return 0;
     }
**4).User defined Exception - Division**

        #include <iostream>
        #include <exception>
        using namespace std;
        class Divide_By_Zero_Exception : public exception
        {
            public:
            const char * what() const throw() {
                return "Divide By Zero Exception";}
        };
        int main()
        {
  
        try
        {
            int a, b;
            cin>>a>>b;
            if(b==0)
            {
                Divide_By_Zero_Exception d;
                throw d;
            }
            else
            {
                cout<<a/b;
            }
        }
        catch(exception& e)
        {
            cout<<e.what();
        }
        return 0;
        }
**5). Multiple Exception - Default Exception**

        #include <iostream>
        using namespace std;
        int main() {
            int N;
            cin>>N;
            try
            {
                if (N==1)
                    cout<<"Integer Exception\nException number=25";
                else if(N==2)
                    cout<<"Float Exception\nException number=25.23";
                else
                    throw(N);
            }
        catch(...)
        {
                cout<<"Default Exception\nWrong Number Used, Input 1 or 2";
        }
        return 0;
        }
 **6).Vowels - Consonants Exceptional Handling**
 
        #include <iostream>
        #include <string.h>
        using namespace std;
        int main() {
            char a[30];
            int len, i, vow=0, cons=0;
                cin>>a;
                len = strlen(a);
                for(i=0; i<len; i++)
                {
                    try
                    {
                        if(a[i]>=65 && a[i] <91 || a[i]>=97 && a[i] < 123)
                         {
                                if(a[i] == 'a' || a[i] == 'e' || a[i] == 'i' || a[i] == 'o' || a[i] == 'u' || a[i] =='A' || a[i] == 'E' || a[i] == 'I' || a[i] == 'O' || a[i] == 'U')
                                {
                                    vow++;
                                }
                                else
                                     cons++;
                                }
                     else
                     {
                            throw a[i];
                     }
                }
   
            catch(char c)
            {
                cout<<"Exception Caught Numeric Value";
                 return 0;
            }
            }

                cout<<"Vowels="<<vow;
                 cout<<endl<<"Consonants="<<cons;

            return 0;
        }
**7).Factorial**

        #include<iostream>
        using namespace std;
        int main()
        {
            int n,i,f=1;
            cin>>n;
            try
            {
                if(n>0&&n<20)
                {
                    for(i=1;i<n+1;i++)
                    f=f*i;
                    cout<<"Factorial of a given Number is= "<<f;
                }
                else if(n<0)
                    throw (0);
                    if(n>20)
                    throw(1.0);
                }
            catch(int i)
            {
                    cout<<"Factorial of a given Number is= "<<i;
             }
            return 0;
            }
 **8).Exceptional - Operator Checking**
 
        #include <iostream>
        using namespace std;
        int main() {
        double a,b,sum;
        char c;
        cin>>a>>c>>b;
        try
        {
            switch(c)
            {
                case '+':sum=a+b;
                    cout<<a<<c<<b<<"="<<sum;
                     break;
                 case '-':sum=a-b;
                    cout<<a<<c<<b<<"="<<sum;
                    break;
                case '/':sum=a/b;
                    cout<<a<<c<<b<<"="<<sum;
                    break;
                case '*':sum=a*b;
                    cout<<a<<c<<b<<"="<<sum;
                    break;
                default:
                    throw(c);
          }
      }
    catch(char c)
    {
            cout<<"Operation Error & is not a valid operator";
    }
    return 0;
    }
 **9).Check input**
 
        #include <iostream>
        using namespace std;

        int main()
        {
                int nr = 0; char ch;
                try
                {
                    cin >> nr;
                    if(cin)
                    {
                        cin.get(ch);
                        if(ch=='.')
                        {
                            cout << "Floting" << endl;
                        }
                        else
                        {
                             cout << "Integer" << endl;
                         }
                    }
                    else
                    {
                    throw nr;
            }
        }
        catch(int nr)
        {
                cout<<"Invalid input";
        }
        return 0;
        }
 **10).Reverse - Array Exceptions**
 
        #include <iostream>
        using namespace std;
        int main() {
        int a,b[1000],i;
        cin>>a;
        try
        {
        if(a<=20&&a>0)
        {
            for(i=0;i<a;i++)
                cin>>b[i];
            for(i=a-1;i>=0;i--)
                cout<<b[i]<<" ";
        }
        else
        {
            throw(a);
        }
        }
        catch(int e)
        {
            cout<<"Exception occurred";
        }
        return 0;
        }
**11).Finding Alphabets**

     #include <iostream>

    #include <ctype.h>
    using namespace std;
    int main() {
    char a,i;

    for(i=0;i<2;i++)
    {
        cin>>a;
         try
        {
        if(isalpha(a))
            cout<<"character "<<a<<" is alphabetic "<<endl;
        else
            throw(a);
        }
        catch(char e)
        {
             cout<<"character "<<e<<" is not alphabetic "<<endl;
        }
    }
    return 0;
    }
**12).Palindrome**

        #include <iostream>

        #include <string.h>
        using namespace std;
        int main() {
        int d=1,j=0,i;
        char a[100],b[100];
        cin>>a;
        for(i=strlen(a)-1;i>=0;i--)
        {
            b[j]=a[i];
            j++;
        }
        // cout<<a<<endl<<b;
        try
        {
        if(strcmp(a,b)==0)
            cout<<a<<" is a palindrome";
        else
            throw(d);
        }
        catch(int e)
        {
            cout<<a<<" is not a palindrome";
        }
        return 0;
    }
**13).Relational Operators - Exceptional Handling**

        #include <iostream>

        using namespace std;
        int main()
        {
            int a,b;
                 cin>>a>>b;
            try
            {
                if(a>0 && b>0)
                {
                    if(a>b)
                    {
                            cout<<a<<"<"<<b<<"=0"<<endl;
                            cout<<a<<"<="<<b<<"=0"<<endl;
                            cout<<a<<"="<<b<<"=0"<<endl;
                            cout<<a<<">"<<b<<"=1"<<endl;
                            cout<<a<<">="<<b<<"=1"<<endl;
                            cout<<a<<"!="<<b<<"=1"<<endl;
                    }
                    else if(a<b)
                    {
                            cout<<a<<"<"<<b<<"=1"<<endl;
                            cout<<a<<"<="<<b<<"=1"<<endl;
                            cout<<a<<"="<<b<<"=0"<<endl;
                            cout<<a<<">"<<b<<"=0"<<endl;
                            cout<<a<<">="<<b<<"=0"<<endl;
                            cout<<a<<"!="<<b<<"=1"<<endl;
                    }
                    else
                    {
                            cout<<a<<"<"<<b<<"=0"<<endl;
                            cout<<a<<"<="<<b<<"=1"<<endl;
                            cout<<a<<"="<<b<<"=1"<<endl;
                            cout<<a<<">"<<b<<"=0"<<endl;
                            cout<<a<<">="<<b<<"=1"<<endl;
                            cout<<a<<"!="<<b<<"=0"<<endl;
                    }
                }
                else
                throw a;
                }
                catch(...)
                {
                    cout<<"No Negative Numbers";
                }
                return 0;
                }
**14).Compare two string**

        #include<iostream>
        #include<string.h>
        using namespace std;
        int main() {
        char ch[10],ch1[10];
        cin>>ch>>ch1;
        try
        {for(int i=0;ch[i]>48&&ch[i]<57;i++)
        throw ch[i];
        for(int i=0;ch[i]>48&&ch1[i]<57;i++)
        throw ch1[i];
        if(strcmp(ch,ch1)!=0)
        cout<<ch<<" is not "<<ch1;
        else
        cout<<ch<<" is "<<ch1;
        }
        catch(char ch)
        {
            cout<<"Invalid input Try again";
        }

        return 0;
        }
**15).Number Exception**

        #include <iostream>
        using namespace std;
        int main()
        {
            float input;
            cin >> input;
            try
            {
                if (!((float(int(input)) == input) && (input != 0)))
                    throw("Invalid input");
                cout << "Number of exceptions: " << int(input / 4);
            }
            catch (const char *msg)
            {
                cout << msg << endl;
            }
            return 0;
        }
 **16).Length of string**
 
        #include <iostream>

        #include <cstring>
        using namespace std;
        int main()
        {
                string str;
                cin >> str;
                int length = str.length();
                try
                {
                        if (str.empty() || str.length() == 1)
                            throw("Invalid input");
                                cout << "Length of the string is: " << length;
                }
                catch (const char *msg)
                {   
                    cout << msg << endl;
                }
                return 0;
        }
  
