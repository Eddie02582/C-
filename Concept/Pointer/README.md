# Pointer

用來儲存記憶體位置的



## Simple

```c++
    int ival = 1024;
    int *p1 = &ival;
```
int *p1 宣告p1是指標變數,其值為ival的address<br>
所以說 *p1即是在ival的address取値


<table>
    <thead>
        <tr>
            <th>variable</th>
            <th>value</th>
            <th>address</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>ival</th>
            <th>1024</th>
            <th>Address ival</th>
        </tr>
         <tr>
            <th>p1</th>            
            <th>Address ival</th>
            <th>Address of p1</th>
        </tr>
         <tr>
            <th>*p1</th>            
            <th>1024</th>
            <th>Address ival</th>
        </tr>  
    </tbody> 
</table>

## twp pointer
```c++
    int ival = 1024;
    int *p1 = &ival;
    int **p2 = &p1;
    cout<< "ival   Value:" << ival  << endl;
    cout<< "ival Address:" << &ival  << endl;
    cout<< endl;
    cout<< "p1     Value:" << p1  << endl;
    cout<< "p1   Address:" << &p1  << endl;
    
    cout<< "*p1    Value:" << *p1  << endl;
    cout<< "*p1  Address:" << &*p1  << endl;
    cout<< endl;
    cout<< "p2     Value:" << p2  << endl;
    cout<< "p2   Address:" << &p2  << endl;
    
    cout<< "*p2    Value:" << *p2  << endl;
    cout<< "*p2  Address:" << &*p2  << endl;  
    
    cout<< "**p2   Value:" << **p2  << endl;
    cout<< "**p2 Address:" << &**p2  << endl; 
```

p2 為p1的位置 => *p2 其實就是 p1<br>
*p1 就是 ival     =>**p2 就是 ival<br>



<table>
    <thead>
        <tr>
            <th>variable</th>
            <th>value</th>
            <th>address</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>ival</th>
            <th>1024</th>
            <th>0x7ffc139c92e4</th>
        </tr>
         <tr>
            <th>p1</th>            
            <th>0x7ffc139c92e4</th>
            <th>0x7ffc139c92e8</th>
        </tr>
         <tr>
            <th>*p1</th>            
            <th>1024</th>
            <th>0x7ffc139c92e4</th>
        </tr> 
         <tr>
            <th>p2</th>            
            <th>0x7ffc139c92e8</th>
            <th>0x7ffc139c92f0</th>
        </tr>  
         <tr>
            <th>*p2</th>            
            <th>0x7ffc139c92e4</th>
            <th>0x7ffc139c92e8</th>
        </tr>  
         <tr>
            <th>**p2</th>            
            <th>1024</th>
            <th>0x7ffc139c92e4</th>
        </tr>        
    </tbody> 
</table>

## *&arr[0] vs *&arr

&arr[0]是一個指標指向arr[0],*&arr[0] = arr[0]<br>
&arr是一個指標指向arr ,arr 跟&arr 都是儲存&arr[0]位置,*&arr = arr = &arr 

























