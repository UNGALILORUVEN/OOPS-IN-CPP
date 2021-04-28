**1).Address Map**

    #include<iostream>

    #include<map>
    using namespace std;
 
    int main()
    {
      int n,key_to_deleted=3,a[100],b[100],i,j;
          cin>>n;
      map<int,int>mymap;
   
        for(i=0;i<n;i++)
        {
            cin>>a[i]>>b[i];
        }
        for(j=0;j<n;j++)
            mymap.insert({a[j],b[j]});
            cin>>key_to_deleted; 
            mymap.erase(key_to_deleted);
      map<int, int>::iterator it1 ;
        for (it1 = mymap.begin(); it1!=mymap.end();  ++it1)
            cout << it1->first << " " << it1->second << endl;
        }
**2).Play with Permutations**

    #include <iostream>

    #include <algorithm>

    int main()
    {
        std::string s;
          std::cin>>s;
        while (1)
        {  
            std::cout << s <<"\n";
            if (!std::next_permutation(s.begin(),s.end()))
            break;
        }

    return 0;
    }
**3).Vector Iterator**

    #include <iostream>

    #include <vector>
    #include <iterator>
    using namespace std;
    int main() {
    int num,n;
        cin>>n;
        vector<int>MyVector;
        for(int i=0;i<n;i++)
        {
          cin>>num;
          MyVector.push_back(num);
        }
        vector<int>::iterator ptr;
        for (ptr = MyVector.begin(); ptr < MyVector.end(); ptr++)
              cout << *ptr << " ";
        /*for(int i=0;i<n;i++)
        {
           cout<<MyVector[i]<<" ";
        }*/
        cout<<endl;
        // vector<int>::reverse_iterator;
        vector<int>::reverse_iterator ptr1;
          for (ptr1 = MyVector.rbegin(); ptr1 < MyVector.rend(); ptr1++)
              cout << *ptr1 << " ";
        /* for(int i=n-1;i>=0;i--)
        {
            cout<<MyVector[i]<<" ";
        }*/
        return 0;
      }
**4).My Pair**

    #include <iostream>
    #include <utility>
    using namespace std;
 
    int main()
    {
        pair<int,string>mypair;
        int a;string b;
            cin>>a>>b;
            mypair.first =a;
            mypair.second =b ;
 
                cout << mypair.first << " " ;
                cout << mypair.second << endl ;
 
       return 0;
    }
**5).Remove Duplicate**

        #include <iostream>

        #include <list>

        using namespace std;

        int  main() {
        list <int> m;
        int n;
        cin >> n;
        int x;
        for (int i=0; i<n; i++) {
        cin >> x;
         m.push_back(x);
        }
        m.unique();
        for (auto v:m)
        cout << v << " ";
        return 0;
        }
 **6).Balancing**
 
        #include <iostream>
        #include <stack>
        #include <cstring>
        using namespace std;
        int main() {
        string str;
        cin>>str;
        stack<char> mystack;
        int l=str.size();
        bool flag=true;
        //cout << str << "\n";
        int ref;
        for (int i=0; i<l; i++) {
        if (mystack.size()==0) {
            mystack.push(str[i]);
            continue;
        }
        ref=(int)str[i];
        if (ref>(int)mystack.top()) {
        if (ref-mystack.top() <=2) {
            mystack.pop();
        }
        else {
            cout << "NO\n";
            return 0;
         }
        }
        else {
        mystack.push(str[i]);
        }
        }
        if (mystack.size()==0) {
            cout << "YES\n";
         }
        else {
            cout << "NO\n";
        }
        return 0;
        }
**7).Programmer**

        #include <iostream>
        #include <vector>
        #include <iterator>
        using namespace std;
        //push_back()
        int main() {
            int num,n;
            cin>>n;
            vector<int> myvector;
            for(int i=0;i<n;i++)
            {
                cin>>num;
                myvector.push_back(num);
            }
            vector<int>::iterator ptr;
            for(ptr=myvector.begin(); ptr<myvector.end();ptr++)
                    cout << *ptr <<" ";
                    cout<<endl;
            vector<int>::reverse_iterator ptr1;
            for (ptr1=myvector.rbegin();ptr1<myvector.rend();ptr1++)
                    cout << *ptr1 <<" ";

            return 0;
            }
 **8).Sort Game**
 
        #include <bits/stdc++.h>


        using namespace std;

        int main() {
        int n;
        cin >> n;
        int x;
        vector<int>v;
        while(n--) {
        cin >> x;
        v.push_back(x);
        }
        sort(v.begin(), v.end());
        for (auto i:v) {
        cout << i << " ";
        }
        return 0;
        }
**9).Vector to Heap**

        #include<iostream>

        #include<algorithm>
        #include<vector>
        using namespace std;
        vector<int> myvector;

        int main()
        {
            int n,i;
            cin>>n;
            int input=0; 
            for(i=0;i<n;i++)
            {
                cin>>input;
                myvector.push_back(input);
            }
   
            make_heap(myvector.begin(), myvector.end());
     
            // Displaying the maximum element of heap
            // using front()
   
            cout << myvector.front() << endl;
     
            return 0;
        } 
**10).Play with Streams**

        #include <sstream>
        #include <vector>
        #include <iostream>
        using namespace std;

        vector<int> parseInts(string str)
        {
            stringstream ss(str);
            vector<int> result;
            int temp_int;
            char temp_char;

                    ss >> temp_int;
                    result.push_back(temp_int);
                    while (ss >> temp_char)
                    {
                        ss >> temp_int;
                        result.push_back(temp_int);
                     }
                    return result;
        }

        int main()
        {
            string str;
            cin >> str;
            vector<int> integers = parseInts(str);
            for (int i = 0; i < integers.size(); i++)
            {
                cout << integers[i] << "\n";
            }

            return 0;
        }
**11).Deque**

        #include <cstdio>
        #include <deque>
        #include <algorithm>
        #include <iostream>

        using namespace std;

        int a[1000000];
        int x[1000000], y[1000000];
        deque<int> dq2;

        int main()
        {
            int T;
                cin >> T;
                while(T--){
            dq2.clear();
                int n, k;
                scanf("%d %d", &n, &k);
  
                for (int i = 0; i < n; i++) scanf("%d", a + i);
  
                for (int i = 0; i < k - 1; i++){
   
                while (dq2.size() && a[dq2[dq2.size() - 1]] <= a[i]) dq2.pop_back();
                    dq2.push_back(i);
             }
  
            for (int i = 0, j; (j = i + k - 1) < n; i++){
            while (dq2.size() && a[dq2[dq2.size() - 1]] <= a[j]) dq2.pop_back();
            dq2.push_back(j);

            y[i] = a[dq2[0]];
            if (dq2[0] == i) dq2.pop_front();
            }
  
          for (int i = 0; i <= n - k; i++) printf("%d%c", y[i], i == n - k ? '\n' : ' ');
            }
         return (0);
 
        }
**12).Swapping two Functions**

        #include <stack>

        #include <iostream>
        #include <vector>
        #include <bits/stdc++.h>
        using namespace std; 

        int main()
        {
                // stack container declaration
                stack<int> mystack1;
                stack<int> mystack2;  
                vector<int>i;
                vector<int>j;
                    int n,k,a;
                        cin>>n;
                for(k=0;k<n;k++)
                {
                cin>>a;
                 mystack1.push(a);
         
                }
                for(k=0;k<n;k++)
                {
                     cin>>a;
                    mystack2.push(a);
                 }

                // using swap() function to swap elements of stacks
                 mystack1.swap(mystack2);
 
                // printing the first stack
                cout<<"";
                while (!mystack1.empty()) {
                    cout<<mystack1.top()<<" ";
                mystack1.pop();
            }
            reverse(i.begin(),i.end());
            reverse(j.begin(),j.end());
                // printing the second stack
            cout<<endl;
            while (!mystack2.empty()) {
                cout<<mystack2.top()<<" ";
                mystack2.pop();
        }
        return 0;
    }
  **13).Marks and Vector**
  
        #include <bits/stdc++.h> 
        using namespace std;   
        int main() 
        {
            int input;
            vector<int> myvector; 
            while (cin>>input)
                myvector.push_back(input);
               cout<<*min_element(myvector.begin(),myvector.end())<<" "<<*max_element(myvector.begin(),myvector.end()); 
                return 0; 
        }
  **14).Play with Set**
  
        #include<bits/stdc++.h>
        #include<iostream>
        #include<set>
        using namespace std;

        int main(){
        set<int>s;
        int size;
        cin >> size;
        int a = size;
        set<int>:: iterator it;
        for(int i = 0; i < size; i++){
        int b;
        cin >> b;
        s.insert(b);
        }
        int c;
        cin >> c;
        if(s.find(c) != s.end()){
        cout << "Element "<< c << " found in the set\n";
        }else{
        cout << "No Element Found\n";
        }
        for(set<int>::iterator itr = s.begin(); itr != s.end(); itr++){
        cout << *itr << " ";
        }
        cout << endl;
        cout << "Size="<< size << endl;
        return 0;
        }
**15).Remove Duplicate**

        #include <iostream>
        #include <list>

        using namespace std;

        int  main() {
            list <int> m;
            int n;
            cin >> n;
            int x;
            for (int i=0; i<n; i++) {
            cin >> x;
            m.push_back(x);
        }
        m.unique();
        for (auto v:m)
            cout << v << " ";
        return 0;
        }
**16).Sets**

        #include <iostream>
        #include <set>
        using namespace std;
        int main() {
            int n;
            set<int>s;
            cin >> n;
            while(n--){
       
                int x,y;
                cin >> y >> x;
                if(y == 1){
                        s.insert(x);
                } else if(y == 2){
                         s.erase(x);
                } else {
                        auto itr = s.find(x);
                        if(distance(itr,s.end()) == 0){
                            cout << "No" << endl;
                } else {
                            cout << "Yes" << endl;
                }
            }
        }
        return 0;
    }

