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
