# Exp-9
## Aim -
To study and implement pointers basics in c++

## Theory -
Pointer is a variable that holds the memory address of another variable.<br>
Pointers are crucial for dynamic memory management, working with arrays, and efficient handling of large data structures.

### 1. *Declaring a Pointer*
A pointer is declared by specifying the type of the data it points to, followed by an asterisk (*), and then the pointer variable name.

```
int* ptr;   // Pointer to an integer
char* cptr; // Pointer to a character
```

### 2. *Pointer Initialization*
To store the address of a variable in a pointer, use the address-of operator (&).

```
int x = 5;
int* ptr = &x; // ptr stores the address of x
```

### 3. *Dereferencing a Pointer*
To access the value at the memory location a pointer points to, use the dereference operator (*).

```
int x = 5;
int* ptr = &x;
cout << *ptr; // Output: 5 (value at the address stored in ptr)
```

### 4. *Pointer Arithmetic*
Pointers can be incremented or decremented to traverse memory locations. Pointer arithmetic depends on the data type the pointer is pointing to.

```
int arr[] = {1, 2, 3, 4};
int* ptr = arr;

ptr++;  // Moves to the next element in the array (because it's int*, it moves 4 bytes ahead)
```

### 5. *Dynamic Memory Allocation*
Pointers are essential when working with dynamic memory allocation using new and delete.

```
int* ptr = new int; // Allocates memory for an integer
*ptr = 5;          // Assigns value
delete ptr;        // Deallocates memory
```
## Code - 
*A*
```
#include <iostream>

using namespace std;

int main() {
    int *ptr, b = 10;
    ptr = &b;
    cout << *ptr << " " << b << endl << ptr << "  " << &b << endl;
    ptr++;
    cout << "After increment: " << ptr << endl;

    float *n, a = 189.99;
    n = &a;
    cout << endl << *n << "  " << a << endl << n << "  " << &a << endl;
    n++;
    cout << "After increment: " << n << endl;

    char *ch, c(10);
    c = '#';
    ch = &c;
    cout << endl << (void*)ch << " " << endl;
    ch++;
    cout << "After increment: " << (void*)ch << endl;
}
```
*B*
```
#include <iostream>
using namespace std;

int main(){
    int a=10;
    int * aptr=&a;

    cout<<*aptr<<endl;
    *aptr = 20;
    cout<<a<<endl;

    int arr[] = {10, 20, 30};
    cout<<*arr<<endl;

    return 0;
}
```
## Output - 
A. ![Screenshot 2024-08-27 142346](https://github.com/user-attachments/assets/b3a06cad-58c1-4154-9f54-6a37ead99d05)
B. ![Screenshot 2024-08-27 142417](https://github.com/user-attachments/assets/26d1b960-c218-4b80-9edf-fbff299d8a44)
## Conclusion - 
Pointers are symbolic representations of addresses. They enable programs to simulate call-by-reference as well as to create 
and manipulate dynamic data structures. 
Iterating over elements in arrays or other data structures is one of the main use of pointers. 
