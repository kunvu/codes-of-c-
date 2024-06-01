
#include <iostream>
using namespace std;
class demo
{ int feet,inch;
  public:
  demo(int f,int i)
  { feet=f;
    inch=i;
  }
  friend int operator >(demo &obj,demo &k);
};
  int operator >(demo & obj,demo & k)
  { 
    if(obj.feet>k.feet || obj.inch>k.inch)
     return 1;
    else
    return 0;
  }
int main()
{ demo d1(10,7);
  demo d2(1,8);
  if(d1>d2)
  cout<<"d1 is greater than d2";
  else
  cout<<"d2 is greater than d1";
  return 0;
}
