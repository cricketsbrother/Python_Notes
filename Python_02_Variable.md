# python_02 variable
## Variable Types
+ 整型：任意大小, Python 3.x中只有int，而且支持
	+ 二进制 `0b100`
	+ 八进制 `0o100` 
	+ 十进制 `100`
	+ 十六进制 `0x100`
+ 浮点型：数学写法`123.456`, 科学计数法`1.23456e2`。
+ 字符串型：单引号或双引号括起来的任意文本，
	EG: `'hello'`
		`"hello"`,
	字符串还有原始字符串表示法、字节字符串表示法、Unicode字符串表示法.
	多行的形式（用三个单引号或三个双引号开头，三个单引号或三个双引号结尾）。

```python
print('''
this is multiline text
hhhhhhh
''')
```

```python
print("""
	hjkhkj
	hjkhkjh
	""")
```
+ 布尔型：可以直接用`True`、`False`表示布尔值（请注意大小写），
也可以通过布尔运算计算出来（例如3 < 5会产生布尔值True，而2 == 1会产生布尔值False）。
+ 复数型：形如`3+5j`，跟数学上的复数表示一样，唯一不同的是虚部的i换成了j。

## Variable Names
+ 硬性规则
	+ 字母、数字、下划线，数字不能开头
	+ 大小写敏感
	+ 保留字不可
+ PEP8 非硬性
	+ 小写字母拼写，多单词下划线连接
	+ `_protectedInstance`
	+ `__privateInstance`

## Basic input output
### Input
从键盘获取为字符串 要类型转换
```python
a = int(input('a = '))
```
### Output

```python
print(*objects, sep=' ', end='\n', file=sys.stdout)
```
+ obj 可输出多个对象，`,`分割
+ sep 用来间隔多个对象，默认`' '`
+ end 以什么结尾，默认`'\n'`
+ file 要写入的文件对象

EG：
```python
>>> a = 1
>>> b = 'runoob'
>>> print(a,b)
1 runoob

>>> print("aaa""bbb") # 可以不分隔啊
aaabbb

>>> print("aaa","bbb")
aaa bbb

>>> print("www","runoob","com",sep=".")  # 设置间隔符
www.runoob.com
```
format print
```python
print('content' % ())
#eg
print('%d + %d = %d' % (a, b, a + b))
```
## Variable Type Checking

```python
#type checking
c = 7.999
d = 1 + 5j #complex
e = 'damn it'
f = True
print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
print(type(f))
```

result (md转义字符)
```
&lt;type 'int'&gt;
<type 'int'>
<type 'float'>
<type 'complex'>
<type 'str'>
<type 'bool'>
```

## Variable Type Convert
+ `int()`: 可以指定进制（源进制）

	`class int(x, base=10)`

	- x 字符串/数字
	- base 进制，默认10。带base参数，x以字符串形式输入。EG：
	```python
	>>> int('12',16) 
	18
	>>> int('0xa',16)  
	10  
	>>> int('10',8)  
	8
	```

+ `float(str)`:将一个字符串转换成浮点数。
+ `str()`：将指定的对象转换成字符串形式，可以指定编码。
+ `chr()`：将整数转换成该编码对应的字符串（一个字符）。
+ `ord()`：将字符串（一个字符）转换成对应的编码（整数）。

## Operator

| 运算符 | 描述 | 
|-----|------|
|`[]` `[:]`	|下标，切片|
|`**`			|指数|
|`~` `+` `-`		|按位取反, 正负号|
|`*` `/` `%` `//`|乘，除，模，整除|
|`+` `-`		|加，减|
|`>>` `<<`		|右移，左移|
|`&`	|按位与|
|`^` `|`	|按位异或，按位或|
|`<=` `<` `>` `>=`	|小于等于，小于，大于，大于等于|
|`==` `!=`	|等于，不等于|
|`is` `is not`	|身份运算符|
|`in` `not in`	|成员运算符|
|`not` `or` `and`	|逻辑运算符|
|`=` `+=` `-=` `*=` `/=` `%=` `//=` `**=` `&=` 	|`=` `^=` `>>=` `<<=`|


