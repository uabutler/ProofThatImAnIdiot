#include <iostream>
#include <string>
using namespace std;
int main()
{
  int node = 1;
  int height = -1;

  string t = "\t\t\t\\node (";
  cout << t << "0) at (0,0) {$(\\{a,b,c\\},a)$};" << endl;
  
  for(char i = 'b'; i <= 'c'; i++)
  {
    cout << t << node << ") at (0," << height << ") {$(\\{a,b,c\\}," << i << ")$};" << endl;
    height--; node++;
  }

  for(char i = 'a'; i <= 'c'; i++)
  {
    for(char j = 'a'; j <= 'c'; j++)
    {
      cout << t << node << ") at (" << (-2)*(j - 'b') << "," << height << ") {$(\\{";
      string tmp = "";
      for(char k = 'a'; k <= 'c'; k++)
      {
        if(j != k)
        {
          tmp += k;
          tmp += ",";
        }
      }
      cout << tmp.substr(0, tmp.length() - 1) << "\\}," << i << ")$};" << endl;
      node++;
    }
    height--;
  }

  height--;

  for(char i = 'a'; i <= 'c'; i++)
  {
    for(char j = 'a'; j <= 'c'; j++)
    {
      cout << t << node << ") at (" << 2*(j - 'b') << "," << height << ") {$(\\{";
      cout << j << "\\}," << i << ")$};" << endl;
      node++;
    }
    height--;
  }

  for(char i = 'a'; i <= 'c'; i++)
  {
    cout << t << node << ") at (0," << height << ") {$(\\varnothing," << i << ")$};" << endl;
    height--; node++;
  }
}
