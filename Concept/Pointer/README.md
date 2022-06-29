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
    int **p2 = &p1; //p2存的是p1指標的位置即是&p1
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












