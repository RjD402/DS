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
