# bouns-task
#include <iostream>
using namespace std;
  //Question 1 in sheet.
//convert every "He" to "He or She" in given string and every "him" to "him or her" in given string and every "he" to "he or she" in given string
void convert(string &s)
{
    int i = 0;
    while (i < s.length())
    {
        if (s[i] == 'H' && s[i + 1] == 'e')
        {
            s.replace(i, 2, "He or She");
            i += 8;
        }
        else if (s[i] == 'h' && s[i + 1] == 'e')
        {
            s.replace(i, 2, "he or she");
            i += 8;
        }
        else if (s[i] == 'h' && s[i + 1] == 'i' && s[i + 2] == 'm')
        {
            s.replace(i, 3, "him or her");
            i += 10;
        }
        else
        {
            i++;
        }
    }
    cout << s << endl;
}
int main()
{
    string s;
    cout << "Enter a string: ";
    getline(cin, s);
    convert(s);
    return 0;
}
