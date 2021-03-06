## Math 

### Hottest topics

1. Greatest Commond Divisor (GCD)
2. Catalan Numbers
3. Prime numbers: Optimized Prime checher, Sieve of Eratosthenes: Generating List of Prime Numbers, Larghest Prime Divisor.
4. Fibonacci number(base exerices for dynamic programming).


[Math for Competitive Programming -> list created by a google competitive coder](https://www.quora.com/How-do-I-get-good-at-math-for-competitive-programming/answer/Sameer-Gulati-3?ch=10&share=e1c30b08&srid=oeMh)

### Key Concepts

* **Number theory:** branch of math that studies integers. 
A number 'a' is called factor or divisor of a number 'b' if a divides b. If a is a facotr of b, we write a|b. 
* A number n >1 is  **prime** if it only positive factors are 1 and n.
* Intersection between two sets: consists of elements that are both in A and B. 
* **Union:** consistes of elements that are in A OR in B. 
* **Complement:** Suppose to have the universal set = {1,2,3,4,5,6,7,8,9,10}, the complement A' of the set A={1,2,3,4,5}, will be {6,7,8,9,10} (The universal set without the elements of our original source set).
* **Difference:** consts of elements that are in A but not in B and elements that are in B but in A. 
* **Cartesian Product:** In mathematics, specifically set theory, the Cartesian product of two sets A and B, denoted A × B, is the set of all ordered pairs (a, b) where a is in A and b is in B.

### Fibonacci Numbers

### Some code example

An efficient way to check if a number is prie is to check all its factors from 2 to sqrt(n).
```
bool prime(int n)
{
    if (n < 2) return false;
    for(int i = 2; i*i <= n; i++)
    {
        if(n % i == o) return false; 
    }
    return true; 
}
```

### Greatest Commond Divisor (GCD) and Least Commond Multiple

Greates commond divisor: the greates commond divisor of two or more integers which are not all zero, is the larghest posiibe integer that divides each integers. For example, the gcd fo 8 and 12 is 4. 

```
int gcd(int a, int b) { return b==0 ? a : gdc(b, a%b); }
int lcm(int a, int b) {  return a * (b/gcd(a,b)); }
```

### Fibonacci Number

f(0) = 0 
f(1) = 1
f(n) = f(n-1) + f(n-2)


## Generate permutations#

A permutation is each one fo the N! possible arrengements the elementws can take (where N is the number of elements in the range). Different permutation can be ordered according to how they compare lexicographicaly to each other; 

```
#include <algorithm>    // std::next_permutation, std::sort
```

Classical problem: generate all permutations of  aset of n elements.
A = {1,2,3}  -- Permutations = [{0,1,2}, {0,2,1}, {1,0,2}, {1,2,0}, {2,0,1} , {2,1,0}].

A simple way to genera permutation is to begin with the permutation {0,1... n-1} and use a function that construct the next permutation in increasing order. 

```
#include <bits/stdc++.h> 
using namespace std; 
  
// Function to display the array 
void display(int a[], int n) 
{ 
    for (int i = 0; i < n; i++) { 
        cout << a[i] << "  "; 
    } 
    cout << endl; 
} 
  
// Function to find the permutations 
void findPermutations(int a[], int n) 
{ 
    // Sort the given array 
    sort(a, a + n); 
    // Find all possible permutations 
    cout << "Possible permutations are:\n"; 
    do { 
        display(a, n); 
    } while (next_permutation(a, a + n)); 
} 
  
// Driver code 
int main() 
{ 
  
    int a[] = { 10, 20, 30, 40 }; 
  
    int n = sizeof(a) / sizeof(a[0]); 
  
    findPermutations(a, n); 
  
    return 0; 
} 
```
##### Source Geeks for Geeks

**Pollard’s rho algorithm**: used for the calculation of factorization of large numbers. 


###### Practice

The Simpler Ones
1. UVa 10055 - Hashmat the Brave Warrior (absolute function; use long long)
2. UVa 10071 - Back to High School ... (super simple: outputs 2 × v × t)
3. UVa 10281 - Average Speed (distance = speed × time elapsed)
4. UVa 10469 - To Carry or not to Carry (super simple if you use xor)
5. UVa 10773 - Back to Intermediate ... * (several tricky cases)
6. UVa 11614 - Etruscan Warriors Never ... (find roots of a quadratic equation)
7. UVa 11723 - Numbering Road * (simple math)
8. UVa 11805 - Bafana Bafana (very simple O(1) formula exists)
9. UVa 11875 - Brick Game * (get median of a sorted input)
10. UVa 12149 - Feynman (finding the pattern; square numbers)
11. UVa 12502 - Three Families (must understand the ‘wording trick’ first)

Medium

1. UVa 00100 - The 3n + 1 problem (do as asked; note that j can be < i)
2. UVa 00371 - Ackermann Functions (similar to UVa 100)
3. UVa 00382 - Perfection * (do trial division)
4. UVa 00834 - Continued Fractions (do as asked)
5. UVa 00906 - Rational Neighbor (compute c, from d = 1 until ab < d c )
6. UVa 01225 - Digit Counting * (LA 3996, Danang07, N is small)
7. UVa 10035 - Primary Arithmetic (count the number of carry operations)
8. UVa 10346 - Peter’s Smoke * (interesting simulation problem)
9. UVa 10370 - Above Average (compute average, see how many are above it)
10. UVa 10783 - Odd Sum (input range is very small, just brute force it)
11. UVa 10879 - Code Refactoring (just use brute force)
12. UVa 11150 - Cola (similar to UVa 10346, be careful with boundary cases!)
13. UVa 11247 - Income Tax Hazard (brute force around the answer to be safe)
14. UV a 11313 - Gourmet Games (similar to UVa 10346)
15. UVa 11689 - Soda Surpler (similar to UVa 10346)
15. UVa 11877 - The Coco-Cola Store (similar to UVa 10346)
16. UVa 11934 - Magic Formula (just do plain brute-force)
17. UVa 12290 - Counting Game (no ‘-1’ in the answer)
18. UVa 12527 - Different Digits (try all, check repeated digits)