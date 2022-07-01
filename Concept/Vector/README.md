# Vector



## Initialize
<table>
    <thead>
        <tr>
            <th></th>
            <th>describe</th>        
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>vector<T> v1</th>
            <th>create empty vector</th>        
        </tr>     
        <tr>
            <th>vector<T> v2 = {a,b,c}</th>
            <th>create vector with initializers elements</th>        
        </tr> 
            <th>vector<T> v3 {a,b,c}</th>
            <th>equivalent vector<T> v3 = {a,b,c}</th>        
        </tr>  
        </tr> 
            <th>vector<T> v4 (n,val)</th>
            <th>has elements with value val </th>        
        </tr>  
        </tr> 
            <th>vector<T> v5 (v2)</th>
            <th>copy v2 element to v4</th>        
        </tr> 
        </tr> 
            <th>vector<T> v6 = v2</th>
            <th>vector<T> v5 (v2)</th>        
        </tr>        
    </tbody> 
</table>

```c++
    vector<int> v1;
    vector<int> v2 {1,2,3,4,5};
    vector<int> v3 ={1,2,3,4,5};
    vector<int> v4(10,0);
    vector<int> v5(v2);
    vector<int> v6 = v2;
```

## operator +

### Adding Two strings

```c++
    string s1 = "hello", s2 = "world"; 
    string s3 = s1 + s2;
    s1 += s2;  
    string s5 = s1.append(s2);     // use append add string
```
 
### Adding Literals and strings 
When we mix strings and string or character literals, at least one operand to each + operator must be a string type
,以下範例s5,s6為錯誤

```c++
    string s1 = "hello", s2 = "world"; 
    string s3 = s1 + ", " + s2 + '\n';
    string s4 = s1 + ", ";     
    string s5 = "hello" + ", ";        // error: no string operand  
    string s6 = s1 + ", " + "world";
    string s7 = "hello" + ", " + s2;   // error: can't add string literals    
    string s8 = s1.append("123");     // use append add string
```
可以將s5修改為
```c++
    string s5 = string("hello") + ", ";// ok:adding a string and a literal
    string s5 = "hello" + string(", ");// ok:adding a string and a literal
```
將s7修改為
```c++
    string s9 = "hello" + (", " + s2); //adding a literal and a string 
```






