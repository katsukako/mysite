# Automate boring shit

> 其他需要学习的内容：操作系统，软件工程基础，linux，计算机网络基本知识，shell程序设计等等 [csdiy](https://csdiy.wiki/)

> [pythonBasic](https://github.com/jackfrued/Python-Core-50-Courses/blob/master/%E7%AC%AC10%E8%AF%BE%EF%BC%9A%E5%B8%B8%E7%94%A8%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B9%8B%E5%AD%97%E7%AC%A6%E4%B8%B2.md)

## 实用技巧

???+ f-string

        a = 5
        b = 10
        result = f"Five plus ten is {a + b}."
        print(result)  # 输出: Five plus ten is 15.

???+ note 'in multiple or'
    为了简洁地表示条件 if months[d] == '04' 或 '09' 或 '11'，您可以使用 in 操作符来检查 months[d] 是否在一个指定的集合中。

### 函数的可变参数 可用于解包语法

???+ note '可变参数'
    *args 任意数量的参数
    **kwargs 任意数量的key=关键字参数

## 生成式

在Python中，生成式（Comprehensions）是一种简洁而强大的构建Python数据结构的方法，包括列表（List Comprehensions）、字典（Dictionary Comprehensions）、集合（Set Comprehensions）和生成器（Generator Expressions）。

### 1. 列表生成式（List Comprehensions）

列表生成式提供了一种创建列表的简洁方法。它可以通过对序列的每个元素应用一个表达式来生成新列表。

```python
# 示例：使用列表生成式创建一个平方数列表
squares = [x**2 for x in range(10)]
```

### 2. 字典生成式（Dictionary Comprehensions）

字典生成式用于创建字典。类似于列表生成式，它通过对序列的元素应用表达式来创建字典的键值对。

```python
# 示例：使用字典生成式根据列表创建一个字典
squares_dict = {x: x**2 for x in range(10)}
```

### 3. 集合生成式（Set Comprehensions）

集合生成式用于创建集合，方式与列表和字典生成式相似。

```python
# 示例：使用集合生成式创建一个平方数集合
squares_set = {x**2 for x in range(10)}
```

### 4. 生成器表达式（Generator Expressions）

生成器表达式类似于列表生成式，但它返回一个生成器对象，而不是一次性生成整个列表。这对于处理大量数据时非常有用，因为它节省内存。

```python
# 示例：使用生成器表达式创建一个生成器
squares_gen = (x**2 for x in range(10))
```

### 作用

生成式的主要作用包括：

- **提高代码简洁性**：生成式允许用一行代码实现循环或条件逻辑来创建数据结构，增强代码的可读性。
- **性能优化**：尤其是列表生成式，通常比使用循环添加元素的方式更快、更高效。
- **内存高效**：使用生成器表达式可以在处理大数据集时节省内存。
- **灵活性**：可以在生成式中嵌入各种复杂的表达式和函数调用，使得数据处理更加灵活。

总的来说，生成式是Python中编写简洁、高效、可读性强代码的重要工具。

**作业集锦**：

```python
for x in range(len(tableData[0])):
    for y in range(len(tableData)):
        print(tableData[y][x].rjust(colwidths[y],' '),end =' ')
    print() # 通过循环结束手动有意识实现换行
```

???+ warning
    print('\n',end='') 和print()等效


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

???+ note 'list bianli'
    ```python
    items = ['Python', 'Java', 'Go', 'Kotlin']

    for item in items:
        print(item)
    ```

* in and not in

* tuple unpacking 快速将list提取并赋值给其他

* enumerate()

???+ example

    for index, item in enumerate(list_name)

    print(messages[random.randint(0, len(messages) - 1)])

* random.choice random.shuffle

### 列表的生成式

```python
# 创建一个由1到9的数字构成的列表
items1 = []
for x in range(1, 10):
    items1.append(x)
print(items1)

# 创建一个由'hello world'中除空格和元音字母外的字符构成的列表
items2 = []
for x in 'hello world':
    if x not in ' aeiou':
        items2.append(x)
print(items2)

# 创建一个由个两个字符串中字符的笛卡尔积构成的列表
items3 = []
for x in 'ABC':
    for y in '12':
        items3.append(x + y)
print(items3)
```

### 嵌套列表

```python
scores = [[0] * 3 for _ in range(5)]
scores[0][0] = 95
print(scores)
# [[95, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0], [0, 0, 0]]
```


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

### 元组应用 打包解包 交换变量

```python
# 打包
a = 1, 10, 100
print(type(a), a)    # <class 'tuple'> (1, 10, 100)
# 解包
i, j, k = a
print(i, j, k)       # 1 10 100
```

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

### 表现形式

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

???+ note
    word[0] word[-1] 可以表示string首尾
    word = word[1:] 或者w[:-1]为word修改形态

**string interpolation** : /%s

`'My name is %s. I am %s years old.' % (name, age)`

**f-strings**: {parameter}

`f'My name is {name}. Next year I will be {age + 1}.'`

### 判断和改变

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

### 分合

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

**自动对齐**: .rjust(num,'fuhao') .ljust() .center()

???+ note
    rjust意味着把之前的文字放在右边

**去除空格**:.strip('') .rstrip() .lstrip()

```python
>>> spam = 'SpamSpamBaconSpamEggsSpamSpam' 
>>> spam.strip('ampS')
'BaconSpamEggs'
```

!!! warning 
    order doesnot matter


**ascii转化**: ord('A') chr(65) 

[moreaboutunicode](https://www.youtube.com/watch?v=sgHbC6udIqc)

**pyperclip module**: pyperclip.copy() .paste()  send and receive

???+ note
    pyperclip可以获取剪贴板内容

**sys.argv**:获取命令行参数 0总是脚本名字

???+ warning 
    sudo chmod +x fileName 赋予文件权限
    命令行参数需要打在命令行里

**批量处理剪贴板**：

```python
#! python3
# bulletPointAdder.py - Adds Wikipedia bullet points to the start # of each line of text on the clipboard.
import pyperclip
text = pyperclip.paste()
# Separate lines and add stars.
lines = text.split('\n')
for i in range(len(lines)): # loop through all indexes for "lines" list
    lines[i] = '* ' + lines[i] # add star to each string in "lines" list
text = '\n'.join(lines)
pyperclip.copy(text)
```

## auto

## ７regular expression　正则表达式 regexes

???+ note
    r 等价于无数\ raw
    impor re
    正则表达式需要把每一种情况拆出来写明白 由于没有if这种东西只能枚举所有情况
    分组判断的时候是要加括号的

[正则表达式测试](https://pythex.org/)


Python中的正则表达式是一种文本模式描述的方法，用于实现字符串的匹配、查找和替换操作。正则表达式是一种非常强大的工具，能够处理复杂的文本处理任务。Python通过内置的`re`模块提供正则表达式支持。

???+ warning 'cuoti'
    ^$正则找首尾，而且sub none就是删除

### 基本使用

1. **导入re模块**：
   ```python
   import re
   ```

2. **基本函数**：
   - `re.match(pattern, string)`：从字符串的开始处匹配正则表达式。
   - `re.search(pattern, string)`：在整个字符串中搜索模式。
   - `re.findall(pattern, string)`：找出字符串中所有符合模式的部分。
   - `re.sub(pattern, repl, string)`：用另一个字符串替换所有符合模式的部分。
   - `re.VERBOSE`:
   - `re.DOTALL`
   - `re.IGNORECASE`
   - `re.compile(pattern)` 定义
   - `robocop = re.compile(r'robocop', re.I)` 忽略大小写

???+ note "替换与查找并替换"
    替换：
    >>> namesRegex = re.compile(r'Agent \w+')
    >>> namesRegex.sub('CENSORED', 'Agent Alice gave the secret documents to Agent Bob.') 'CENSORED gave the secret documents to CENSORED.'

    查找并替换：
    >>> agentNamesRegex = re.compile(r'Agent (\w)\w*')
    >>> agentNamesRegex.sub(r'\1****', 'Agent Alice told Agent Carol that Agent Eve knew Agent Bob was a double agent.')
    A**** told C**** that E**** knew B**** was a double agent.'


???+ note "findall分组规则
    findall 有无分组返回的值不一样 有分组会把所有分组单独返回

3. **编译正则表达式**：
   - 如果同一个正则表达式需要多次使用，可以先将其编译为一个正则表达式对象，以提高效率。
   ```python
   pattern = re.compile(r'\bfoo\b')
   ```

### 正则表达式语法

- **字符**： 以下都是找一个，要复数要组合
  - `.`：匹配任意单个字符（除了换行符）。
  - `\d`：匹配任意数字。
  - `\D`: 任意非数字
  - `\w`：匹配任意字母数字字符。
  - `\W`：匹配任意非字母数字字符。
  - `\s`：匹配任意空白字符。
  - `\S`：匹配任意非空白字符。

???+ warning
    >>> atRegex = re.compile(r'.at')
    >>> atRegex.findall('The cat in the hat sat on the flat mat.') ['cat', 'hat', 'sat', 'lat', 'mat']
    只匹配一个字符 例如flat变成lat

**(.*) anything**: 

.* greedy  .*? non-greedy

???+ note "re.DOTALL 找\n 换行"
    re.DOTALL 找\n 换行
    >>> noNewlineRegex = re.compile('.*')
    >>> noNewlineRegex.search('Serve the public trust.\nProtect the innocent. \nUphold the law.').group()
    'Serve the public trust.'
    >>> newlineRegex = re.compile('.*', re.DOTALL)
    >>> newlineRegex.search('Serve the public trust.\nProtect the innocent. \nUphold the law.').group()
    'Serve the public trust.\nProtect the innocent.\nUphold the law.'

- **字符类**：
  - `[abc]`：匹配方括号内的任意一个字符（a、b 或 c）。
  - `[^abc]`：匹配不在方括号内的任意字符。
  - `[3-5]`
  - `[a-zA-Z]`

- **量词**：
  - `*`：匹配前面的字符0次或多次。
  - `+`：匹配前面的字符1次或多次。
  - `?`：匹配前面的字符0次或1次。
  - `{n}`：匹配前面的字符n次。
  - `{n,}`：匹配前面的字符至少n次。
  - `{n,m}`：匹配前面的字符至少n次，但不超过m次。

???+ note
    ()? 用来分组 比如bat(wo)?man
    (){3,5} greedy
    (){3,5}? lazy
    (?:)? 非捕获组

- **边界**：
  - `^`：匹配字符串的开始。
  - `$`：匹配字符串的结束。
  - `\b`：匹配单词边界。


- **分组和引用**：
  - `(pattern)`：匹配括号内的模式，并作为一个组。
  - `\1`, `\2`等：引用前面定义的组。
  - `\)` 括号逃逸
  - | or 返回第一个找到的

### 示例

```python
import re

# 查找字符串中的所有数字
result = re.findall(r'\d+', 'hello 123 world 456')
print(result)  # 输出: ['123', '456']

# 替换字符串中的数字为'#'
replaced = re.sub(r'\d+', '#', 'hello 123 world 456')
print(replaced)  # 输出: hello # world #

# 分组
phoneNumRegex = re.compile(r'(\d\d\d)-(\d\d\d-\d\d\d\d)') 
mo = phoneNumRegex.search('My number is 415-555-4242.') 
mo.group(1)
'415'
mo.group(2)
```

正则表达式非常强大，但同时也相对复杂。在使用时需要注意正确构造模式字符串，并理解其含义。常见的应用场景包括数据验证、数据提取和复杂字符串操作等。

### 组合

```python
r`^\d+$` 
>>> wholeStringIsNum = re.compile(r'^\d+$')
>>> wholeStringIsNum.search('1234567890')
<re.Match object; span=(0, 10), match='1234567890'> 
>>> wholeStringIsNum.search('12345xyz67890') == None 
True
>>> wholeStringIsNum.search('12 34567890') == None 
True
```

### 复杂时写法

```python
    phoneRegex = re.compile(r'''( 
    (\d{3}|\(\d{3}\))?  # area code
    (\s|-|\.)?          # separator
    \d{3}               # first 3 digits
    (\s|-|\.)           # separator
    \d{4}               # last 4 digits
    (\s*(ext|x|ext.)\s*\d{2,5})?     # extension
    )''', re.VERBOSE)
```

!!! warning expression
    note that ''' is not ```
    (?!...) 否定预测

{'at least one'} 创建集合的构筑器

set()

???+ note 'set去重'

    set可以去重，这很方便

```python
set1 = {1, 2, 3, 3, 3, 2}
print(set1)         # {1, 2, 3}
print(len(set1))    # 3    
```




 











