# Basic C++ Programs

## 1. Program to ask the user for their name and print "Hello, [name]!"

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string name;
    cin >> name;
    cout << "Hello, " << name << "!" << endl;
    return 0;
}
```
## 2. Program to add two numbers entered by the user and print the result
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a, b;
    cin >> a >> b;
    cout << "The sum is: " << a + b << endl;
    return 0;
}
```
## 3. Program to convert temperature from Celsius to Fahrenheit
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    float celsius, fahrenheit;
    cin >> celsius;
    fahrenheit = (celsius * 9/5) + 32;
    cout << "Temperature in Fahrenheit: " << fahrenheit << endl;
    return 0;
}
```
## 4. Program to find the area of a rectangle using given width and height (input by the user)
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    float width, height;
    cin >> width >> height;
    cout << "Area of the rectangle is: " << width * height << endl;
    return 0;
}
```
## 5. Program to swap two numbers using a third variable
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a, b, temp;
    cin >> a >> b;
    
    temp = a;
    a = b;
    b = temp;
    
    cout << "After swapping: a = " << a << ", b = " << b << endl;
    return 0;
}
```
## 6. Program that checks if a number is even or odd
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int num;
    cin >> num;
    
    if (num % 2 == 0)
        cout << num << " is even." << endl;
    else
        cout << num << " is odd." << endl;
    
    return 0;
}
```
## 7. Program to check if a person is eligible to vote based on their age (input by user)
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int age;
    cin >> age;
    
    if (age >= 18)
        cout << "You are eligible to vote." << endl;
    else
        cout << "You are not eligible to vote." << endl;
    
    return 0;
}
```
## 8. Program to print the first n even numbers
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << 2 * i << " ";
    }
    cout << endl;
    return 0;
}
```
## 9. Program to calculate the sum of all numbers from 1 to n
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, sum = 0;
    cin >> n;
    
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    
    cout << "Sum of numbers from 1 to " << n << " is: " << sum << endl;
    return 0;
}
```
## 10. Function to check whether a given number is prime
```cpp

#include <bits/stdc++.h>
using namespace std;

bool isPrime(int num) {
    if (num <= 1)
        return false;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0)
            return false;
    }
    return true;
}

int main() {
    int n;
    cin >> n;

    if (isPrime(n))
        cout << n << " is a prime number." << endl;
    else
        cout << n << " is not a prime number." << endl;
    
    return 0;
}
``` 
## 11. Function to find the factorial of a number
```cpp
#include <bits/stdc++.h>
using namespace std;

int factorial(int num) {
    if (num == 0 || num == 1)
        return 1;
    return num * factorial(num - 1);
}

int main() {
    int n;
    cin >> n;
    cout << "Factorial of " << n << " is: " << factorial(n) << endl;
    return 0;
}
```

## 12. Function to find the greatest common divisor (GCD) of two numbers using the Euclidean algorithm
```cpp
#include <bits/stdc++.h>
using namespace std;

int gcd(int a, int b) {
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int a, b;
    cin >> a >> b;
    
    cout << "GCD of " << a << " and " << b << " is: " << gcd(a, b) << endl;
    return 0;
}
```
## 13. Program to determine if a number is a palindrome or not
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int num, reversed = 0, original, remainder;
    cin >> num;
    
    original = num;
    while (num != 0) {
        remainder = num % 10;
        reversed = reversed * 10 + remainder;
        num /= 10;
    }
    
    if (original == reversed)
        cout << original << " is a palindrome." << endl;
    else
        cout << original << " is not a palindrome." << endl;
    
    return 0;
}
```
## 14. Program to count how many numbers in a list are greater than a given number x
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, x, count = 0;
    cin >> n;
    
    int arr[n];
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    cout << "Enter the value of x: ";
    cin >> x;
    
    for (int i = 0; i < n; i++) {
        if (arr[i] > x) {
            count++;
        }
    }
    
    cout << "There are " << count << " numbers greater than " << x << endl;
    return 0;
}
```
## 15. Program to find the second largest element in an array
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    int arr[n];
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    int largest = arr[0], secondLargest = -1;
    
    for (int i = 1; i < n; i++) {
        if (arr[i] > largest) {
            secondLargest = largest;
            largest = arr[i];
        } else if (arr[i] > secondLargest && arr[i] != largest) {
            secondLargest = arr[i];
        }
    }
    
    if (secondLargest == -1)
        cout << "No second largest element." << endl;
    else
        cout << "The second largest element is: " << secondLargest << endl;
    
    return 0;
}
```
