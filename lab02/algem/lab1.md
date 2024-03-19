<h2 style="text-align: center;">Бюджетное учреждение высшего образования Ханты-Мансийского автономного округа – Югры</h2>

<h1 style="text-align: center;">«СУРГУТСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<h2 style="text-align: center;">Политехнический институт</h2>

<p style="text-align: center;">Кафедра прикладной математики</p>

<p style="text-align: center;">Миронов Роман Алексеевич</p>

<h1 style="text-align: center;">Индивидуальное задание №1</h1>

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
![image](https://github.com/zbtka/web/assets/144006033/f6e6fc9b-dc77-4330-b64f-4f5ceb7e37eb)


#### Программное решение 1

```python
import numpy as np

# матрица
A = np.array([[4, -1, 7], [0, 1, -2], [0, 0, 9]])
B = np.array([[-1, 1, 0], [0, 0, 3], [6, 2, -1]])
C = np.array([[5, 1, 1], [1, 5, 1], [1, 1, 5]])

# считаем B и А
B_T = np.transpose(B)
A_T = np.transpose(A)

# вычисления
term1 = np.add(A, 3*B_T)
term2 = 3*A_T - B

product = np.dot(term1, term2)

# решаем уравнение
X = np.linalg.solve(product, C)
# проверка
equation = np.dot(np.dot((A+3*B_T), (3*A_T-B)), X)
print(np.allclose(equation, C))
print("\nитог:")
print(X)
```

#### Результат 1

![image](https://github.com/zbtka/web/assets/144006033/4b0bd527-bdeb-4c6a-8616-8d020bfd69af)

#### Задание 2

![image](https://github.com/zbtka/web/assets/144006033/268e0ff5-0905-4c94-ac5d-27f3eb36d0db)

#### Программное решение 2

```python
import numpy as np

# матрица
A = np.array([[-1, 2, -4], [1, -1, 7], [-1, 0, 0]])
B = np.array([[1, 0, 0], [0, 2, 0], [1, 0, 3]])
C = np.array([[3, 8, -1], [0, 8, 0], [2, -1, 3]])

# Вычисления
term1 = np.dot(np.dot(A, A), B)
term2 = np.dot(np.dot(B, B), np.dot(B, A))
result = np.transpose(term1 + term2)

# решаем уравнение
X = np.linalg.solve(result, np.dot(B, C))

print(X)

# проверка, если верно - True
equation = np.dot(np.transpose(term1 + term2), X)
print(np.allclose(equation, np.dot(B, C)))  
print("\nитог:")
print(X)
```

#### Результат 2

![image](https://github.com/zbtka/web/assets/144006033/d9ff2d49-d585-40ab-9885-58a4e0dee4f1)


#### Задание 3

![image](https://github.com/zbtka/web/assets/144006033/ba0edadd-3a32-4b6b-a760-66ea233c535a)

#### Программное решение 3

```python
import numpy as np
#матрица
A = np.array([[2, -1, -1], [0, 2, -1], [0, 0, -1]])
B = np.array([[-1, 0, 0], [1, -3, 0], [1, 1, -5]])

#вычисления
A_cubed = np.linalg.matrix_power(A, 3)
A_squared = np.linalg.matrix_power(A, 2)

expression = A_cubed - 2 * A_squared + 3 * A
B_squared = np.linalg.matrix_power(B, 2)
result = 4 * B_squared - B

#транспонированное выражение
expression_transpose = expression.T


#считаем уравнение
X = np.linalg.solve(expression_transpose, result)

print(X)

```

#### Результат 3

![image](https://github.com/zbtka/web/assets/144006033/cc24cad0-f730-4d14-9ff4-4783d438c07f)

