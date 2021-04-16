### one's and two's compliment of a number
1’s complement of a binary number is another binary number obtained by toggling all bits in it, i.e., transforming the 0 bit to 1 and the 1 bit to 0
```
1's complement of "0111" is "1000"
1's complement of "1100" is  "0011"
```
2’s complement of a binary number is 1 added to the 1’s complement of the binary number. 
```
2's complement of "0111" is  "1001"
2's complement of "1100" is  "0100"
 2s complement of 100100 is 011100
```
Trick to get the 2s compliment of any binary number.  
Start traversing from the rightmost bit to left (keeping the bits as they are) till you find the first set bit. Keep this set bit as it is and now flip all the bits to the left of this bit.

### Bitwise left shift
```
 num = num << i;    //multiplication  by pow(2,i)
```
1 << 1 = 2 = pow(2,1) = (00010)  
1 << 2 = 4 = pow(2,2) = (00100)  
1 << 3 = 8 = pow(2,3) = (01000)  
1 << 4 = 16 = pow(2,4) = (10000)

### Bitwise right shift
```
      num = num >> i;  //division by pow(2,i)
```
4 >> 1 = 4/pow(2,1) = 2  
6 >> 1 = 6/pow(2,1) = 3  
5 >> 1 = 5/pow(2,1) = 2  
16 >> 4 = 16/pow(2,4) = 1

The left shift and right shift operators should not be used for negative numbers.
Time complexity for both left and right shift is O(1)
### XOR

XOR of a number with 0 results in the number itself

XOR of any bit with zero keeps the value of the bit same

XOR of any bit with one toggles the value of that bit

example:

```

1^0 = 1

0^0 = 0

1^1 = 0

0^1 = 1

```

XOR is associative i.e.

```

x^y^z = (x^y)^z = x^(y^z)

```

XOR is also commutative

```

x^y = y^z

```

#### Finding the rightmost set bit in a number

```

METHOD 1

//the number whose rmsb you need to find

int num = 5;

int rmsb = num & -n;

cout<<rmsb<<endl;

METHOD 2

//the number whose rmsb you need to find

int num = 5;

//the rmsb

int rmsb = 1;

while((num&rmsb)==0){

rmsb = rmsb<<1;

}

cout<<rmsb<<endl;

```

#### finding the position of the rightmost set bit

```

int num = 16;

int position = log2(num & -num) +1;

cout<<position<<endl;

```
#### BIT questions
1. Toggle the kth bit of a number - use xor
2. check if a number is even or odd - check the rightmost(0th) bit is set or not
3. swap two numbers - https://www.geeksforgeeks.org/swap-two-numbers-without-using-temporary-variable/
4. check if the ith bit is set or not - https://www.geeksforgeeks.org/check-whether-k-th-bit-set-not/
5. switch off the ith bit of a number - https://www.geeksforgeeks.org/how-to-turn-off-a-particular-bit-in-a-number/
6. turn on kth bit - https://www.geeksforgeeks.org/turn-particular-bit-number-2/
7. check if a number is power of 2 - https://www.geeksforgeeks.org/program-to-find-whether-a-no-is-power-of-two/
8. Upper case letter to lower case letter and vice versa- https://www.geeksforgeeks.org/toggle-case-string-using-bitwise-operators/#:~:text=The%20integer%20with%206th%20LSB,lower%20case%20and%20vice%20versa.

#### USEFUL LINKS

[bit tricks](https://leetcode.com/problems/sum-of-two-integers/discuss/84278/A-summary%3A-how-to-use-bit-manipulation-to-solve-problems-easily-and-efficiently)
