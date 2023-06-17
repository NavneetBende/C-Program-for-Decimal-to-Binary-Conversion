# C-Program-for-Decimal-to-Binary-Conversion

Program for Decimal to binary Conversion in C++
In this post, we will learn how to write a code for Decimal to Binary Conversion in C++. We will look at different ways for coding Decimal to Binary in C++.

Decimal to Binary in C++
While loop in C
Various Methods discussed
Method 1: Binary Bits stored in Array
Method 2: Using mathematical operations to generate binary equivalent.
Method 1
Decimal to Binary Conversion in C++ -2
C++ Code:
Run
#include<iostream>
using namespace std;
 
void convertBinary(int num)
{
    // creating an array to store binary equivalent
    int binaryArray[32];
 
    // using i to store binary bit at given array position
    int i = 0;
    while (num > 0) {
 
        // resultant remainder is stored at given array position
        binaryArray[i] = num % 2;
        num = num / 2;
        i++;
    }
 
    // printing binary array in reverse order
    for (int j = i - 1; j >= 0; j--)
        cout << binaryArray[j];
}
 
int main()
{
    int n = 21;
    convertBinary(n);
    return 0;
}
Output
10101
Related Pages
Octal to Decimal conversion

Hexadecimal to Decimal conversion

Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Method 2
Decimal to Binary Conversion in C++
C++ Code:
Run
#include<iostream>
using namespace std;

void convertBinary(int num)
{
    // long long used to store large binary values
    long long binary = 0;
    int rem, i = 1;
    
    while(num!=0)
    {
        rem = num % 2;
        num /= 2;
        binary += rem * i;
        
        // moving to next position ex: units -> tens
        i *= 10;
    }
    cout << binary;
}
 
int main()
{
    int decimal_num = 21;
    convertBinary(decimal_num);
    return 0;
}
Output
10101
