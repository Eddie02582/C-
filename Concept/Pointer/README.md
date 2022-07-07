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
&arr是一個指標指向arr ,arr 表示陣列arr[0]的位置,&arr表示整個陣列的位置

### sizeof
```c++
int arr[5] = {1,2,3,4};
cout << sizeof(arr) <<endl; //20 (4*5)
cout << sizeof(&arr) <<endl; //8
```
### &

```c++
int arr[5] = {1,2,3,4};
cout << arr + 1 <<endl;
cout << &arr + 1 <<endl; //equal(arr + 4) + 1
cout << (arr + 4) + 1<<endl;
```



## (*p)[n] vs *p[n]

### (*p)[n]
pointer to an array of ten ints,所以n必須跟arr個數一樣,p是存整個arr位置(&arr),即p = &arr,*p = arr,操作就跟array 一樣

```c++
int arr[5] = {5,4,3,2,1};
int (*p)[5] = &arr; 

//get address 

cout << *p  <<endl;      //arr   
cout << *p + 1 <<endl;   //arr + 1

cout << p[0] <<endl;    //&arr[0](&*p[0])
cout << p[1] <<endl;    //&arr[1](&*p[1])

//get value

cout << (*p)[0] <<endl;    //arr[0]
cout << (*p)[1] <<endl;    //arr[1]

cout << **p <<endl;          //*arr
cout << *(*p + 1) <<endl;    //*(arr + 1)

return 0;

```

### *p[n] 

*p[n]就是有n個指標的陣列

```c++
    int arr[5] = {1,2,3,4,5};
    int *p [5] ; //5 pointers
    p[0] = arr;
    p[1] = arr + 1;
    p[2] = &arr[3];
    cout << *p[0] <<endl;   //arr[0]
    cout << *p[1] <<endl;  //*(arr + 1)*/
    cout << *p[2] <<endl; //arr[3]
```












