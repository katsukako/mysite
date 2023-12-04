# Automate boring shit

> 其他需要学习的内容：操作系统，软件工程基础，linux，计算机网络基本知识，shell程序设计等等 [csdiy](https://csdiy.wiki/)

> 

## 实用技巧

???+ f-string

        a = 5
        b = 10
        result = f"Five plus ten is {a + b}."
        print(result)  # 输出: Five plus ten is 15.


## 1 basic

1. input只能输入str，要变成数值需要int或者float

2. input可以input("加上提示")

3. != 不等于

4. True 大写

5. %求余数；// ：整除运算符，返回两个数相除的商的整数部分；** ：幂运算符，返回一个数的另一个数次幂。

6. 赋值运算符：

`= ：赋值运算符，将右边的值赋给左边的变量。`

`+= ：加法赋值运算符，等同于 x = x + y。`

`-= ：减法赋值运算符，等同于 x = x - y。`

`*= ：乘法赋值运算符，等同于 x = x * y。`

`/= ：除法赋值运算符，等同于 x = x / y。`

`%= ：模赋值运算符，等同于 x = x % y。`

`**= ：幂赋值运算符，等同于 x = x ** y。`

`//= ：整除赋值运算符，等同于 x = x // y。`

## 2 flow control

1. if elif else elif说明不满足if条件下，else说明不满足if和elif  

2. while loop； while 条件:

3. inside loop continue break

4. 0 和空格是False

5. for loop （for in） and range() a <= x < b

6. import module, name **py文件命名避免与mod重名**； 使用时module.functionname()

7. round() abs()

## 3 functions

### keyword arguments

* 自定义function def 变量用完会被忘记

!!! warning
    def 中可以使用return 定义函数返回的值

???+ note inline end "how"

        def a():

            print('a')

            print('b')

???+ example

        def test(t):
            print(t)
            return(t) # 将t的值返回给方程
            t = input() # 从外部获取t的值
            print(test(t))

            # 或者

        def test1():
            k = input("请输入一个值: ")
            print("输入的值是:", k)

test1()

* return  call=return value  None print()

* print('hello', end='')　disable new lines

* print('cat','dog','mice',sep=',')

### the call stack

* function calls return to the line number they were called from.

* local and global scope = 作用域 访问

!!! note "f()"

    在 Python 中，定义函数时是否在括号内写参数取决于你的函数是否需要从外部接收数据。如果你的函数不需要外部传入的数据来执行任务，那么就定义为不带参数的函数。如果函数需要外部数据，那么就需要在括号内定义一个或多个参数。

```python
def test(t):
    print("参数值为:", t)
test("Hello")
```

???+ scope

    local can access to global
    python可以用模组所以都规定好local可以方便

```python
    global eggs    
    eggs = 'spam'
```

* fuction as a black box(parameters in value out)

``` python
def greet(name, message="Hello"):
    print(message, name)

```

* (errot) try and except 

``` python
def spam(divideBy): 
    try:
        return 42 / divideBy 
    except ZeroDivisionError:
        print('Error: Invalid argument.')
```

???+ try and exception

    if exception it will never return

```
Python 中有许多内置的异常，用于处理不同类型的错误情况。以下是一些常见的 Python 异常：

SyntaxError：语法错误。当 Python 解释器遇到不符合语法规则的代码时引发。

NameError：尝试访问一个未被定义的变量时引发。

TypeError：操作或函数应用于不适当类型的对象时引发。

ValueError：操作或函数接收到具有正确类型但不适当的值时引发。

IndexError：在使用序列索引（列表、元组等）时，索引超出范围时引发。

KeyError：使用字典时，尝试访问字典中不存在的键时引发。

AttributeError：尝试访问对象不存在的属性或方法时引发。

ZeroDivisionError：当除数为零时引发。

IOError / OSError：输入/输出操作失败（例如打开文件）时引发。

ImportError：在导入模块或对象时，找不到对应项时引发。

StopIteration：在迭代器没有更多元素可迭代时引发。

KeyboardInterrupt：用户中断程序执行（通常是通过按下 Ctrl+C）时引发。

FileNotFoundError：尝试访问的文件或目录不存在时引发。

MemoryError：操作因内存不足而无法完成时引发。

OverflowError：算术运算的结果太大而无法表示时引发。
```

## 4 lists tuples

### basic

* list[0] starting from 0 负数就是倒着数

???+ multiple

    >>> spam = [['cat', 'bat'], [10, 20, 30, 40, 50]]

    >>> spam[0]

    ['cat', 'bat']

    >>> spam[0][1]

    'bat'

    >>> spam[1][4] 50

!!! warning inline end "warning"

    python的范围都是从0到不含右端，【0，x）

* slice list_name[0:4]  (从零到三，4不包括) function[:]

* len(list_name)

* del list_name[2]

### for loop and list

!!! warning 
    在for里使用return会直接返回值然后结束循环

* range(len(list_name))

        >>> supplies = ['pens', 'staplers', 'flamethrowers', 'binders']
        >>> for ...
        Index 0 Index 1 Index 2 Index 3
        i in range(len(supplies)):
        print('Index ' + str(i) + ' in supplies is: ' + supplies[i])
        in supplies is: pens
        in supplies is: staplers
        in supplies is: flamethrowers in supplies is: binders

* for i in [0,1,2,3]

* in and not in

* tuple unpacking 快速将list提取并赋值给其他

* enumerate()

???+ example

    for index, item in enumerate(list_name)

    print(messages[random.randint(0, len(messages) - 1)])

* random.choice random.shuffle

### Augmented Assignmet Operators

       x += num --> x = x+num
        -= num
        *= num
        /= num
        %= num

### method methods belong to a single data type

> 方法是和对象关联的函数

* list_name.index('0')

* list_name.append('ex')

* list_name.insert(1,'ex')

* list_name.remove('ex')  pop del

* list_name.sort() 排序 list_name.sort(reverse=True) list_name.sort(key=str.lower)

* listname.reverse()

* \ 表示换行但是语句连续

### sequence data types

!!! note inline end "rules"
    上述语法对所有sequence类都适用，包括for in 等等，但是string不能改自身数据

> strings lists tuple

* tuple is immutable

### tuple

* tuple = (0,1,2)  tuple[0:3]

* type(('hello',)) == tuple  type(('hello')) == string

???+ note
    也就是说通过加逗号可以让str变成tuple，这样别人可以知道你不希望它被改变

### reference

!!! note
    编程时为变量赋值的实际含义是首先在电脑中存放数值，然后将其reference给变量，因此我们改变的是变量的reference而不是真的那个值

???+ warning "list value"
    当为list赋值，储存的也是reference，这意味着真的表只有一个，如果修改表值所有用到reference的变量都会跟着变。
        
        ➊ >>>spam=[0,1,2,3,4,5]
        ➋ >>> cheese = spam # The reference is being copied, not the list. 
        ➌ >>> cheese[1] = 'Hello!' # This changes the list value.
        >>> spam
        [0, 'Hello!', 2, 3, 4, 5]
        >>> cheese # The cheese variable refers to the same list.
        [0, 'Hello!', 2, 3, 4, 5]

* id() list() tuple()

* passing reference

        def eggs(someParameter): 
        someParameter.append('Hello')
        spam = [1, 2, 3] 
        eggs(spam) 
        print(spam)

* 不改变原表

```python
import copy
copy.copy() # 复制一个表，不含lists的表
copy.deepcopy() # 如果原表内包含lists
```

## ５dictionaries and structuring DATA

### basic

* key and key-value pair  (key and value) = item

`myCat = {'size': 'fat', 'color': 'gray', 'disposition': 'loud'} `

            >>> myCat['size']
            'fat'
            >>> 'My cat has ' + myCat['color'] + ' fur.' 
            'My cat has gray fur.'

* unoredered which means same dictionary in different order is ok

* data deleted after running. ch.9 to learn how to save data

* method: .keys() .value() .items()  tuple value can be used in for loops

???+ type
    上述method返回的值是dict_key类型的类表

        spam = {'color': 'red', 'age': 42} 
        for v in spam.values():
            print(v)

        red 
        42

* 检查值是否在： in 、 not in 查key可以省略

* get() get('key's value',value if wrong)

* setdefault(key, default value) 

!!! warning
    spam.setdefault('color', 'black')
    这行代码的作用是：检查字典 spam 中是否有 'color' 这个键，如果没有，则将 'color' 键的值设置为 'black'。如果 'color' 已经存在于 spam 中，则 setdefault() 不做任何改变，并保留原来的值。

* import pprint   pprint() pformat()

### data structure

* 基本上就是建模 画流程图分析 把实际问题转化为数学模型选择合适的数据结构去解决

### nested dictionaries and lists

* to contain ordered series of value

???+ note 
        def totalBrought(guests, item): numBrought = 0
            for k, v in guests.items():
            numBrought = numBrought + v.get(item, 0)
            return numBrought 

        使用 .items() 可以遍历字典的键和值。
        使用 .get() 可以安全地访问字典中的特定键的值，并在该键不存在时返回一个默认值。 

## ６manipulating strings

## string literals

* " "   ''  "" if ' is included

**escape characters** ：\ 

`spam = 'Say hi to Bob\'s mother.'`

???+ example
    \'
    \"
    \t
    \n
    \\

**raw string** :r    对打印路径很实用

`>>> print(r'That is Carol\'s cat.') That is Carol\'s cat.`

**triple quotes**：``` multiline ```

**multiline comments**: """ """

**indexing and slicing strings**: spam[7:]  spam[:5]

**string interpolation** : /%s

`'My name is %s. I am %s years old.' % (name, age)`

**f-strings**: {parameter}

`f'My name is {name}. Next year I will be {age + 1}.'`

**string method**: return new string value

```python
to handle input problems:
method:
    stringName.upper()
    .lower()
    .isupper()
    .islower()
    

print('How are you?')
feeling = input()
if feeling.lower() == 'great':
    print('I feel great too.') 
else:
    print('I hope the rest of your day is good.')

'HELLO'.lower().islower()
True
```

**the isX() methods**: helpful to valid users's input

```python
isalpha()  whether only letters
isalnum()  wheter all letters and nums
isdecimal()
isspace() [spaces,tabs and newlines]
istitle() [Title]
```

```python
>>> 'hello'.isalpha() True
>>> 'hello123'.isalpha() False
>>> 'hello123'.isalnum() True
>>> 'hello'.isalnum() True
>>> '123'.isdecimal() True
>>> ' '.isspace() True
>>> 'This Is Title Case'.istitle() True
>>> 'This Is Title Case 123'.istitle() True
>>> 'This Is not Title Case'.istitle()
False
>>> 'This Is NOT Title Case Either'.istitle() False
```

```python
while True:
    print('Enter your age:') 
    age = input()
    if age.isdecimal():
        break
    print('Please enter a number for your age.')
while True:
    print('Select a new password (letters and numbers only):') 
    password = input()
    if password.isalnum():
        break
    print('Passwords can only have letters and numbers.')
```

**the .startwith() and endwith() method**:

```python
>>> 'Hello, world!'.startswith('Hello') True
>>> 'Hello, world!'.endswith('world!') True
>>> 'abc123'.startswith('abcdef') False
>>> 'abc123'.endswith('12') False
>>> 'Hello, world!'.startswith('Hello, world!') True
>>> 'Hello, world!'.endswith('Hello, world!') True
```

**the .join() and split() methods**:

* join called on lists and return strings

* split called on strings and return lists

???+ warning
    the words used as a sign to split will not saved to lists

```python
>>> ', '.join(['cats', 'rats', 'bats'])
'cats, rats, bats'
>>> ' '.join(['My', 'name', 'is', 'Simon'])
 'My name is Simon'
>>> 'ABC'.join(['My', 'name', 'is', 'Simon']) 'MyABCnameABCisABCSimon'

>>> 'My name is Simon'.split()
 ['My', 'name', 'is', 'Simon']

 >>> 'MyABCnameABCisABCSimon'.split('ABC') 
 ['My', 'name', 'is', 'Simon']
>>> 'My name is Simon'.split('m')
['My na', 'e is Si', 'on']
```

???+ note
    a common use for split() is to split multiline strings

```python
>>> spam = '''Dear Alice,
How have you been? I am fine. There is a container in the fridge that is labeled "Milk Experiment."
Please do not drink it.
Sincerely,
Bob'''
>>> spam.split('\n')
['Dear Alice,', 'How have you been? I am fine.', 'There is a container in the fridge', 'that is labeled "Milk Experiment."', '', 'Please do not drink it.', 'Sincerely,', 'Bob']
```

**split with .partition() method**: 一分为三

???+ warning 
    this will keep the split word and only split once.
    if no split word found, return whole string and two '' '' 

```python
>>> 'Hello, world!'.partition('w') 
('Hello, ', 'w', 'orld!')
>>> 'Hello, world!'.partition('world') 
('Hello, ', 'world', '!')
```

```python
>>> 'Hello, world!'.partition('XYZ')
 ('Hello, world!', '', '')
```

**use this to assign value**

```python
>>> before, sep, after = 'Hello, world!'.partition(' ') 
>>> before
'Hello,'
>>> after
'world!'
```



