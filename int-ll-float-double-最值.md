# int-ll-float-double-最值

```
4 8 4 8
int 类型能存储的最大值和最小值
INT_MAX = 2147483647
INT_MIN = -2147483648
long 类型能存储的最大值和最小值
LONG_MAX = 9223372036854775807
LONG_MIN = -9223372036854775808
float 类型能存储的最大值和最小值
FLT_MAX = 3.40282e+38
FLT_MIN = 1.17549e-38
double 类型能存储的最大值和最小值
DBL_MAX = 1.79769e+308
DBL_MIN = 2.22507e-308
```

```c++
/*
 coder: ACboy
 date: 2010-3-1
 */

#include <iostream>
#include <float.h>
#include <limits.h>
using namespace std;

int main()
{
    cout << sizeof(int) <<" " << sizeof(long) <<" " << sizeof(float) <<" " << sizeof(double) << endl;
    cout << "int 类型能存储的最大值和最小值" << endl;
    cout << "INT_MAX = " << INT_MAX << endl;
    cout << "INT_MIN = " << INT_MIN << endl;
    cout << "long 类型能存储的最大值和最小值" << endl;
    cout << "LONG_MAX = " << LONG_MAX << endl;
    cout << "LONG_MIN = " << LONG_MIN << endl;
    cout << "float 类型能存储的最大值和最小值" << endl;
    cout << "FLT_MAX = " << FLT_MAX << endl;
    cout << "FLT_MIN = " << FLT_MIN << endl;
    cout << "double 类型能存储的最大值和最小值" << endl;
    cout << "DBL_MAX = " << DBL_MAX << endl;
    cout << "DBL_MIN = " << DBL_MIN << endl;
    return 0;
}
```

[int float double 最大值，最小值及内存分布](https://blog.csdn.net/sunny04/article/details/46793665)