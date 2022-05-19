#include <bits/stdc++.h>
using namespace std;
 
void ifComment(string line)
{
 
    if (line[0] == '/' && line[1] == '/'
        && line[2] != '/') {
 
        cout << "It is a single-line comment";
        return;
    }
 
    if (line[line.size() - 2] == '*'
        && line[line.size() - 1] == '/' && line[0] == '/' && line[1] == '*') {
 
        cout << "It is a multi-line comment";
        return;
    }
 
    cout << "It is not a comment";
}
 
int main()
{
    string line = "/*Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.*/";
    cout<<line<<"\n";
    ifComment(line);
    return 0;
}
