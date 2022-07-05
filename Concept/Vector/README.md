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
            <th>copy v2 element to v5</th>        
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
    vector<int> v4(10,0); // equal vector<int> v4(10)
    vector<int> v5(v2);
    vector<int> v6 = v2;
```

## operator 

<a href = "https://m.cplusplus.com/reference/vector/vector/cend/">vector</a>

### insert

```c++
    vector<int> myvector (3,100); //{100,100,100}
    vector<int>::iterator it;
    
    it = myvector.begin();
    it = myvector.insert ( it , 200 );//add 200 {200,100,100,100}    
    myvector.insert (it,2,300);//add two 300 {300,300,200,100,100,100} 

    it = myvector.begin();    
    std::vector<int> anothervector (2,400);
    myvector.insert (it+2,anothervector.begin(),anothervector.end()); // 在it+2前面差入 =>{300,300,400,400,200,100,100,100}

```


## copy vector

### initial

```c++
    vector<int> vect1{1, 2, 3, 4};
    vector<int> vect2 = vect1;
    vector<int> vect3(vect1);
    vector<int> vect4(begin(vect1) ,end(vect1));
    vector<int> vect5(&vect1[0],&vect1[0] + vect1.size());
```

### normal

```c++
    vector<int> vect1{1, 2, 3, 4};
    
    vector<int> vect2 ;
    vect2 = vect1;
    
    vector<int> vect3 ;
    vect3.insert(begin(vect3),begin(vect1),end(vect1));
    
    vector<int> vect4;	
	vect4.assign(begin(vect1) ,end(vect1));    
    
```



## copy arr to vector

```c++
    int arr [] = {1,2,3};
	int n = sizeof(arr) / sizeof(arr[0]);
    
    vector<int> vect1 (arr ,arr + n);	
    
    vector<int> vect2;	
	vect2.insert(vect2.begin(),arr ,arr + n);
    
    vector<int> vect3;	
	vect3.assign(arr ,arr + n);

    vector<int> vect4;
	for (int i = 0; i < n; i++){
		v.push_back(arr[i]);
	} 
    
```




