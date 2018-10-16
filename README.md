# hello-world
							begin PY learning
i've done nothing
exit()----shot down the software
print('******')					#print,do not mix ' with "
print（*，*）					#add ','and there will be a space
input（）						#input str  
name=input(‘please input ur name：’)    
wyz
print('hello',name)


Python is sensitive about CAPs 


\ means transference          \n means tab    \t means character table     \\ mean one '\'         
'I\'m \"OK\"!'======I'm "OK"!		#combine both ‘’ and “”
example:
print('I\'m ok')
I'm ok

print('I\'m learning\nPython')
I'm learning 
Python

r'' 					# the thing inside '' will not be transfered   
example：
print(r'\\\t\\')
\\\t\\
>>> print('\\\t\\')  
\	\

							tab structure
print('''line1
line2
line3''')
line1
line2
line3


							boolean  
							
only true or false  			  and（与） or（或） not（非）
example：
3>2
True
2>3
False

and  					# all the operations are true the output is true
>>> True and True
True
>>> True and False
False
>>> False and False
False
>>> 5 > 3 and 3 > 1
True


or  					# as long as one true appeared the out put is true 
>>> True or True
True
>>> True or False
True
>>> False or False
False
>>> 5 > 3 or 1 > 3
True


not   					# turn true into false and false into true
>>> not True
False
>>> not False
True
>>> not 1 > 2
True


    a=1		# a is a int          a='1'		# a is a str
example:
a = 123			 # a is a int  
print(a)
a = 'ABC' 		# a is a str
print(a)


/ # output is a float     // # output is a int     % # output is a remainder
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


ord（） # obtain the int of character        chr（） # change code into character
example：
>>> ord('c')
99
>>> chr(100)
'd'

‘ABC’ is a str      b'ABC'（ or b"ABC"）only takes one byte   str and bytes change
example:
>>> 'ABC'.encode('ascii')           # turn ABC into ASCII code
b'ABC'
>>> '中文'.encode('utf-8')            # turn chinese into utf-8 code
b'\xe4\xb8\xad\xe6\x96\x87'


decode（） 			# turn bytes into str ."error='ignore'" can be used to some mistakes that can't be translated    
example：
 b'ABC'.decode('ascii')         
'ABC'
>>> b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
'中文'
 b'\xe4\xb8\xad\xe6'.decode('utf-8',errors='ignore')
'中'


len（‘****’）		 # get the byte of str
example：
len('ANC')
3
len(b'\xe4\xb8\xad\xe6\x96\x87')
6
>>> len('中文'.encode('utf-8'))
6
be advised. use the same code to code in one program. the first line is always：  # -*- coding: utf-8 -*-


'%'	 # format
'%%'	 # one '%'    
'%d'	 # int replace      
'%f'	 # float      
'%s'	 # str replace any data type into str   
'%s' 	 # hexadecimal int
example：
'age: %s. male: %s' % (24,True)     #   '%s' means replace
'age: 24. male: True'
'growth rate: %d %%' %10      	  # two '%%' is transfered into one '%'
'growth rate: 10 %'

little question:
# -*- coding: utf-8 -*-
s1 = 72
s2 = 85
r = (s2-s1)/s1*100
print("growth rate:%s %%" % r)
growth rate:18.055555555555554 % 


							list
							
LIST     	 	 # can be expressed :T=['A','B','C']      
len（T）			# query amount of element in T      
T[0]		 	 # first element in list T       
T[-1]			 # last element
T.append('****') 	# add element into the end of T       
T.insert(1,'***')	# add element into position 1 of T     
T.pop()			# delete the end element          
T.pop(i)		# delete the element in position i      
T[i]='***'		# replace the element in position i



								TUPLE      
								
T=('A','B','C')   		  # elements in TUPLE can only be queried and can't be changed,very stable！
T=(1,)				# define one element TUPLE need to use ',' to eliminate mathematical ambiguity(数学歧义)
one little question:
# -*- coding: utf-8 -*-
L = [
    ['Apple', 'Google', 'Microsoft'],
    ['Java', 'Python', 'Ruby', 'PHP'],
    ['Adam', 'Bart', 'Lisa']
]
answer:
# 打印Apple:
print(L[0][0])
# 打印Python:
print(L[1][1])
# 打印Lisa:
print(L[2][2])

							
								judge
								
question：
小明身高1.75，体重80.5kg。请根据BMI公式（体重除以身高的平方）帮小明计算他的BMI指数，并根据BMI指数：
低于18.5：过轻
18.5-25：正常
25-28：过重
28-32：肥胖
高于32：严重肥胖
# -*- coding: utf-8 -*-
height = 1.75
weight = 80.5
bmi = weight/(height*height)
if bmi<18.5:
      print('too light')
elif  bmi<25:
      print('pass')
elif  bmi<32:
      print('fat')  
else:
      print('too fat')
      

							loop
							
for and while loop：
sum=0
>>>for x in range(101):
	sum=sum+x
	print (sum)   		  # sum from 1-100

sum=0
>>> n=99
>>> while n>0:
	sum=sum+n
	n=n-2
	print(sum)   		   # odd number sum from 1-100

'break' usd in while
n = 1
while n <= 100:
    if n > 10: 			# while n=11 the condition is satisfied to implement 'break' sentence
        break 			# 'break' will end current loop
    print(n)
    n = n + 1
print('END')

'continue' use in while
n = 0
while n < 10:
    n = n + 1
    if n % 2 == 0: 	# if n is even number, implement 'continue' sentence 
        continue	# 'continue' sentence will continue next round loop and the following sentence 'print()' will be implemented
    print(n)


							
						dict and set
							
D={'a':12,'b':13,'c':14,'d':15}		# set dict'D',element:a=12,b=13,c=14,d=15
D['a']					# query a in D
12
D['e']=18				# put e=18 in D，the ahead 'e' will be covered if continue put 'e'

'h' in D				# it will report error if 'h' not in D

D.pop('a')
12
D
｛'b':13,'c':14,'d':15,'e':18｝		# delete a from D

get语句不太会用

请务必注意，dict内部存放的顺序和key放入的顺序是没有关系的。

和list比较，dict有以下几个特点：

查找和插入的速度极快，不会随着key的增加而变慢；
需要占用大量的内存，内存浪费多。
而list相反：

查找和插入的时间随着元素的增加而增加；
占用空间小，浪费内存很少。
所以，dict是用空间来换取时间的一种方法。

dict可以用在需要高速查找的很多地方，在Python代码中几乎无处不在，正确使用dict非常重要，需要牢记的第一条就是dict的key必须是不可变对象。这是因为dict根据key来计算value的存储位置，如果每次计算相同的key得出的结果不同，那dict内部就完全混乱了。这个通过key计算位置的算法称为哈希算法（Hash）。要保证hash的正确性，作为key的对象就不能变。在Python中，字符串、整数等都是不可变的，因此，可以放心地作为key。而list是可变的，就不能作为key：


set similar to  dict，a group of keys，not storage value。but there is not repeat key in set
S=set（[1,2.3,2,2,2,3,3,4,5,5,6]）		#set a "SET‘S’"，contain element:1,2,3,no order,repeat element will be filtered 
S
{1,2,3,4,5,6}

S.add(9)
S
{1,2,3,4,5,6,9}					# add 9 into S 

S.remove（2）
S
{1,3,4,5,6,9}					# delete 2 from S

T=set（[1,2,3,8]）				# set a "set‘T’"
S&T						
{1,3}						# intersection
S|T
{1,2,3,4,5,6,8,9}				# aggregation



							function
						
abs（**)			# the absolute value of **
a=abs			
a(-1)
1			# command a=abs

max(1,2,*,*,*,*,)	# the max one betwween the elements
hex(i)			# hexadecimal
	
define a function
def my_abs(i):
	if i >=0:
		return i
	else:
		return -i

	
>>> print(my_abs(-100))		# define a abs

def nop():
	pass			# if not figure out what to put here can use a empty funcion here

if age>=18:
	pass			# this sentence will be passed
	
 if not isinstance(x, (int, float)):
        raise TypeError('bad operand type')		# parameter check, only allow int and float


def my_abs(i):
	if not isinstance(i, (int, float)):
       		raise TypeError('bad operand type')
	if i >=0:
		return i
	else:
		return -i			# parameter checked function

def quadratic(a, b, c):
	for i in[a,b,c]:
		if not isinstance(i, (int, float)):
			raise TypeError('bad operand type')
	D=b*b-4*a*c
	if a==0:
		x=-c/b
		return x
	elif D<0:
		print('no answer')
	elif D>0:
		x1=(-b+math.sqrt(b*b-4*a*c))/2*a
		x2=(-b-math.sqrt(b*b-4*a*c))/2*a
		return x1,x2
	elif D==0:
		x1=x2=-b/(2*a)
		return x1,x2					# can't run
	
定义函数时，需要确定函数名和参数个数；

如果有必要，可以先对参数的数据类型做检查；

函数体内部可以用return随时返回函数结果；

函数执行完毕也没有return语句时，自动return None。

函数可以同时返回多个值，但其实就是一个tuple。


def power(x):
	return:x*x			# define x^2

def power(x,n):
	i=1
	while n>0:
	n=n-1
	i=i*x
	return i			# calculate x^n
一是必选参数在前，默认参数在后，否则Python的解释器会报错（思考一下为什么默认参数不能放在必选参数前面）；

二是如何设置默认参数。

当函数有多个参数时，把变化大的参数放前面，变化小的参数放后面。变化小的参数就可以作为默认参数。默认参数必须指向不变对象！！！


def calc(numbers):
	sum=0
	for n in numbers:
		sum=sum+n*n
	return sum				
calc([1,2,3,])
14
calc((1,2,3))
14					# it need to in put a list or tuple

reprogram:
def calc(*numbers):
	sum=0
	for n in numbers:
		sum=sum+n*n
	return sum
calc(1,2)
5					# add a '*',the numbers will make input as a tuple
if a tuple is already ahead,then we can use following code:
nums=[1,2,3]
calc(*nums)
14					# *num will change the elements in num as a changable parameter

def x(*nums):
	sum=1
	for i in nums:
		sum*=i
	return sum			# a plus fun
>>>x(1,2,3,4,5)
120

						variable parameter
						
						
 person('w',24)
name w age 24 other {}
>>> def person(name,age,**kw):				# define a fun,'**kw' is a keyword parameter
	print('name:',name,'age:',age,'other',kw)	# print it

	
>>> person('w',24)					# input the parameter
name: w age: 24 other {}				# it will automatically print it
>>> person('wyz',24,city='chongqing')
name: wyz age: 24 other {'city': 'chongqing'}
>>> person('wyz',24,gender='male',city='chongqing')	# u can put many parameters,varialbe parameter can expand the function
name: wyz age: 24 other {'gender': 'male', 'city': 'chongqing'}


extra={'city':'chongqing','job':'student'}
>>> person('wyz',24,**extra)
name: wyz age: 24 other {'city': 'chongqing', 'job': 'student'}		# make a dic and use '**extra' to input the value of the dic



def f1(a,b,c=0,*args,**kw):				# define a f1,parameter behind '*' will be regard as keyword parameter
	print('a=',a,'b=',b,'c=',c,'args=',args,'kw=',kw)	
	
>>> f1(1,2)				
a= 1 b= 2 c= 0 args= () kw= {}

>>> f1(1,2,c=3)
a= 1 b= 2 c= 3 args= () kw= {}

>>> f1(1,2,3,'a','b')
a= 1 b= 2 c= 3 args= ('a', 'b') kw= {}

>>> f1(1,2,3,'a','b',x=99)
a= 1 b= 2 c= 3 args= ('a', 'b') kw= {'x': 99}
	
	
	
>>> def f2(a,b,c=0,*,d,**kw):				# 
	print('a=',a,'b=',b,'c=',c,'d=',d,'kw=',kw)		
	


>>> f2(1,2,d=99,ext=None)
a= 1 b= 2 c= 0 d= 99 kw= {'ext': None}

*args是可变参数，args接收的是一个tuple；

**kw是关键字参数，kw接收的是一个dict。

以及调用函数时如何传入可变参数和关键字参数的语法：

可变参数既可以直接传入：func(1, 2, 3)，又可以先组装list或tuple，再通过*args传入：func(*(1, 2, 3))；

关键字参数既可以直接传入：func(a=1, b=2)，又可以先组装dict，再通过**kw传入：func(**{'a': 1, 'b': 2})。

使用*args和**kw是Python的习惯写法，当然也可以用其他参数名，但最好使用习惯用法。

命名的关键字参数是为了限制调用者可以传入的参数名，同时可以提供默认值。

定义命名的关键字参数在没有可变参数的情况下不要忘了写分隔符*，否则定义的将是位置参数。



						recursion
					

>>> def fact(n):
	if n==1:
		return 1
	else:
		return n*fact(n-1)		# a fun 'n!'
>>> fact(5)
120













