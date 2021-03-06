# minacalc-standalone
Standalone version of MinaCalc along with a C API for easy access and bindings

# How to build
MinaCalc requires C++17.

The following commands assume GCC and Linux. Adjust the commands to your platform of choice

1. Compile the source files:
    - `g++ -std=c++17 -O2 -c MinaCalc/MinaCalc.cpp API.cpp`
    - If the C API is not needed, omit API.cpp: <br/>
      `g++ -std=c++17 -O2 -c MinaCalc/MinaCalc.cpp`
2. Link the object files together into a library: `ar rcs libminacalc.a *.o`

# Example usage
```c
#include <stdio.h>
#include "API.h"

int main() {
    printf("calc version: %d\n", calc_version());
}
```

Run with `gcc -lstdc++ -lm main.c libminacalc.a && ./a.out` (or equivalent for your platform and compiler)
