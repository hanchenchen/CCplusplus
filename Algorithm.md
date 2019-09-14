# Algorithm

##### `#include<algorithm>`

1. `count(v.begin(),v.end(),val)`

2. `count(v.begin(),v.end(),[](int val){return true;})`

3. `min_element(v.begin(),v.end(),[](){});`

   `max_element(v.begin(),v.end(),[](){});`

4. `string s`

   `transform(s.begin(),s.end(),s.begin(),::tolower);`

   ```c++
   int main(){
       string a,b;
       cin>>a;
       
       transform(a.begin(),a.end(),b.begin(),::tolower);
       cout<<b<<endl;//空
       
       b="x";
       transform(a.begin(),a.end(),b.begin(),::tolower);
       cout<<b<<endl;//a
       
       b="xxxxx";
       transform(a.begin(),a.end(),b.begin(),::tolower);
       cout<<b<<endl;//abcxx
       
       cout<<a<<endl;//ABC
       return 0;
   }
   ```

5. 1

