# my solution to tasks-Python c курса  
### https://stepik.org/course/67/syllabus

#### Шахматная доска.  
Заданы две клетки шахматной доски. Если они покрашены в один цвет, то выведите слово YES, а если в разные цвета — то NO. Программа получает на вход четыре числа от 1 до 8 каждое, задающие номер столбца и номер строки сначала для первой клетки, потом для второй клетки.  
x1 = int(input())  
y1 = int(input())  
x2 = int(input())  
y2 = int(input())  
if (x1 + y1 + x2 + y2) % 2 == 0: print('YES')  
  else:  print('NO')  

#### Ход короля.
Шахматный король ходит по горизонтали, вертикали и диагонали, но только на 1 клетку. Даны две различные клетки шахматной доски, определите, может ли король попасть с первой клетки на вторую одним ходом. Программа получает на вход четыре числа от 1 до 8 каждое, задающие номер столбца и номер строки сначала для первой клетки, потом для второй клетки. Программа должна вывести YES, если из первой клетки ходом короля можно попасть во вторую или NO в противном случае.  
x1 = int(input())  
y1 = int(input())  
x2 = int(input())  
y2 = int(input())  
if abs(x1 - x2) <= 1 and abs(y1 - y2) <= 1: print('YES')  
  else:     print('NO')  
  
#### Шахматный слон ходит по диагонали.  
Даны две различные клетки шахматной доски, определите, может ли слон попасть с первой клетки на вторую одним ходом.  
x1 = int(input())  
y1 = int(input())  
x2 = int(input())  
y2 = int(input())  
if abs(x1 - x2) ==  abs(y1 - y2): print('YES')  
else:      print('NO')  

#### Шахматный ферзь ходит по диагонали, горизонтали или вертикали.  
Даны две различные клетки шахматной доски, определите, может ли ферзь попасть с первой клетки на вторую одним ходом.  
x1 = int(input())  
y1 = int(input())  
x2 = int(input())  
y2 = int(input())  
if (abs(x1 - x2) ==  abs(y1 - y2)) or (x1-x2==0) or (y1-y2==0): print('YES')  
else:   print('NO')  

#### Шахматный конь ходит буквой “Г” — на две клетки по вертикали в любом направлении и на одну клетку по горизонтали, или наоборот.   
Даны две различные клетки шахматной доски, определите, может ли конь попасть с первой клетки на вторую одним ходом.  
x1 = int(input())  
y1 = int(input())  
x2 = int(input())  
y2 = int(input())  
if (abs(x1 - x2) == 2 and abs(y1 - y2) == 1) or (abs(x1-x2) == 1 and abs(y1-y2) == 2):      print('YES')  
else:      print('NO')  

### Шоколадка имеет вид прямоугольника, разделенного на n×m долек. Шоколадку можно один раз разломить по прямой на две части.  
Определите, можно ли таким образом отломить от шоколадки часть, состоящую ровно из k долек. Программа получает на вход три числа: n, m, k и должна вывести YES или NO.
n = int(input())
m = int(input())
k = int(input())
if k < n * m and ((k % n == 0) or (k % m == 0)):
    print('YES')
else:
    print('NO')
    
    
#### Дано натуральное число. Выведите его последнюю цифру.  
a = int(input())  
print(a % 10)  

#### МКАД   
Длина Московской кольцевой автомобильной дороги —109 километров. Байкер Вася стартует с нулевого километра МКАД и едет со скоростью vv километров в час. На какой отметке он остановится через tt часов?  
Программа получает на вход значение vv и tt. Если v>0v>0, то Вася движется в положительном направлении по МКАД, если же значение v<0v<0, то в отрицательном.  
Программа должна вывести целое число от 0 до 108 — номер отметки, на которой остановится Вася.  
a = int(input())  
b = int(input())  
print((a * b) % 109)  

#### Первая цифра после точки  
Дано положительное действительное число X. Выведите его первую цифру после десятичной точки.  
x = float(input())  
print(int(x * 10) % 10)  

#### Конец уроков.  
В некоторой школе занятия начинаются в 9:00. Продолжительность урока — 45 минут, после 1-го, 3-го, 5-го и т.д. уроков перемена 5 минут, а после 2-го, 4-го, 6-го и т.д. — 15 минут.  
Дан номер урока (число от 1 до 10). Определите, когда заканчивается указанный урок.  
Выведите два целых числа: время окончания урока в часах и минутах.  
a = int(input())  
a = a*45 + (a//2)*5 + ((a+1)//2-1)*15  
print(a//60 + 9, a%60)  

#### За день машина проезжает n километров. Сколько дней нужно, чтобы проехать маршрут длиной m километров?  
Программа получает на вход числа n и m.  
from math import ceil    #ceil –округление вверх  
n = int(input())  
m = int(input())  
print(ceil(m / n))  

### Стоимость покупки  
Пирожок в столовой стоит a рублей и b копеек. Определите, сколько рублей и копеек нужно заплатить за n пирожков. Программа получает на вход три числа: a, b, n, и должна вывести два числа: стоимость покупки в рублях и копейках.  
a = int(input())  
b = int(input())  
n = int(input())  
cost = n * (100 * a + b)  
print(cost // 100, cost % 100)  

#### Разность времени  
Даны значения двух моментов времени, принадлежащих одним и тем же суткам: часы, минуты и секунды для каждого из моментов времени. Известно, что второй момент времени наступил не раньше первого. Определите, сколько секунд прошло между двумя моментами времени.  
Программа на вход получает три целых числа: часы, минуты, секунды, задающие первый момент времени и три целых числа, задающих второй момент времени.  
Выведите число секунд между этими моментами времени.  
a = int(input())  
b = int(input())  
c = int(input())  
x = int(input())  
y = int(input())  
z = int(input())  
print((x-a)*3600 + (y-b)*60 + z - c)  
a1 = int(input())  
b1 = int(input())  
c1= int(input())  
a2 = int(input())  
b2 = int(input())  
c2= int(input())  
a=abs(a1-a2)  
if b1<=b2:  
    b=b2-b1  
else:  
    b=60-b1+b2  
     a-=1  
if c1<=c2:  
     c=c2-c1  
 else: 
 c=60-c1+c2  
     b-=1  
print(a*3600+b*60+c)  

#### Улитка  
Улитка ползет по вертикальному шесту высотой hh метров, поднимаясь за день на aa метров, а за ночь спускаясь на bb метров. На какой день улитка доползет до вершины шеста?  
Программа получает на вход натуральные числа hh, aa, bb.  
Программа должна вывести одно натуральное число. Гарантируется, что a>ba>b.  
import math  
h = int(input())  
a = int(input())  
b = int(input())  
n=(h-b)/(a-b)  
x=math.ceil(n)  
print(x)  


#### Разработчики:
h = int(input())  
a = int(input())  
b = int(input())  
print(int((h - a - 1) // (a - b) + 2))  


#### Число десятков  
Дано натуральное число. Найдите число десятков в его десятичной записи.  
a=int(input())  
print(a//10%10)  

#### Сумма цифр  
Дано трехзначное число. Найдите сумму его цифр.  
n = int(input())  
a = n // 100  
b = n // 10 % 10  
c = n % 10  
print(a + b + c)  

#### Часы  
С начала суток прошло H часов, M минут, S секунд (0 ≤ H < 12, 0 ≤ M < 60, 0 ≤ S < 60). По данным числам H, M, S определите угол (в градусах), на который повернулаcь часовая стрелка с начала суток и выведите его в виде действительного числа.  
h = int(input())  
m = int(input())  
s = int(input())  
print(h * 30 + m * 30 / 60 + s * 30 / 3600)  

мое:  
H = int(input())  
M = int(input())  
S = int(input())  
HMS = H*3600+M*60+S  
proz = HMS/432  
a=360*proz/100  
print(a)  

#### Часы 2  
С начала суток часовая стрелка повернулась на угол в α градусов. Определите на какой угол повернулась минутная стрелка с начала последнего часа. Входные и выходные данные — действительные числа.  
alpha = float(input())  
print(alpha % 30 * 12)  

мое:   
a = float(input())  
ch=a*12/360 #часов прошло  
m =ch*60 # минут прошло  
m1 = m%60 #остаток минут от часа  
b=m1*360/60 #% угла от 360градусов  
print(b)  

#### Проценты  
Процентная ставка по вкладу составляет P процентов годовых, которые прибавляются к сумме вклада. Вклад составляет X рублей Y копеек. Определите размер вклада через год.
Программа получает на вход целые числа P, X, Y и должна вывести два числа: величину вклада через год в рублях и копейках. Дробная часть копеек отбрасывается.  
p = int(input())  
x = int(input())  
y = int(input())  
money_before = 100 * x + y  
money_after = int(money_before * (100 + p) / 100)  
print(money_after // 100, money_after % 100)  

мое:  
X = int(input())  
Y = int(input())  
Y=Y/100  
XY=X+Y   
procent=XY*P/100 #процент от Р  
V=XY+procent  
print(int(V), int(V*100%100))  


#### Даны два целых числа A и В, A>BA>B.   
Выведите все нечётные числа от A до B включительно, в порядке убывания. В этой задаче можно обойтись без инструкции if.  
a = int(input())  
b = int(input())  
for i in range(a, b-1, -1):  
    if i%2 == 1:  
            print(i, end=' ')  
            
            
#### Сумма 10 чисел  
Дано 10 целых чисел. Вычислите их сумму. Напишите программу, использующую наименьшее число переменных.  
S=0  
for i in range(10):  
    a=int(input())  
        S+=a  
        print(S)  
        

#### Количество нулей  
Дано N чисел: сначала вводится число N, затем вводится ровно N целых чисел. Подсчитайте количество нулей среди введенных чисел и выведите это количество. Вам нужно подсчитать количество чисел, равных нулю, а не количество цифр.  
num_zeroes = 0  
for i in range(int(input())):  
    if int(input()) == 0:  
            num_zeroes += 1  
    print(num_zeroes)  
    

#### Лесенка  
По данному натуральному n ≤ 9 выведите лесенку из n ступенек, i-я ступенька состоит из чисел от 1 до i без пробелов.  
n = int(input())  
for i in range(1, n+1):  
    for i in range(1, i+1):  
            print(i, end='')  
    print()  
1
12  
123  


#### Потерянная карточка  
Для настольной игры используются карточки с номерами от 1 до N. Одна карточка потерялась. Найдите ее, зная номера оставшихся карточек.  
Дано число N, далее N − 1 номер оставшихся карточек (различные числа от 1 до N). Программа должна вывести номер потерянной карточки.   
Для самых умных: массивами и аналогичными структурами данных пользоваться нельзя  
n = int(input())  
sum = 0  
for i in range(1, n + 1):  
    sum += i  
 можно доказать формулу: sum == n * (n + 1) // 2но мы посчитаем это значение циклом  
for i in range(n - 1):  
    sum -= int(input())  
    print(sum)  
    
мое:  
n = int(input())  
a = ''  
b = ''  
for i in range(1, n):  
    number = input()  
        a+=number  
for i in range(1, n+1):  
            b+=str(i)  
for i in range(len(b)):  
    if b[i] not in a:  
            print(b[i])  
    

