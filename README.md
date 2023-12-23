# Лабораторная работа 5.
## Построение графиков в Python
### Уроки 1-3
![](1,1.png)
![](1,2.png)
![](1.3.png)
![](1.4.png)
![](1.5.png)
![](1.6.png)
![](1.8.png)
![](2.2.png)
![](2.2.1.png)
![](2.3.1.2.png)
![](2.3.1.png)
![](2.3.2.png)
![](2.3.3.1.png)
![](2.3.3.2.png)
![](2.4.1.png)
![](2.4.2.png)
![](3.1.1.png)
![](3.1.2.png)
![](3.1.3.png)
![](3.2.1.png)
![](3.2.2.png)
![](3.2.3.png)
![](3.3.png)
![](3.3.1.png)
![](3.3.2.png)
![](3.3.3.png)
![](3.3.4.png)
![](3.3.5.png)
![](3.3.6.png)
![](3.4.1.png)
![](3.4.2.png)
![](3.4.3.png)
![](3.5.1.png)
![](3.5.2.png)
### Задание
Выберите одну из неразрывных функции своего варианта из лабораторной работы №2, постройте график этой функции и касательную к ней. Добавьте на график заголовок, подписи осей, легенду, сетку.

```python
import math
import matplotlib.pyplot as plt
import numpy as np

def f(x):
    return np.sqrt(x + 1) - np.sqrt(x) - 0.5

def f_pr(x):
    return 0.5 / np.sqrt(x + 1) - 0.5 / np.sqrt(x)
def yk(t, x):
    for i in x:
        y1.append(f(t) + f_pr(t) * (i - t))
    return y1
tochka_kasaniya = 0.2
x = np.linspace(0,1,100)
y = []
for i in x:
    y.append(f(i))
x1 = [0.0, 1.0]
y1 =[]
plt.title('График') 
plt.xlabel('x') 
plt.ylabel('y') 
plt.grid()
plt.plot(x, y)
plt.plot(x1, yk(tochka_kasaniya, x1))
plt.plot(tochka_kasaniya, f(tochka_kasaniya), "ro")

plt.show()
```
### График
![](5.png)