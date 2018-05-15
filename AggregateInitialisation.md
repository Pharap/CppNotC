# Aggregate Initialisation

## Valid C, Invalid C++

Example taken from cppreference's [aggregate initialisation page](http://en.cppreference.com/w/cpp/language/aggregate_initialization#Designated_initializers).

```cpp
struct A a = {.y = 1, .x = 2}; // valid C, invalid C++ (out of order)
int arr[3] = {[1] = 5};        // valid C, invalid C++ (array)
struct B b = {.a.x = 0};       // valid C, invalid C++ (nested)
struct A a = {.x = 1, 2};      // valid C, invalid C++ (mixed)
```
