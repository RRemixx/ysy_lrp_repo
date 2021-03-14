### n-arr tree 的析构算法

```c++
Node::~Node(){
    for(int i=0;i<child_num;i++){
        children[i]->~Node();
        delete children[i];
    }
    delete[] children;
}
```

