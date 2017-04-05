# lambda表达式

- lambda表达式可以用在简单的函数上。

> 普通函数

```python
def f1():
    return 1
r1 = f1()
print(r1)
```

> lambda表达式

```python
f2 = lambda : 2
r2 = f2()
print(r2)
```

> 有参函数

```python
def f3(a1, a2):
    return a1 + a2
r3 = f3(10, 10)
print(r3)
```

> lambda表达式

```python
f4 = lambda a1, a2 : a1 + a2
r4 = f4(10, 10)
print(r4)
```