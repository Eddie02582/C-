# Regex


## regex 宣告

```c++
    std::regex smiles_regex("[:|;](-|~)?[)|D]");
    std::regex reg2("[0-9]{3}\\w+", std::regex_constants::icase); /不區分大小寫
```

## regex_match

```c++
#include <iostream>
#include <regex>
using namespace std;
int main()
{
    string c = ":D";
    regex smiles_regex("[:|;](-|~)?[)|D]");
    if (regex_match(c, smiles_regex ))
    {
        cout << "Match";
    }    
    return 0;
}
```

getmatch
```c++
#include <iostream>
#include <regex>
using namespace std;
int main()
{
    string c = ":D";
    regex smiles_regex("[:|;](-|~)?[)|D]");
    smatch sm;
    if(regex_match(c,sm, smiles_regex ) ){
        cout << "Match!" << endl;
        for( int i = 0 ; i < sm.size() ; ++i ){
          cout << i << ": [" << sm[i] << ']' << endl;
        }
    }     
    return 0;
}
```

## regex_search

