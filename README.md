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


ord（）获取字符的整数表示          chr（）把编码转换为对应的字符
example：
>>> ord('c')
99
>>> chr(100)
'd'

‘ABC’是字符串      b'ABC'（或b"ABC"）这只占用一个字节的     str与bytes互相变换
example:
>>> 'ABC'.encode('ascii')           #将ABC转换为ASCII编码
b'ABC'
>>> '中文'.encode('utf-8')            #将中文转换为utf-8编码
b'\xe4\xb8\xad\xe6\x96\x87'


将Bytes变成str需要用到decode（）         其中如果出现些许错误则不能正常编译，但可以使用errors=‘ignore’忽略错误字节
example：
 b'ABC'.decode('ascii')         
'ABC'
>>> b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
'中文'
 b'\xe4\xb8\xad\xe6'.decode('utf-8',errors='ignore')
'中'


len（‘****’）可以计算str有多少个字符
example：
len('ANC')
3
len(b'\xe4\xb8\xad\xe6\x96\x87')
6
>>> len('中文'.encode('utf-8'))
6
总结，在编码过程中尽量使用utf-8进行编码，或者使用统一的字符。       开头一般使用：  # -*- coding: utf-8 -*-


%是python中的格式化     %%表示一个%    %d整数（替换）      %f浮点数      %s字符串（替换），可以把任何数据类型转换为字符串     %s十六进制整数
example：
'age: %s. male: %s' % (24,True)     #   %s表示替换
'age: 24. male: True'
'growth rate: %d %%' %10        #可以用两个%%转义成%
'growth rate: 10 %'

little question:
# -*- coding: utf-8 -*-
s1 = 72
s2 = 85
r = (s2-s1)/s1*100
print("growth rate:%s %%" % r)
growth rate:18.055555555555554 % 




















