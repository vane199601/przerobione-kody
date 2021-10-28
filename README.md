#include <iostream>
#include <cstdio>

using namespace std;

int potega(int a, int b, int m);

int main()
{
    int t;
    cin >> t;
    while(t--)
    {
    int a, b, m;
    cin >> a >> b >> m;
    cout << potega(a, b, m);
    }
    return 0;
}

int potega(int a, int b, int m)
{
   a%=10000;
   if (a==0) return 0;
   if (b==0) return 1;
   int y =a;
   int r=1;
   while (b>0)
   {
       if (b%2==1) r= (r*y) % 10000;
       y=(y*y) % 10000;
       b/=2;
   }
   return r;
}


