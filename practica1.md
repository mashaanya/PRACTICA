task2
```pyton
n = int(input())
a = []
for i in range(n+1):
    a.append(i)
b = []
for i in range(2, n+1):
    if a[i] != 0:
        b.append(a[i])
        for j in range(i+i, n+1, i):
            a[j] = 0
print(*b)

```
task6
```python
a = int(input())
b = int(input())
c = int(input())
d = int(input())
for x in range(d):
    for y in range(d):
        for z in range(d):
            if a*x + b*y + c*z == d:
                print(x, y, z)

```
task7
```python
a = int(input())
b = int(input())
l = []
for i in range(a, b+1):
    while i > 1:
        if i % 2 == 0:
            i //= 2
        else:
            i = (i*3+1)//2
    l.append(i)
print(l)
if len(l) == b-a+1:
    print("Right")
else:
    print("Wrong")
```
task8
```python
a = []
n = input()
znaki = ['+', '-', '/', '*']
while n != '0':
    a.append(n)
    n = input()

for i in range(len(a)):
    if not(a[i] in znaki):
        a[i] = int(a[i])
s = a[0]
for i in range(len(a)):
    if a[i] == '+':
        s += a[i+1]
    if a[i] == '-':
        s -= a[i+1]
    if a[i] == '/':
        s /= a[i+1]
    if a[i] == '*':
        s *= a[i+1]
print(s)

```
task9
```python
a = [1, 0, 1, 1, 1, 0, 1, 1]
lmain = 0
i1 = 0
l = 0
for i in range(len(a)):
    if a[i] == 1:
        l += 1
        if l >= lmain:
            lmain = l
            i1 = i
    else:
        l = 0
print('length =', lmain, 'index:', i1-lmain+1, i1)

```
task11
```python
school = {'1a': 25, '3a': 30}
inp = input()
while inp != 'stop':
    if inp == 'show':
        print(school)
    if (inp == 'change') or (inp == 'create'):
        clas = input()
        students = int(input())
        school.update({clas: students})
    if inp == 'delete':
        clas = input()
        school.pop(clas)
    inp = input()

```
входные данные для 12 задачи, чтобы не запутаться, лучше их скопировать:
create
next
cat
koshka
next
dog
sobaka
stop
- после уже можно пробовать вводить самому
{'cat': 'koshka', 'dog': 'sobaka'}
translaterus
sobaka
dog
task12
```python
def create(d):
    inp = input()
    while inp != 'stop':
        eng = input()
        rus = input()
        # d.update({eng: rus})
        d[eng] = rus
        inp = input()

#сначала сами должны заполнить словарь теми парами слов, которые хотим в нем иметь
dict = {}
i = input()
if i == 'create':
    create(dict)
    print(dict)
inp = input()
if inp == 'translateeng':
    eng = input()
    print(dict.get(eng))
if inp == 'translaterus':
    rus = input()
    for i in dict:
        if dict.get(i) == rus:
            print(i)

```
