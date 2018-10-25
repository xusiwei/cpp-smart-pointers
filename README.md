<!-- $theme: gaia -->

# C++ Smart Pointers

## by Siwei Xu

---

## Topics

* C/C++的动态内存管理
* C++标准库的智能指针
* Android工具库的智能指针

---

## C/C++的动态内存管理

* malloc/free
	* malloc/realloc/calloc, etc...
	* `<stdlib.h>`, `libc.so`
* new/delete
* new[]/delete[]

---

## malloc/free

```c++
int* buffer = (int*)malloc(count * sizeof(int));

do_sth(buffer); // ...

free(buffer);
```

--- 

## new[]/delete[]

```
int* buffer = new int[count];

// ...

delete [] buffer;
```

---

## new/delete

```
Node* p = new Node();

// ...

delete p;
```

---

## 痛点：

### 容易引发内存泄漏问题!


---

## C++标准库的智能指针

`<memory>`
* auto_ptr
* unique_ptr
* shared_ptr
	* enable_shared_from_this
* weak_ptr

---

* auto_ptr
	* C++98 自动释放
* unique_ptr
	* C++11 独占“所有权” 替代auto_ptr
* shared_ptr
	* C++11 共有“所有权” 引用计数
* weak_ptr
	* C++11 没有“所有权” 可以“提升”
	* “提升”失败：被指物（pointee）已被释放

---




---

## Android工具库的智能指针



---




