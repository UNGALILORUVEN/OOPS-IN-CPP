
**1.)Professor Omkar**

            #include <iostream> 
            using namespace std;
            int main() {int water,it,ft;
                        float Q;
                        cin>>water>>it>>ft;
                        Q=water*(ft-it)*4184;
                        cout<<"The energy needed is "<<Q;
                       return 0;
            } 

**2.)SCIENTIST GAME**

            #include <iostream>
            using namespace std;

            int main()
            {
                int num, r, sum = 0, temp;
                cin >> num;
                for (temp = num; num != 0; num = num / 10) 
                        {
                    r = num % 10;
                    sum = sum + (r * r * r);
                }
                if (sum == temp)
                    cout << "Give to Scientist Armstrong" << endl;
                else
                    cout <<"Dont Give to Scientist Armstrong" << endl;
            }

**3.)Sachin and his Pills**

             #include <iostream>
            using namespace std;
            class Month{
              int days;
              public:
              Month(int,int);
              bool leapYear(int);
              int getDays();
            };
            Month::Month(int number,int year){
              if(number<8) (number%2==1)?(days=31):(days=30);
              else (number%2==0)?(days=31):(days=30);
              if(number==2){
                if(leapYear(year)==1) days=29;
                else days=28;
              }
            }
            bool Month::leapYear(int year){
              if(year%400==0) return 1;
              if(year%100==0) return 0;
              if(year%4==0) return 1;
              return 0;
            }
            int Month::getDays(){
              return days;
            }
            int pillDays(int day,int month,int year,int count=0){
              Month M(month,year);
              int monthDays = M.getDays(),i;
              for(i=day;i<=monthDays;i++) if(i%2==1)count++;
              if(monthDays%2==0){
                pillDays(1,month+1,(month==12)?(year+1):(year),count);
              }
              else return count;
            }
            int main(){
              int i,j,n,day,month,year,date[10];
              char temp[10];
              //char date[10];
              cin>>n;
              for(i=0;i<n;i++){
                cin>>temp;
                for(j=0;j<10;j++) date[j]=temp[j]-48;
                day = date[8]*10 + date[9];
                month = date[5]*10 + date[6];
                year = date[0]*1000 + date[1]*100 + date[2]*10 + date[3];
                cout << pillDays(day,month,year) << endl;
              }
              return 0;
            }

**4.)Legends of Indian Cricket**

             #include <iostream> 
            using namespace std; 
            string one[] = { "", "one ", "two ", "three ", "four ", 
                             "five ", "six ", "seven ", "eight ", 
                             "nine ", "ten ", "eleven ", "twelve ", 
                             "thirteen ", "fourteen ", "fifteen ", 
                             "sixteen ", "seventeen ", "eighteen ", 
                             "nineteen " }; 
            string ten[] = { "", "", "twenty ", "thirty ", "forty ", 
                             "fifty ", "sixty ", "seventy ", "eighty ", 
                             "ninety " }; 
            string numToWords(int n, string s) 
            {  string str = ""; 
                if (n > 19) 
                    str += ten[n / 10] + one[n % 10]; 
                else
                    str += one[n]; 
                 if (n) 
                    str += s; 
                  return str; 
            } 
            string convertToWords(long n) 
            { 
                string out; 
                out += numToWords((n / 10000000), "crore ");
                out += numToWords(((n / 100000) % 100), "lakh ");
                out += numToWords(((n / 1000) % 100), "thousand ");
                out += numToWords(((n / 100) % 10), "hundred "); 

                if (n > 100 && n % 100) 
                    out += "and "; 
                out += numToWords((n % 100), ""); 

                return out; 
            } 
            int main() 
            {   long n;
              cin>>n;
                cout << convertToWords(n) << endl; 
              return 0; 
            }

**5.)SRM Calculator**

             #include <stdio.h>
            int main()
            {
              char a;
              int b,c;
              scanf("%c",&a);
              switch (a)
              {
                case '1':
                scanf("%d %d",&b,&c);
                printf("%d",b+c);
                break;
                case '2':
                scanf("%d %d",&b,&c);
                printf("%d",b-c);
                break;
                case '3':
                scanf("%d %d",&b,&c);
                printf("%d",b*c);
                break;
                case '4':
                scanf("%d %d",&b,&c);
                printf("%d",b/c);
                break;
                default:
                  printf("Invalid Input");
              }
            return 0;
            }

**6.)You and Me**

             #include <iostream>
            using namespace std;
            int main() {
             int a,b,c;
              cin>>a;
              cin>>b;
              c=(a+b)/2;
              cout<<"I am "<<a;
              cout<<"\nYou are "<<b;
              cout<<"\nWe are around "<<c;
             return 0;
            }

**7.)COUNTRY**

             #include <stdio.h>
            int main()
            {
              int a;
              scanf("%d",&a); 
              if(a>=18 && a<=60)
                printf("Eligible");
              else
                printf("Not Eligible");

             return 0;
            }    

**8.)DHONI AND ZIVZ IN CHENNAI** 

            #include <iostream>
            using namespace std;
            int main() {
             float a;
              int b;
              cin>>b;
              a=(16.6*b)/100;
              cout<<"Your weight on moon is : "<<a;
             return 0;
            }

**9.)SWIM**

             #include <iostream>
            using namespace std;
            int main() {
             int a,b,c,s;
              cin>>a>>b;
              c=3.14*a*a;
              s=b*b;
              if(c>s)
                cout<<"I prefer centre 1";
              else
                cout<<"I prefer centre 2";
             return 0;
            }

**10.)PLAY WITH XOR**

             #include <iostream>
            using namespace std;
            int main() {
            int t;cin>>t;
              while(t--){
                int n;cin>>n;int a[n],c1=0,c0=0;
                for(int i=0;i<n;i++){
                  cin>>a[i];
                  if(a[i]==1)c1++;
                  }
                c0=n-c1;
                if(c1%2==0){
                  cout<<c0<<endl;
                  }
                if(c1%2!=0){
                  cout<<c1<<endl;
                  }
                }
             return 0;
              }
 **11).Waiting or Not Waiting**
 
            #include <iostream>
            using namespace std;
            int main() {
            int a;
            cin>>a;
            if(a>0)
                        cout<<"I am waiting";
            else
             if(a<0)
                        cout<<"I am not waiting";
            else
                        cout<<"Sorry";
 
            return 0;
            }
 **12).Print Floyd's**
 
            #include <iostream>
            using namespace std;
            int main()
            {
                        int n,k,i,j;
                        cin>>n;
                        k=1;
                        for(i=1;i<=n;i++)
                        {
                        for(j=1;j<=i;j++,k++)
                        {
                                    cout<<k;
                        }
                        cout<<endl;
            }
            //cout<<"Hello World";
            return 0;
            }
 **13).Upper case conversion**
 
            #include <iostream>
            #include <string>
            using namespace std;

            int main()
            {
                        char s[30];
                        int i;
 
                        cin>>s;
 
                        for(i=0;i<=10;i++)
                         if(s[i]>=97 && s[i]<=122)
                        {
                        s[i]=s[i]-32;
                         }
            }
            cout<<s;
            return 0;
            }
 **14).Digits in Words**
 
            #include <iostream>
            using namespace std;
            int main() {
            long int n,sum=0,r;   
 
            cin>>n;   
            while(n>0)   
            {   
            r=n%10;   
            sum=sum*10+r;   
            n=n/10;   
            }   
            n=sum;   
            while(n>0)   
            {   
            r=n%10;   
            switch(r)   
            {   
            case 1:   
            cout<<"One ";   
            break;   
            case 2:   
            cout<<"Two ";   
            break;   
            case 3:   
            cout<<"Three "; 
            break;   
            case 4:   
            cout<<"Four "; 
            break;   
            case 5:   
            cout<<"Five "; 
            break;   
            case 6:   
            cout<<"Six "; 
            break;   
            case 7: 
            cout<<"Seven "; 
            break; 
            case 8:   
            cout<<"Eight ";   
            break;   
            case 9:   
            cout<<"Nine "; 
            break;   
            case 0:   
            cout<<"Zero "; 
            break;   
            default:   
            cout<<"tttt ";   
            break;   
            }   
            n=n/10;   
            }   
 
 
             return 0;
            }
**15).Letter Pattern**

            #include <iostream>

            using namespace std;
            int main()
            {

                        int i,j,n;
                        char ch='A';
                        cin>>n;
                        for(i=1;i<=n;i++)
                        {
                                    for(j=1;j<=i;j++)
                                    {
                                     if(ch < 'Z'+1)
                                    cout<<ch++;
                                    else{
                                    ch = 'A';
                                    cout << ch++;
                                    }
                        }
                        cout<<endl;
            }
            return 0;
            }
            
++++=======================================================================++++

****PLEASE UPDATE WITH LEFT OVER CODINGS****
