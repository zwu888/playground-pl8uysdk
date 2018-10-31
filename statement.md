# description: 
 Jumping into a block and bypassing a declaration with an initialization is ill-formed.  In this example there are cases which would bypass the declaration and initialization of block scope x declaration.

```C++ runnable
#include <iostream>

int main() 
{ 
  int x = 3;

  switch(x)
  {
    case 0:
      int x = 1;
      std::cout << x << std::endl;
    break;
    case 3:
      std::cout << x << std::endl;
    break;
    default:
      x = 2;
      std::cout << x << std::endl;
  }

  return 0;
} 
