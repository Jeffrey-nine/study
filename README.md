#### <div id='title'>第二章作业</div>

##### 1.列举你了解的编码及他们之间的区别？
- ASCII: python2默认的编码，一个字母是8位
- Unicode(万国码)：一个字母是32位
- UTF-8：万国码的压缩码，最少用一个字节，ascii码中的内容用1个字节保存、欧洲的字符用2个字节保存，东亚的字符用3个字节保存

##### 2.列举你了解的Python2和Python3的区别？
- python2默认的编码是ACSII，python3默认的编码是UTF-8
- print不一样
```
>>> print("hello", "world")
('hello', 'world')

>>> print("hello", "world")
hello world
```
##### 3.你了解的python都有那些数据类型？
- 整型
- 字符串
- 布尔

##### 4.补充代码，实现以下功能。
value = ('51devops"niubi')

print(value)  # 要求输出  51devops"niubi

##### 5.用print打印出下面内容：
```python
value = """
⽂能提笔安天下,
武能上⻢定乾坤.
⼼存谋略何⼈胜,
古今英雄唯是君。
"""
print(value)
```

##### 6.变量名的命名规范和建议？
- 变量的等号两边必须是有空格的，各大公司code review
- 变量名必须要有意义
- 变量名只能是字母、数字或下划线的任意组合
- 变量名建议不使用拼音和中文
- 变量名不要过长

##### 7.如下那个变量名是正确的？
```python
name = '51devops'   对
_ = 'echo'          对
_9 = "zhangsan"     对
9name = "xxx"
devops(edu = 666
```
##### 8.简述你了解if条件语句的基本结构
- if ...
- if ... else ...
- if ... elif ...  else ...


##### 9.设定一个理想数字比如：66，让用户输入数字，如果比66大，则显示猜测的结果大了；如果比66小，则显示猜测的结果小了;只有等于66，显示猜测结果正确。
```python
num = int(input("请输入数字："))
if num > 66:
    print("猜测的结果大了")
elif num < 66:
    print("猜测的结果小了")
else:
    print("猜测结果正确")
``` 

##### 10.写程序，成绩有ABCDE5个等级，与分数的对应关系如下.要求用户输入0-100的数字后，你能正确打印他的对应成绩
A   90-100
B   80-89
C   60-79
D   40-59
E   0-39
```python
number = int(input("请输入0-100的数字:"))
if number >= 90:
    print("成绩：A")
elif number >= 80:
    print("成绩：B")
elif number >= 60:
    print("成绩：C")
elif number >= 40:
    print("成绩：D")
elif number >= 0:
    print("成绩：E")
```

##### 11.模拟10086客服电话（条件语句的嵌套）

#### <div id='title'>第三章作业</div>

##### 1.猜数字，设定一个理想数字比如：66，让用户输入数字，如果比66大，则显示猜测的结果大了；如果比66小，则显示猜测的结果小了;只有等于66，显示猜测结果正确，然后退出循环。
```python
while True:
    num = int(input('请输入你要猜的数:'))
    if num > 66:
        print('猜测的结果大了')
    elif num < 66:
        print('猜测的结果小了')
    else:
        print('猜测结果正确')
        break
```
##### 2.在上一题的基础，设置：给用户三次猜测机会，如果三次之内猜测对了，则显示猜测正确，退出循环，如果三次之内没有猜测正确，则自动退出循环，并显示‘大笨蛋’
```python
count = 1
while count <= 3:
    num = int(input('请输入你要猜的数:'))
    if num > 66:
        print('猜测的结果大了')
    elif num < 66:
        print('猜测的结果小了')
    else:
        print('猜测结果正确')
        break
    count = count + 1
else:
    print('大笨蛋')
```

##### 3.使用两种方法实现输出 1 2 3 4 5 6 8 9 10 
```python
num = 0
while num < 10:
    num = num + 1
    if num == 7:
        continue
    print(num)
```
```python
num = 1
while True:
    if num == 10:
       print(num)
       break
    if num == 7:
       num = num + 1
       continue
    print(num)
    num = num + 1
```
##### 4.求1-100的所有数的和
```python
num = 1
sum = 0
while num <= 100:
	sum = sum + num
	num = num + 1
print(sum)
````

##### 5.输出 1-100 内的所有奇数
```python
num=0
while num<100:
    num = num + 1
    if num % 2==0:
        continue
    print(num)
```

##### 6.输出 1-100 内的所有偶数
```python
num = 1
while num < 101:
	if num % 2 == 0:
		print(num)
	num = num + 1
```

##### 7.求1-2+3-4+5 … 99的所有数的和
```python
num = 1
sum = 0
while num <100:
    if num % 2 == 1:
        sum = sum + num
    else:
        sum = sum - num
    num = num + 1
print(sum)
```

##### 8.⽤户登陆（三次输错机会）且每次输错误时显示剩余错误次数（提示：使⽤字符串格式化）
```python
count=3
username='zhaohui'
password='123456'
while count>0:
    name=input('请输入你的名字:')
    count = count - 1
    if name==username:
        password1=input('请输入密码:')
        if password1==password:
            print('登录成功')
            break
        else:
            print('请重新输入你的剩余错误次数%s'%(count))
            if countzhahu == 0:
                print('您的机会已经用完，结束本次操作')
                break
            continue
    else:
        print('用户名错误,剩余次数%s'%(count))
```
##### 9.猜年龄游戏
要求：允许用户最多尝试3次，3次都没猜对的话，就直接退出，如果猜对了，打印恭喜信息并退出。

```python
count = 0
age = 30
while count <3 :
    count =count + 1
    age_input = int(input("请输入您猜的年龄:"))
    if age_input != age:
        print("猜错了，请重新输入")
    else:
        print("恭喜")
        break
    if count == 3:
        print("")
```

##### 10.猜年龄游戏升级版
要求：允许用户最多尝试3次，每尝试3次后，如果还没猜对，就问用户是否还想继续玩，如果回答Y，就继续让其猜3次，以此往复，如果回答N，就退出程序，如猜果对了，就直接退出。
```python
count = 0
age = '30'
while True:
    age_input = input('请输入您猜的年龄:')
    if age_input == age:
        print('恭喜你，猜对啦！')
        break
    else:
        print('猜错啦，请重新输入')
        count = count + 1
        if count == 3:
            print('您是否想重新玩，回答Y或者N')
            ans = input('请输入Y或者N： ')
            if ans == 'Y':
                print('请继续猜')
            elif ans == 'N':
                print('感谢参与！')
                break
```


##### 第四章作业
##### 1.有变量name = “szk zeNb “ 完成如下操作：
- 移除 name 变量对应的值两边的空格,并输出处理结果
```python
name = "szk zeNb "
ret = name.strip()
print(ret)
```
- 判断 name 变量是否以 “sz” 开头,并输出结果（用切片）
```python
name = "szk zeNb "
value = (name[0:2])
if value == 'sz':
    print("是以'sz'开头")
else:
    print("不是以'sz'开头")
```
- 判断name变量是否以”Nb”结尾,并输出结果（用切片）
```python
name = "szk zeNb "
value = (name[-2:])
if value == 'Nb':
    print("是以'Nb'结尾")
else:
    print("不是以'Nb'结尾")
```
- 将 name 变量对应的值中的 所有的”z” 替换为 “p”,并输出结果
```python
name = "szk zeNb "
value = name.replace('z','p')
print(value)
```
- 将name变量对应的值中的第一个”z”替换成”p”,并输出结果
```python
name = "szk zeNb "
value = name.replace('z','p',1)
print(value)
```
- 将 name 变量对应的值根据 所有的”z” 分割,并输出结果
```python
name = "szk zeNb "
value = name.split('z')
print(value)
```
- 将name变量对应的值根据第一个”z”分割,并输出结果
```python
name = "szk zeNb "
value = name.split('z',1)
print(value)
```
- 将 name 变量对应的值变大写,并输出结果
```python
name = "szk zeNb "
value = name.upper()
print(value)
```
- 将 name 变量对应的值变小写,并输出结果
```python
name = "szk zeNb "
value = name.lower()
print(value)
```
- 请输出 name 变量对应的值的第 2 个字符?
```python
name = "szk zeNb "
print(name[1:2])
```
- 请输出 name 变量对应的值的前 3 个字符?
```python
name = "szk zeNb "
print(name[0:4])
```
- 请输出 name 变量对应的值的后 2 个字符?
```python
name = "szk zeNb "
print(name[-2:])
```
##### 有字符串s = “123a4b5c”
- 通过对s切片形成新的字符串 “123”
```python
s = "123a4b5c"
print(s[0:3])
```
- 通过对s切片形成新的字符串 “a4b”
```python
s = "123a4b5c"
print(s[3:6])
```
- 通过对s切片形成字符串s5,s5 = “c”
```python
s = "123a4b5c"
s5 = s[-1:]
print(s5)
```

- 通过对s切片形成字符串s6,s6 = “ba2”
```python
s = "123a4b5c"
s6 = s[-3:-8:-2]
print(s6)
```

##### 使用while和for循环字符串 s=”asdfer” 中每个元素
```python
s = "asdfer"
for value in s:
    print(value)
```

```python
s= 'asdfer'
count =0
while count<len(s):
    print(s[count])
    count+=1
```

##### 使用while和for循环分别对字符串 message = “伤情最是晚凉天，憔悴厮人不堪言。” 进行打印。
```python
message = "伤情最是晚凉天，憔悴厮人不堪言。"
count =0
while count<len(message):
    print(message[count])
    count+=1
```

```python
message = "伤情最是晚凉天，憔悴厮人不堪言。"
for value in message:
    print(message)
```

##### 获取用户输入的内容，并计算前四位”l”出现几次,并输出结果。
```python
value = input("请输入内容：")
lenth = len(value)
index = 0
count = 0
while index < 4:
    if value[index] =='l':
        count += 1
    else:
        pass
    if index == lenth-1:
        break
    index += 1
print("一共有%s个l"%(count,))
```

##### 获取用户两次输入的内容，并将所有的数据获取并进行相加
```python
num1 = input("请输入：")
num2 = input("请输入：")
count = 0
new_num1 = ''
while count < len(num1):
    s1 = num1[count]
    if s1.isdigit():
        new_num1 += s1
    count += 1
n1 = int(new_num1)
count = 0
new_num2 = ''
while count < len(num2):
    s2 = num2[count]
    if s2.isdigit():
        new_num2 += s2
    count += 1
n2 = int(new_num2)
print(n1 + n2)
```
