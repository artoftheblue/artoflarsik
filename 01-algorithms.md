# Квадратичные формы

## 1. Построение матрицы квадратичной формы

1. **Заполняем главную диагональ:**
   Коэффициент перед $x_i^2$ записываем на место $i$-й строки $i$-го столбца.
2. **Остальные элементы:**
   Коэффициент перед $x_{ij}$ делим на $2$ и записываем в $i$-ю строку, $j$-й столбец и в $j$-ю строку, $i$-й столбец.

:::{warning} Важно!
Коэффициент при $x_{ij}$ равен коэффициенту при $x_{ji}$.
:::

## 2. Восстановление квадратичной формы по матрице

1. Элементы в $i$-й строке $i$-м столбце (на главной диагонали) будут коэффициентацми перед соотвествующими $x_i^2$.
2. Элементы на $i$-м $j$-м месте умножаем на $2$. Они будут коэффициентами перед $x_{ij}$.

:::{warning} Важно!
Коэффициенты при $x_{ji}$ выписывать не нужно, потому что они уже были учтены умножением на $2$.
:::

## 3. Знакоопределённость квадратичной формы

1. Находим матрицу квадратичной формы.
2. Находим все угловые миноры $\delta_1,\delta_2,\dots,\delta_n$.
3. * Если $\forall i\colon 1\leqslant i \leqslant n$ все $\delta_i>0$, то квадратичная форма положительно определена.
   * Если

## 4. Приведение формы к нормальному виду

### Метод угловых миноров

1. Ищем матрицу квадратичной формы.
2. Ищем угловые миноры $\delta_1,\delta_2,\dots,\delta_n$
3. * $\delta_1$ это коэффициент перед $x_1^2$;
   * $\displaystyle\frac{\delta_2}{\delta_1}$ это коэффициент перед $x_2^2$;
   * и так далее

Нормальный вид:

$$\delta_1x_1^2+\frac{\delta_1}{\delta_2}x_2^2+\frac{\delta_3}{\delta_2}x_3^2+\dots+\frac{\delta_n}{\delta_{n-1}x_n^2}$$

### Симметричный Гаусс

Главное правило: если мы выполняем какую-то операцию с $i$ и $j$ строкой (или умножаем на $\lambda$ $i$-ю строку), то следующим шагом мы должны сделать то же самое с $i$ и $j$ столбцом (соответственно, с $i$-м столбцом).

:::{prf:example} Пример
$$\begin{pmatrix}
    1 & 4\\
    4 & 6
\end{pmatrix}\mapsto\begin{pmatrix}
    1 & 4\\
    0 & -6
\end{pmatrix}\mapsto\begin{pmatrix}
    1 & 0\\
    0 & -6
\end{pmatrix}$$

1. Прибавляем ко второй строке первую, умноженную на $-4$.
2. Прибавляем ко второму столбцу 1-й, умноженный на $-4$.
3. Ура, матрица теперь диагональна.
:::

## 5. Нахождение матрицы перехода к системе координат, в которых квадратичная форма имеет канонический вид

1. Пусть $Q$ – квадратичная форма. Найдём её матрицу $A$.
2. Запишем матрицу $B$ – векторы-базисы в столбцы.
3. Запишем расширенную матрицу следующим образом:

$$\begin{pmatrix}
   A \bigm | C
\end{pmatrix}$$

4. Приведём матрицу $A$ к диагональному виду, используя симметричный метод Гаусса.

:::{warning} Важно
Элементарные преобразования строк **касаются** и матрицы $C$. А вот преобразования столбцов – нет!
:::

## 6. Ортогонализация базиса

Дан базис $e: (e_1, e_2 ... e_n)$. Необходимо сделать из него ортогональный базис $(f_1, ... f_n)$.

### Решение.

Положим, $e_1 = f_1$. Остальные векторы $f_i$ будем достраивать по следующей формуле:
$$f_{k + 1} = e_{k + 1} - \sum_{i = 1}^{k}{\lambda _if_i},$$
где $\lambda_i = \frac{e_{k + 1}, f_i}{f_i, f_i}$ и $(v, w)$ - скалярное произведение любых двух векторов $v$ и $w$.

К примеру, $f_{2} = e_2 - \frac{e_2, f_1}{f_1, f_1}$

## 7. Проверка матрицы Грама на предмет соответствия системе векторов

Дана матрица $A  \in M_2(\mathbb{R})$. Необоходимо узнать, является ли она матрицей Грама какой-нибудь из систем векторов, и, если да - предъявить эту систему.

1. Проверим матрицу на симметричность: $\forall x_{ij}: x_{ij} = x_{ji}$. Если матрица не симметрична, ответ на поставенный в задаче вопрос - "нет"
2. Используя симметричный метод Гаусса (см. алгоритм 5), приведём расширенную матрицу $A\mid E$ к диагональному виду $D\mid B$, где $D$ - диагональная матрица, $B$ - результат преобразований матрицы $E$.

**! Важно:** операции, выполняемые со столбцами, выполняем только для матрицы $A$! Ниже будет показан пример того, как это делается.

3. Матрица $B$ - транспонированнакя матрица $C$, иными словами, $B = C^T$
4. Обозначим элементы, стоящие на $ii$ месте в получившейся диагональной матрице $D$, как $d_i$. Найдём векторы нового базиса по формуле $f_i = \sqrt{d_i}e_i$, где $e_i$ - векторы стандартного базиса.
5. Найдём искомую систему векторов по формуле $(v_1, v_2 ... v_n) = (f_1, f_2 ... f_n)*C^{-1}$

Пример того, как привести расширенную матрицу к диагональному виду:

Положим, $A = \begin {pmatrix}
1 & 4\\
4 & 6 
\end{pmatrix}
$. Тогда $A \mid E = \begin {pmatrix}
1 & 4 & \bigm| & 1 & 0\\
4 & 6 & \bigm| & 0 & 1
\end{pmatrix}\implies$ ко **всей** второй строке прибавляем первую, умноженную на (-4) $\implies\begin {pmatrix}
1 & 4 & \bigm| & 1 & 0\\
0 & -10 & \bigm| & -4 & 1
\end{pmatrix}\implies$ теперь, поскольку алгоритм - симметричный, ко второму столбцу тоже прибавляем первый, умноженный на (-4), однако эту операцию проделываем лишь для матрицы $A \implies$ $\begin {pmatrix}
1 & 0 & \bigm| & 1 & 0\\
0 & -10 & \bigm| & -4 & 1
\end{pmatrix}$
Заметим, матрица справа никак не меняется после преобразования столбцов. Эта матрица справа - и есть искомая матрица $B$

## 8. Вычисление ортогональной проекции вектора.

### Способ 1.
 **Условие:** дан вектор $v$ и ортогональный базис $e$ в подпространствe $S$. Важно: именно ортогональный - иначе необходимо привести его к виду ортогонального, воспользовавшись алгоритмом 6.

**Найти:** ортогональную проекцию вектора $v$ на $S$.

### Решение.

Посчитаем проекцию по формуле: $$pr_S v = \sum_{i = 1}^{k}{\frac{v, e_i}{e_i, e_i}}e_i$$

### Способ 2.

**Условие:** дан вектор $v$ в пространстве $\mathbb{E} = \mathbb{R^n}$ со стандартным скалярным произведением и *любой* базис $F$ в подпространствe $S$.

**Найти:** ортогональную проекцию вектора $v$ на $S$.

### Решение.

1. Запишем базисные векторы $f_1, ... f_n$ в столбцы матрицы - получим матрицу $A$.
2. Вычислим ортогональную проекцию по формуле:
$$pr_S v = A(A^TA)^{1}A * v$$

## 9. Переопределение системы уравнений.

Дана система линейных уравнений $Ax = b$ $(A \in M_{m*n}; m > n)$ , не имеющая решения. Необходимо найти решение так называемой *переопределённой системы уравнений*.

### Решение.

Воспользуемся формулой $x = (A^T A)^{-1}A^Tb$

## 10. Поиск векторного произведения в $\mathbb{R^3}$

Даны два вектора $a$, $b \in \mathbb{R}^3$ и базис $e$ в $\mathbb{R}^3$. Найти векторное произведение $[a, b]$ в базисе $e$.

### Решение.

1. Составим матрицу $A_i$, записав в первый столбец координаты вектора $a = (a_1, a_2, a_3)$, во второй - координаты вектора $b = (b_1, b_2, b_3)$, а в третий - координаты базисного вектора $e_i = (e_{i1}, e_{i2}, e_{i3})$:

$$\begin {pmatrix}
a_1 & b_1 & e_{i1}\\
a_2 & b_2 & e_{i2}\\
a_3 & b_3 & e_{i3}\\
\end{pmatrix}$$

2. Определитель $det A_i$ - это $i$-я координата вектора $c = [a, b]$. Таким образом посчитаем все координаты, найдя определители всех возможных матриц $A_i$.

**Например,** для нахождения первой координаты найдём определитель матрицы $A_1$, в первый столбец которой записаны координаты вектора $a$, во второй - координаты вектора $b$, а в третий - координаты базисного вектора $e_1$.