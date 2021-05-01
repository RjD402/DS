## Miscellaneous


```
        int res = 0;
        unordered_map<int, int> count;
        for (int a: A) {
        //what will happen first? will count[a] value be added to res then incremented or will it be first incremented then added to res
            res += count[a]++;
        }
        
        first the value of count[a] will be added to res
        then the value of count[a] be incremented

```

#### How arrays are passed to functions in C/C++


#### vector
passing by reference in another function.  
We can get the size of the vector in another funciton(doesn't matter if passed by reference of not) unlike array where we need to pass the size as well.
```
using namespace std;
void solve(vector<int> temp){
    
    cout<<temp.size()<<endl;
 
}

int main()
{
   
   vector<int> temp;
   int arr[] = {1,2,3};
   for(int i=0;i<5;i++){
       temp.push_back(i);
   }
   solve(temp);
   return 0;
}

OUTPUT
5
```

#### sorting a vector of vector containing pair
example
```
int main()
{
   vector<vector<pair<int, int>>> big;
   vector<pair<int,int>> small1,small2,small3;
   small1.push_back({1,2});
   small2.push_back({3,4});
   small3.push_back({5,6});
   
   big.push_back(small3);
   big.push_back(small1);
   big.push_back(small2);
   
   sort(big.begin(),big.end());
   
   for(auto p: big){
       for(auto q: p){
           cout<<q.first<<" "<<q.second<<endl;
       }
   }
   return 0;
}

OUTPUT
1 2
3 4
5 6
```
