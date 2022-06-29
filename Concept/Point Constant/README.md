# Constant Pointer

<ul>
    <li>const int *p</li>
    <li>int const *p</li>
    <li>int *const p</li>
    <li>const int *const p</li>
</ul>


       
## const int *p

const 修試int *p為常量,所以*p為const,但是p可以改變            
            
```c++
    const int  a= 42;
    const int *p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    cout << *p << endl;
```
            
## int const *p     
   一樣const 修試*p,*p為const,但是p可以改變,所以const int * 等於 int const *
   
```c++
    const int  a= 42;
    int const*p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    *p = 3; //not allow
    cout << *p << endl;
    return 0;
```