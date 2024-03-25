<h2 style="text-align: center;">Бюджетное учреждение высшего образования Ханты-Мансийского автономного округа – Югры</h2>

<h1 style="text-align: center;">«СУРГУТСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<h2 style="text-align: center;">Политехнический институт</h2>

<p style="text-align: center;">Кафедра прикладной математики</p>

<p style="text-align: center;">Миронов Роман Алексеевич</p>

<h1 style="text-align: center;">Индивидуальное задание №2</h1>

<p style="text-align: center;">Дисциплина «Алгебра и геометрия»</p>

<p style="text-align: center;">направление 01.03.02 «Прикладная математика и информатика»</p>

<p style="text-align: center;">направленность (профиль): «Технологии программирования и анализ данных»</p>

<pre>

</pre>

<p style="text-align: right;">Преподаватель: Шапошникова Ирина Вадимовна  </p>

<p style="text-align: right;">Доцент</p>

<p style="text-align: right;">Студент гр. № 601-31</p>

<p style="text-align: right;">Миронов Роман Алексеевич</p>

<pre>

</pre>

<p style="text-align: center;">Сургут 2024 г.</p>

#### Задание 1

![image](https://github.com/zbtka/web/assets/144006033/0085c7c4-887b-477b-be88-721d838da565)

#### Программное решение 1

```python
# c помощью solve
import numpy as np
# задаём матрицу А
A = np.array([[1, 2, -1],
              [2, -3, 1],
              [1, 1, -1]])

# вектор правой части уравнения
B = np.array([7, 3, 16])

# решаем с помощью solve
X = np.linalg.solve(A, B)

# вывод ответа с solve
print("Ответ с функцией solve:")
print("x1 =", X[0])
print("x2 =", X[1])
print("x3 =", X[2])



# решение при помощи метода Крамера
import numpy as np

# задаём матрицу А
A = np.array([[1, 2, -1],
              [2, -3, 1],
              [1, 1, -1]])

# вектор правой части уравнений
B = np.array([7, 3, 16])

# инициализация решения
X = np.zeros(3)

# нахождение определителя матрицы 
detA = np.linalg.det(A)

# вычисление определителя для неизвестных
for i in range(3):
 
 A[:, i] = B
 
 # вычисление определителя новой матрицы
 detAi = np.linalg.det(A)
 
 # Вычисляем i-ую неизвестную
 X[i] = detAi / detA
 
 A = np.array([[1, 2, -1],
               [2, -3, 1],
               [1, 1, -1]])
# Ответ при решении методом Крамера
print("ответ с использованием метода Крамера:")
print("x1 =", X[0])
print("x2 =", X[1])
print("x3 =", X[2])
```

#### Результат 1

![image](https://github.com/zbtka/web/assets/144006033/94fd13ef-a1ad-4473-8b7a-2f1274969b02)

#### Задание 2

![image](https://github.com/zbtka/web/assets/144006033/3e6ab8c3-2a76-47a0-89d8-9e26d1691a42)

#### Программное решение 2

```python
# c помощью solve
import numpy as np

# задаем матрицу коэффицентов
A = np.array([[1, 1, 1, 1, 1],
 [0, 2, 1, 1, 1],
 [0, 0, 3, 1, 1],
 [0, 0, 0, 4, 1],
 [0, 0, 0, 0, 5]])

# вектор правой части уравнений
B = np.array([5, 4, 3, 2, 1])

# решаем с помощью solve
X = np.linalg.solve(A, B)

# вывод ответа с solve
print("Ответ с функцией solve:")
for i in range(len(X)):
 print("x" + str(i+1) + " =", X[i])


# при помощи обратного хода метода Гаусса.
import numpy as np

# задаем матрицу коэффицентов
A = np.array([[1, 1, 1, 1, 1],
 [0, 2, 1, 1, 1],
 [0, 0, 3, 1, 1],
 [0, 0, 0, 4, 1],
 [0, 0, 0, 0, 5]])

# вектор правой части уравнений
B = np.array([5, 4, 3, 2, 1])

# решение с обратным ходом метода Гаусса
X = np.linalg.inv(A).dot(B)

# Ответ при решении обратным ходом метода Гаусса
print("Решение с использованием метода обратного хода метода Гаусса:")
for i in range(len(X)):
 print("x" + str(i+1) + " =", X[i])
```

#### Результат 2

![image](https://github.com/zbtka/web/assets/144006033/481f30d5-3aec-4522-adb3-c5dbc1b909db)

#### Задание 3

![image](https://github.com/zbtka/web/assets/144006033/441cf700-5f16-4015-bd54-d8cc2f0123a7)

#### Программное решение 3

```python
# c помощью solve
import numpy as np
# задаем матрицу коэффицентов
A = np.array([[1, 1, 1, 1, 5],
 [1, 1, 1, 5, 0],
 [1, 1, 5, 0, 0],
 [1, 5, 0, 0, 0],
 [5, 0, 0, 0, 0]])

# вектор правой части уравнений
B = np.array([1, 1, 1, 1, 1])

# решаем с полмощью solve
X = np.linalg.solve(A, B)

# вывод ответа с solve
print("Решение с использованием функции solve:")
for i in range(len(X)):
 print("x" + str(i+1) + " =", X[i])
```

```python
# решение при помощи метода исключения переменных
import numpy as np
# задаем матрицу коэффицентов
A = np.array([[1, 1, 1, 1, 5],
 [1, 1, 1, 5, 0],
 [1, 1, 5, 0, 0],
 [1, 5, 0, 0, 0],
 [5, 0, 0, 0, 0]])

# вектор правой части уравнений
B = np.array([1, 1, 1, 1, 1])

# решаем с полмощью solve
X = np.linalg.solve(A, B)

# вывод ответа с solve
print("Решение с использованием функции solve:")
for i in range(len(X)):
 print("x" + str(i+1) + " =", X[i])
```
#### Результат 3

![image](https://github.com/zbtka/web/assets/144006033/4bb260f4-5a22-4d0b-a040-768c1a86c8a1)








