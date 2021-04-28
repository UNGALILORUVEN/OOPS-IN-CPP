**1.)LARGEST OF LONG**

    #include <iostream>
    using namespace std;
    template <class T>
      int GetMax(T x, T y, T z)
    { 
       if(x>y)
        {
           if(x>z)
               cout<<x;
           else
               cout<<z;
        }
       else if(y>z)
           cout<<y;
       else
           cout<<z;
       return 0;
    }
    int main() {
     long a,b,c;
       cin>>a>>b>>c;
       GetMax(a,b,c);
     return 0;
    }

**2.)PRODUCT OF NUMBERS**

         #include <iostream>
         using namespace std;
         template<class T>
         T displayresult(T n1, T n2)
       {
             cout<<n1<<endl<<n2<<endl<<n1*n2; 
              return 0;
         }
            int main() {
            float a,b;
            cin>>a>>b; 
            displayresult(a,b);
            return 0;
           } 
 **3).Swap**
 
        #include<iostream>
        #include<string.h>
        using namespace std;
        template<class T>
        void Swap(T &x,T &y)
        {
            T z;
            strcpy(z,x);
            strcpy(x,y);
            strcpy(y,z);
        };
        int main() {
        char a[20],b[20];
        cin>>a>>b;
        Swap(a,b);
        cout<<a<<" "<<b;
        return 0;
        }
 **4).Adding Array**
 
        #include <iostream>
        using namespace std;
        template<class T>
        T sum(T n1, T n2, T n3, T n4, T n5)
        {
            return n1+n2+n3+n4+n5;
        }
        int main() {
        int a,b,c,d,e;
        float f,g,h,i,j;
        cin>>a>>b>>c>>d>>e>>f>>g>>h>>i>>j;
        cout<<sum(a,b,c,d,e)<<endl;
        cout<<sum(f,g,h,i,j);
        return 0;
        }
 **5).Subtraction**
 
        #include <iostream>
        using namespace std;
        template<class T>
        T displayresult(T n1, T n2)
        {
        cout<<n1<<endl<<n2<<endl<<n1-n2;
        return 0;
        }
        int main() {
        float a,b;
        cin>>a>>b;
        displayresult(a,b);
        return 0;
        }
 **6).Minimum of given elements (Banglore)**
 
    #include <iostream>
    using namespace std;
    template <class T>
        void min(T n1,T n2,T n3)
        {
            if(n1<n2)
            {
                if(n1<n3)
                    cout<<n1;
                else
                    cout<<n3;
            }
            else if(n2<n3)
                cout<<n2;
    else
        cout<<n3;
    }
    int main() {
    float a,b,c;
        cin>>a>>b>>c;
        min(a,b,c);
    return 0;
    }
 **&).Adding Numbers**
 
    #include <iostream>
    using namespace std;
    template<class T>
    T displayresult(T n1, T n2)
    {
        cout<<n1<<endl<<n2<<endl<<n1+n2;
        return 0;
    }
    int main() {
        float a,b;
         cin>>a>>b;
        displayresult(a,b);
        return 0;
    }
**9).sum of Numbers**

    #include <iostream>
    using namespace std;
    template <class T>
    T sum(T n1, T n2)
    {
        return n1+n2;
    }
        int main() {
        float a,b,c,d;
        cin>>a>>b>>c>>d;
            cout<<sum(a,b)<<endl<<sum(c,d)<<endl<<sum(a,c);
        return 0;
        }
**10).Largest Number**

    #include <iostream>
    using namespace std;
    template<class T>
    class largestno
    {
    public:
    T Large(T n1,T n2)
    {
    return (n1 > n2) ? n1 : n2;
    }
    };
    int main() {
    largestno <int> t; 
    largestno <float> u;
    int a,b;
    float c,d;
    cin>>a>>b>>c>>d;
    cout<<t.Large(a,b)<<endl<<u.Large(c,d);
    return 0;
    }
 **11).Division**
 
    #include <iostream>
    using namespace std;
    template<class T>
        T displayresult(T n1,T n2)
    {
        return n1/n2;
    }
    int main() {
    float a,b;
    cin>>a>>b;
    cout<<a<<endl<<b<<endl<<displayresult(a,b);
    return 0;
    }

