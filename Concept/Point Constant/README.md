# Constant Pointer

<ul>
    <li>const int *p</li>
    <li>int const *p</li>
    <li>int *const p</li>
    <li>const int *const p</li>
</ul>


       
## const int *p

const �׸�int *p���`�q,�ҥH*p��const,���Op�i�H����            
            
```c++
    const int  a= 42;
    const int *p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    cout << *p << endl;
```
            
## int const *p     
   �@��const �׸�*p,*p��const,���Op�i�H����,�ҥHconst int * ���� int const *
   
```c++
    const int  a= 42;
    int const*p = &a; // we can change p; const is low-level,can not change *p 
    int b = 5;
    p = &b ;
    *p = 3; //not allow
    cout << *p << endl;
    return 0;
```