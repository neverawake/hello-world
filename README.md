# hello-world
begin PY learning
i've done nothing
exit()----shot down the software
print('******')----打印出文字，单双引号不能混用
print（*，*）---中间加，会输出空格
input（）---输入字符串    
name=input(‘please input ur name：’)    
wyz
print('hello',name)


#字开头则表示注释
Python大小写敏感，，，千万别写错


\是转义字符          \n代表换行    \t表示制表符     \\表示\         
'I\'m \"OK\"!'======I'm "OK"!----这段话既包含‘’也包含“”
example:
print('I\'m ok')
I'm ok

print('I\'m learning\nPython')
I'm learning 
Python

r''表示''内部的字符默认不转义   
example：
print(r'\\\t\\')
\\\t\\
>>> print('\\\t\\')  
\	\

换行结构：
print('''line1
line2
line3''')
line1
line2
line3


布尔值    只有true 或者false    可以用and（与） or（或） not（非）运算
example：
3>2
True
2>3
False

and   所有运算都是true输出才是true
>>> True and True
True
>>> True and False
False
>>> False and False
False
>>> 5 > 3 and 3 > 1
True


or    只要有一个true输出就是true
>>> True or True
True
>>> True or False
True
>>> False or False
False
>>> 5 > 3 or 1 > 3
True


not   可以把true变成false ，false变成true
>>> not True
False
>>> not False
True
>>> not 1 > 2
True


    a=1---a是整数型变量          a='1'---a是字符串
example:
a = 123 # a是整数型变量
print(a)
a = 'ABC' # a变为字符串
print(a)


/计算结果为浮点数     //计算结果为整数     %计算结果为整除剩下的余数
example：
>>> 10/3
3.3333333333333335
>>> 10//3
3
>>> 10%3
1

one little work.....
n=123
f=456.789
s1='hello,world'
s2='hello,\'adam\''
s3=r'hello,"bart"'
s4=r'''hello,
lisa！'''
print(n,'\n',f,'\n',s1,'\n',s2,'\n',s3,'\n',s4,)

