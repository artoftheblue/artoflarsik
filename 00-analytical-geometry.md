# Линейные операторы и аналитическая геометрия

## 1. Составление уравнения прямой по имеющимся двум точкам:

Дано: две точки $A(x_0, y_0, z_0)$ и $B(x_1, y_1, z_1)$. Необходимо построить каноническое уравнение прямой

Решение: подставляем соответствующие координаты в формулу 
$$\frac{x - x_0}{x_1 - x_0} = \frac{y - y_0}{y_1 - y_0} = \frac{z - z_0}{z_1 - z_0}$$

и получаем ответ (как и в двумерном случае, только на этот раз равенства два).

## 2. Переход от канонического вида прямой к параметрическому

Дано: каноническое уравнение прямой вида
$$\frac{x - a_0}{a} = \frac{y - b_0}{b} = \frac{z - c_0}{c}$$

Необходимо: записать параметрическое уравнение.

**Решение:** 

1. Найдём любую точку, принадлежащую прямой. Это можно сделать так: выбираем любое число - например, $k$, и по очереди приравниваем каждую дробь к этому числу, решая систему уравнений:
$$\begin {equation*}
\begin{cases}
\frac{x - a_0}{a} = k,
\\
\frac{x - b_0}{b} = k,
\\
\frac{x - c_0}{c} = k
\end{cases}
\end {equation*}
$$

Получим $(x_1, y_1, z_1)$ 

2. $a, b$ и $c$ в знаменателях уравнения - координаты векторов нормали.
3. Составляем параметрическое уравнение по следующей схеме:
$$\begin {equation*}
\begin{cases}
x = at + x_1,
\\
y = bt + y_1,
\\
z = ct + z_1
\end{cases}
\end {equation*}
$$

## 3. Построение прямой $l_1$ в $R^3$, проходящей через данную точку $A(x_1, y_1, z_1)$ и параллельную прямой $l_2$

**Решение:** знаем, что у параллельных прямых *один и тот же вектор нормали.*

1. Если прямая $l_1$ задана параметрически, коэффиценты перед параметром в соответствующих уравнениях - и есть координаты вектора нормали. То есть, если параметрически прямая задана как

$$\begin {equation*}
\begin{cases}
x = at + x_0,
\\
y = bt + y_0,
\\
z = ct + z_0
\end{cases}
\end {equation*}
$$

, $(a, b, c)$ - координаты вектора нормали.

2. Если же прямая $l_2$ задана в каноническом виде, координаты вектора нормали - знаменатели каждой из дробей. То есть, если канонически прямая задана как

$$\frac{x - a_0}{a} = \frac{y - b_0}{b} = \frac{z - c_0}{c}$$

, $(a, b, c)$ - координаты вектора нормали.

3. Теперь запишем само уравнение: в параметрическом виде оно выглядит как

$$\begin {equation*}
\begin{cases}
x = at + x_0,
\\
y = bt + y_0,
\\
z = ct + z_0
\end{cases}
\end {equation*}
$$
, где $x_1, y_1, z_1$ - координаты точки $A$. А то, как перейти от параметрического вида к каноническому, мы уже знаем.
   
## 4. Построение плоскости, проходящей через данную точку $A(x_1, y_1, z_1)$ и параллельную данной плоскости

**Дано:** уравнение плоскости $\alpha: A_1x+ B_1y + C_1z + D_1 = 0$ и точка $A(x_1, y_1, z_1)$. Необходимо построить плоскость $\beta$, проходящую через точку $A$ и параллельную плоскости $\alpha$

**Решение:**
1. Вектор нормали у параллельных плоскостей один. Соответственно, из уравнения $A_1x+ B_1y + C_1z + D_1 = 0$ можем получить $(A_1, B_1, C_1)$ - его координаты.
2. Подставим координаты точки $A(x_1, y_1, z_1)$ в уравнение

$$A_1(x - x_1) + B_1(y - y_1) + C_1(z - z_1) = 0$$
, приводим подобные слагаемые - и получаем уравнение нужной нам плоскости $\beta$.

**? Почему этот метод работает?** Для того, чтобы плоскости были параллельны, система

$$\begin {equation*}
\begin{cases}
A_1x+ B_1y + C_1z + D_1 = 0,
\\
A_1(x - x_1) + B_1(y - y_1) + C_1(z - z_1) = 0
\end{cases}
\end {equation*}
$$

должна быть несовместной - иными словами, у плоскостей не должно найтись ни одной общей точки.
Посмотрим на данную нам систему: поскольку $A_1x_1, B_1y_1$ и $C_1z_1$ - числа, второе уравнение в системе может принять вид:

$$A_1x+ B_1y + C_1z + (A_1x_1 + B_1y_1 + C_1z_1) = 0$$

А значит, если последнее слагаемое в левой части этого уравнения не равно $D_1$, после приведения системы

$$\begin {equation*}
\begin{cases}
A_1x+ B_1y + C_1z + D_1 = 0,
\\
A_1x+ B_1y + C_1z + (A_1x_1 + B_1y_1 + C_1z_1) = 0
\end{cases}
\end {equation*}
$$

к ступенчатому виду, получим $D_1 - (A_1x_1 + B_1y_1 + C_1z_1) = 0$ - что означает несовместность всей системы, учитывая указанное ранее неравенство.

## 5. Нахождение координат точки пересечения прямой и плоскости:

**Дано:** прямая $l$, заданная параметрически, и плоскости $\alpha$, заданная уравнением $A_1x+ B_1y + C_1z + D_1 = 0$. Необходимо найти точку пересечения прямой и плоскости.

**Решение.** Параметрический вид прямой имеет вид:

$$\begin {equation*}
\begin{cases}
x = at + x_0,
\\
y = bt + y_0,
\\
z = ct + z_0
\end{cases}
\end {equation*}
$$

Подставим в уравнение плоскости каждую координату, заданную через $t$, получив уравнение:

$$A_1(at + x_0) + B_1(bt + y_0) + C_1(ct + z_0) + D_1 = 0$$

с одной переменной $t$. Решим его и подставим найденное значение $t_0$ в каждую из координат, заданную в уравнении прямой. Тогда точка $A(at_0 + x_0, bt_0 + y_0, ct_0 + z_0)$ - и есть искомая точка пересечения.

## Линейные операторы.

## 1. Нахождение собственных значений и базисов собственных пространств линейного оператора

Дано: матрица линейного оператора $\varphi$ (рассмотрим на примере трёхмерного пространства):

$$A = \begin {pmatrix}
a_1 & b_1 & с_1\\
a_2 & b_2 & с_{2}\\
a_3 & b_3 & с_{3}\\
\end{pmatrix}$$

### Нахождение собственных значений:

**! Напоминание:** *собственные значения линейного оператора - такие числа $\lambda$, для которых выполняется $\varphi(v) = \lambda v$, где $v$ - вектор, принадлежащий пространству, на котором определён линейный оператор, $\varphi(v)$ - его образ в этом линейном оператор, $\lambda$ - какой-то из скаляров.*

Ищем корни характеристического многочлена: это определитель такой матрицы:

$$A(t) = \begin {pmatrix}
a_1 - t & b_1 & с_1\\
a_2 & b_2 - t & с_{2}\\
a_3 & b_3 & с_{3} - t\\
\end{pmatrix}$$

- то есть, из всех элементов на главной диагонали мы вычитаем $t$ - переменную в уравнении, корни которого нам нужны.

Приравниваем $det (A(t))$ к $0$ и ищем все действительные (если, конечно, работаем в $R^n$) корни - это и есть все собственные значения! Обозначим каждое как $\lambda_i$.

### Нахождение базисных векторов собственных подпространств:

У нас есть полученные в предыдущем пункте $\lambda_i$ - собственные значения.

**! Напоминание:** *собственные подпространства линейного оператора, отвечающие собственному значению $\lambda$ - это множество всех векторов, для которых верно: $\varphi(v) = \lambda v$*

Теперь для каждого из найденных $\lambda_i$ необходимо найти ФСР ОСЛУ, заданной такой матрицей:

$$A(\lambda_i) = A - \lambda_i E = \begin {pmatrix}
a_1 & b_1 & с_1\\
a_2 & b_2 & с_{2}\\
a_3 & b_3 & с_{3}\\
\end{pmatrix} - \lambda_i E \ = \begin {pmatrix}
a_1 - \lambda_i & b_1 & с_1\\
a_2 & b_2 - \lambda_i & с_{2}\\
a_3 & b_3 & с_{3} - \lambda_i\\
\end{pmatrix}$$

- ФСР для матрицы $A(\lambda_i)$ и будет базисом собственного подпространства, отвечающего этому значению $\lambda_i$

## 2. Нахождение базиса, в котором линейный оператор имеет диагональный вид, если матрица оператора симметрична 

Дано: симметричная матрица линейного оператора $\varphi$ (снова используем $R^3$ как пример):

$$A = \begin {pmatrix}
a_1 & b_1 & с_1\\
b_1 & b_2 & с_{2}\\
с_1 & с_{2} & с_{3}\\
\end{pmatrix}$$

Необходимо найти базис, в котором матрица оператора $\varphi$ принимает диагональный вид.

### Решение:

**Шаг 1.** Ищем корни характеристического многочлена $\varphi$ (алгоритм 1)

**Шаг 2.** Проверяем количество получившихся действительных корней. Если их число меньше размерности пространства, в котором определён линейный оператор - к диагональному виду матрицу оператора привести нельзя.

**Шаг 3.** В ином случае число получившихся корней (они же - собственные значения $\lambda_i$) равно размерности пространства, в котором определён оператор (больше получиться не может - степень характеристического многочлена не превосходит размерности пространства). Для каждого из $\lambda_i$ ищем базис собственного подпространства (алгорим 1).

**!** В каждой ФСР должен содержаться *лишь один* базисный вектор $v_i$

**Шаг 4.** Объединение этих базисов и даёт базис подпространства, в котором матрица линейного оператора имеет диагональный вид. На главной диагонали в такой матрице будут стоять все собственные значения - то есть, она примет следующий вид:

$$A = \begin {pmatrix}
\lambda_1 & 0 & 0\\
0 & \lambda_2 & 0\\
0 & 0 & \lambda_3\\
\end{pmatrix}$$

**!** *Собственные подпространства, отвечающие разным значениям, не просто попарно линейно независимы, но и попарно ортогональны - значит, объединять три базиса в одну систему точно можно*

## 3. Определение канонического вида, к которому квадратичная форма приводится ортогональным преобразованием

Дано: квадратичная форма вида $Q(x_1 x_2, x_3) = a_1x_1^2 + a_2x_2^2 + a_3x_3^2 + b_1x_1x_2 + b_2x_1x_3 + b_3x_2x_3$. 

Необходимо найти канонический вид, к которому форма приводится ортогональным преобразованием, базис, в котором она принимает канонический вид и замену координат (выражение старых координат через новые).

### Решение.

**Шаг 1.** Выписываем матрицу квадратичной формы (алгоритм (сделай ссылку, пожалуйста, поскольку вы видите тут эту надпись - Артемис не читает алгоритмы перед тем, как их закинуть))

**Шаг 2.** *Поскольку для любой квадратичной формы существует ортонормированный базис, в котором квадратичная форма имеет канонический вид - более того, этот вид определяется однозначно - далее решение сводится к поиску базисов, в которых выписанная в шаге 1 матрица имеет диагональный вид.* Иными словами, выполняем для матрицы квадратичной формы алгоритм 2.

**Шаг 3.** Ортонормируем получившийся базис $v_1, v_2, v_3$ - для этого поделим каждый из векторов на его норму.

**Шаг 4.** Выпишем само ортогональное преобразование (выражение новых базисных векторов через старые). Для этого найдём матрицу $C$ - матрицу перехода от старого базиса к новому (в нашем случае - от стандартного к найденному - здесь столбцами матрицы $C$ будут векторы нового базиса). 

Теперь решим уравнение $Cx = x'$ - то есть, умножим $C^{-1}$ на вектор $(x_1, x_2, x_3)^T$ (в данном случае $x_i$ - именно буквы). Элементы вектора $(x'_1, x'_2, x'_3)^T$ - и есть искомая замена координат.


### Пример: 

Дано: квадратичная форма $Q(x_1 x_2, x_3) = x_1^2 + x_2^2 - x_3^2 - 4x_1x_3 - 4x_2x_3$. Найти канонический вид, к которому форма приводится ортогональным преобразованием, базис, в котором она принимает канонический вид и замену координат (выражение старых координат через новые).

**Решение:**

**Шаг 1.** Составляем матрицу квадратичной формы: *знаем, что любую квадратичную форму можно привести к каноническому виду - оператор диагонализуем:*

$$Q = \begin {pmatrix}
1 & 0 & -2\\
0 & 1 & -2\\
-2 & -2 & -1\\
\end{pmatrix}$$

**Шаг 2.** 2.1. Находим корни характеристического многочлена: то есть, приравниваем к нулю определитель следующей матрицы:

$$Q(t) = \begin {pmatrix}
1 - t & 0 & 2\\
0 & 1 - t & 2\\
2 & 2 & -1 - t\\
\end{pmatrix}$$

$(1 - t)^2(-1 - t) - 8(1 - t) = 0 \implies$

$\implies (1 - t)((t - 1)(t + 1) - 8) = 0 \implies (t - 1)(t - 3)(t + 3) = 0$

Полученные корни: $t_1 = 1, t_2 = 3, t_3 = -3$. Значит, все собственные значения - $\lambda_1 = 1, \lambda_2 = 3, \lambda_3 = -3$

Число корней и собственных значений совпадает с размерностью пространства (собственно говоря, так и должно быть, ведь диагонализовать ортогональными преобразованиями мы можем матрицу любой квадратичной формы) - значит, можно решать дальше.

2.2. Ищем базисы собственных подпространств:

$\lambda_1 = 1$ - ищем ФСР для матрицы 

$$\begin {pmatrix}
1 - 1 & 0 & -2\\
0 & 1 - 1 & -2\\
-2 & -2 & -1 - 1\\
\end{pmatrix} = \begin {pmatrix}
0 & 0 & -2\\
0 & 0 & -2\\
-2 & -2 & -2\\
\end{pmatrix} \rightarrow УСВ \rightarrow \begin {pmatrix}
1 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0\\
\end{pmatrix}$$

$$x_3 = 0; x_1 = -x_2; \ ФСР: v_1 = \begin {pmatrix}
1\\
-1\\
0\\
\end{pmatrix}$$

$\lambda_2 = 3$ - ищем ФСР для матрицы 

$$\begin {pmatrix}
1 - 3 & 0 & 2\\
0 & 1 - 3 & 2\\
2 & 2 & -1 - 3\\
\end{pmatrix} = \begin {pmatrix}
-2 & 0 & -2\\
0 & -2 & -2\\
-2 & -2 & -4\\
\end{pmatrix} \rightarrow УСВ \rightarrow \begin {pmatrix}
1 & 0 & 1\\
0 & 1 & 1\\
0 & 0 & 0\\
\end{pmatrix}$$

$$x_1 = 0 = x_2 = -x_3; \ ФСР: v_1 = \begin {pmatrix}
-1\\
-1\\
1\\
\end{pmatrix}$$

$\lambda_3 = -3$ - ищем ФСР для матрицы 

$$\begin {pmatrix}
1 - (-3) & 0 & -2\\
0 & 1 - (-3) & -2\\
-2 & -2 & -1 - (-3)\\
\end{pmatrix} = \begin {pmatrix}
4 & 0 & -2\\
0 & 4 & -2\\
-2 & -2 & 2\\
\end{pmatrix} \rightarrow УСВ \rightarrow \begin {pmatrix}
1 & 0 & -\frac{1}{2}\\
0 & 1 & -\frac{1}{2}\\
0 & 0 & 0\\
\end{pmatrix}$$

$$x_2 = \frac{1}{2}x_3; x_1 = \frac{1}{2}x_3; \ ФСР: v_3 = \begin {pmatrix}
1\\
1\\
2\\
\end{pmatrix}$$

**Шаг 3.** Ортонормируем все три вектора: для этого поделим каждый на его длину:

$$v'_1 = \begin {pmatrix}
\frac{1}{\sqrt 2}\\
-\frac{1}{\sqrt 2}\\
0\\
\end{pmatrix}; v'_2 = \begin {pmatrix}
-\frac{1}{\sqrt 3}\\
-\frac{1}{\sqrt 3}\\
\frac{1}{\sqrt 3}\\
\end{pmatrix}; v'_3 = \begin {pmatrix}
\frac{1}{\sqrt 6}\\
\frac{1}{\sqrt6}\\
\frac{2}{\sqrt6}\\
\end{pmatrix}$$

**Шаг 4. Искомый базис - $v'_1, v'_2, v'_3$.** По диагональной матрице, на главной диагонали которой стоят все собственные значения, выпишем **канонический вид квадратичной формы:**

$$Q' = \begin {pmatrix}
1 & 0 & 0\\
0 & 3 & 0\\
0 & 0 & -3\\
\end{pmatrix}; Q'(x) = x_1^2 + 3x_2^2 - 3x_3^2$$

**Шаг 5.** Замена координат: поскольку матрица перехода от старого (стандартного) базиса к новому - матрица $C$, в строки которой выписаны найденные нами базисные векторы, умножим обратную на вектор $x$ и получим выражение новых координат через старые:

$$C = \begin {pmatrix}
\frac{1}{\sqrt 2} & -\frac{1}{\sqrt 3} & \frac{1}{\sqrt 6}\\
- \frac{1}{\sqrt 2} & -\frac{1}{\sqrt 3} & \frac{1}{\sqrt 6}\\
0 & \frac{1}{\sqrt 2} & \frac{1}{\sqrt 3}\\
\end{pmatrix}; C^{-1} = \begin {pmatrix}
\frac{\sqrt 3}{2} & -\frac{\sqrt 3}{2} & 0\\
-\frac{3 \sqrt 2}{4} & -\frac{\sqrt 2}{4} & \frac{\sqrt 2}{2}\\
-\frac{\sqrt 6}{4} & \frac{\sqrt 6}{4} & \frac{\sqrt 6}{2}\\
\end{pmatrix}$$

$$\begin {pmatrix}
x_1'\\
x_2'\\
x_3'\\
\end{pmatrix} = C^{-1} \begin {pmatrix}
x_1\\
x_2\\
x_3\\
\end{pmatrix} \implies \begin {matrix}
x_1' = \frac{\sqrt 3}{2}x_1 - \frac{\sqrt 3}{2}x_2\\
x_2' = -\frac{3 \sqrt 2}{4}x_1 -\frac{\sqrt 2}{4}x_2 + \frac{\sqrt 2}{2}x_3\\
x_3' = -\frac{\sqrt 6}{4}x_1 + \frac{\sqrt 6}{4}x_2 + \frac{\sqrt 6}{2}x_3\\
\end{matrix}$$
- **выражение старых координат через новые** 

## 4. Поиск SVD для матрицы.

В данном случае наша задача - представить произвольную матрицу $A$ в виде произведения матриц $U \sum V^T$, где $U$ и $V$ - ортогональные, а $\sum$ - диагональна, причём элементы на главной диагонали, именуемые *сингулярными значениями*, неотрицательны и расположены на диагонали в порядке убывания.
Искать можно как полное разложение матрицы, так и усечённое - в алгоритме будут указаны различия между способами поиска и того, и другого.

Более того, этот алгоритм всегда начинается с умножения матрицы $A$ на транспонированную ей - но в зависимости от перестановки множителей размер результата может отличаться. И, поскольку чем меньше матрица, тем удобнее с ней работать, в одном из способов предлагается найти сингулярное разложение для матрицы $A^T$, позже просто переписав его для исходной.

*Итак, если размер $A^TA$ меньше размера $AA^T$ - удобнее использовать первый способ, в ином случае - второй.*

### Первый способ.

**Дано:** матрица $A$. Требуется найти для неё сингулярное разложение.

### Решение.

**Шаг 1.** Вычисляем матрицу $A^TA$ и находим её ненулевые собственные значения. То есть, корни характеристического многочлена.

Записываем полученные значения в порядке убывания: получаем $s_1 \geq s_2\ ... \geq s_r$ (важно - они получатся положительными). Тогда собственные значения - $\sigma _1,\ ..., \sigma_r$, где $\sigma_i = \sqrt{s_i}$

*! Важно!* Если алгебраическая кратность $k$ какого-то из значений больше 1, его нужно записать $k$ раз.

**Шаг 2.** Находим векторы $v_1, ... v_r$ - это ортонормированные базисы собственных подпространств, и $v_i$ - ФСР для ОСЛУ, задаваемой матрицей:

$$A^TA - \lambda _i E$$

Не забываем нормировать векторы или приводить к ортонормированному виду весь базис. Потом "сортируем" векторы по убыванию собственных значений, собственным подпространствам которых они отвечают.

**Шаг 3.** Для каждого $i = 1, 2\ ...\ r$ считаем все $u_i = \frac{1}{\sigma_i}Av_i$. Эту систему ортонормировать не нужно - она таковой *уже является.*

**Шаг 4.** Если ищем **полное сингулярное разложение**, дополняем системы $v_i$ и $u_i$ до ортонормированного базиса. В случае же с **усечённым разложением** если $k = r$, просто ничего не делаем - иначе необходимо дополнить векторы до ортноромированной системы размера $k$. Например, можно найти векторы $v_{r + 1}\ ...\ v_n$ как ортонормированную ФСР для матрицы $A$, а $u_{r + 1}\ ...\ u_n$ - как ортонормированную ФСР для $A^T$.

**Шаг 5.** Числа $\sigma _i$ - элементы главной диагонали матрицы $\sum$ (все остальные элементы этой матрицы равны 0); векторы $v_i$ записываем в столбцы матрицы $V$, а векторы $u_i$ - в столбцы матрицы $U$.

Осталось записать полученное сингулярное разложение:

$$A = U \sum V^T$$

### Способ второй.

**Дано:** матрица $A$. Требуется найти для неё сингулярное разложение.

### Решение.

**Шаг 1.** Вычисляем матрицу $AA^T$ и находим её ненулевые собственные значения. То есть, корни характеристического многочлена.

Записываем полученные значения в порядке убывания: получаем $s_1 \geq s_2\ ... \geq s_r$ (важно - они получатся положительными). Тогда собственные значения - $\sigma _1,\ ..., \sigma_r$, где $\sigma_i = \sqrt{s_i}$

*! Важно!* Если алгебраическая кратность $k$ какого-то из значений больше 1, его нужно записать $k$ раз.

**Шаг 2.** Находим векторы $u_1, ... u_r$ - это ортонормированные базисы собственных подпространств, и $u_i$ - ФСР для ОСЛУ, задаваемой матрицей:

$$AA^T - \lambda _i E$$

Не забываем нормировать векторы или приводить к ортонормированному виду весь базис. Потом "сортируем" векторы по убыванию собственных значений, собственным подпространствам которых они отвечают.

**Шаг 3.** Для каждого $i = 1, 2\ ...\ r$ считаем все $v_i = \frac{1}{\sigma_i}A^Tu_i$. Эту систему ортонормировать не нужно - она таковой *уже является.*

**Шаг 4.** Если ищем **полное сингулярное разложение**, дополняем системы $v_i$ и $u_i$ до ортонормированного базиса. В случае же с **усечённым разложением** если $k = r$, просто ничего не делаем - иначе необходимо дополнить векторы до ортноромированной системы размера $k$. Например, можно найти векторы $v_{r + 1}\ ...\ v_n$ как ортонормированную ФСР для матрицы $A$, а $u_{r + 1}\ ...\ u_n$ - как ортонормированную ФСР для $A^T$.

**Шаг 5.** Числа $\sigma _i$ - элементы главной диагонали матрицы $\sum$ (все остальные элементы этой матрицы равны 0); векторы $v_i$ записываем в столбцы матрицы $V$, а векторы $u_i$ - в столбцы матрицы $U$.

Осталось записать полученное сингулярное разложение:

$$A = V \sum U^T$$

### Пример.

Для матрицы $A = \begin{pmatrix}
2 & 2 & -6 \\
6 & 1 & 2 \\
\end{pmatrix}$ найти её усечённое сингулярное разложение и матрицу $B$ ранга 1, для которой норма Фробениуса $||A - B||$ минимальна.

### Решение.

Нужно найти все матрицы для равенства $A = U\sum V^T$

- Исходная матрица имеет размер $m$ на $n$, где $m = 2, n = 3; min (2, 3) = 2.$ Поскольку нас интересует именно усечённое разложение, диагональная - она же центральная - матрица-компонента $\sum$ будет иметь размер $2$ на $2$.
- Заметим, что матрица $A^TA$ имеет размер 3 на 3, в то время как $AA^T$ - 2 на 2. Значит, удобнее использовать **второй способ нахождения сингулярного разложения.**

**Шаг 1.** Считаем $AA^T$ - получаем матрицу $\begin{pmatrix}
44 & 2\\
2 & 41\\
\end{pmatrix}$.

Теперь ищем её собственное значения - то есть, корни определителя матрицы $\begin{pmatrix}
44 - t & 2\\
2 & 41 - t\\
\end{pmatrix}$. Считаем:

$(44 - t)(41 - t) - 4 = 1804 - 85t + t^2 - 2 = t^2 - 85t + 1800 = 0$

$D = 7225 - 7200 = 25$ - два действительных корня

$t_1 = 40; t_2 = 45$. Многочлен раскладывается на линейные множители следующим образом:

$$(t - 45)(t - 40);$$

Сортируем собственные значения в порядке убывания и получаем $s_1 = 45, s_2 = 40$. Значит, сингулярные значения матрицы - $\sigma_1 = \sqrt {45} = 3 \sqrt 5; \sigma_2 = \sqrt {40} = 2 \sqrt {10}$

**Шаг 2.** Ищем векторы $u_1$ И $u_2$. Для этого достаточно просто найти ФСР такой матрицы:

$$AA^T - s_1 E = \begin{pmatrix}
44 & 2\\
2 & 41\\
\end{pmatrix} - 45*\begin{pmatrix}
1 & 0\\
0 & 1\\
\end{pmatrix} = \begin{pmatrix}
-1 & 2\\
2 & -4\\
\end{pmatrix}$$

УСВ: $\begin{pmatrix}
1 & -2\\
0 & 0\\
\end{pmatrix}, x_1 = 2x_2$, ФСР$:(2\ \ 1)$.

Нормируем этот вектор и получим $u_1 = \frac{1}{\sqrt 5} (2\ \ 1)$

...и ФСР такой матрицы:

$$AA^T - s_1 E = \begin{pmatrix}
44 & 2\\
2 & 41\\
\end{pmatrix} - 40*\begin{pmatrix}
1 & 0\\
0 & 1\\
\end{pmatrix} = \begin{pmatrix}
4 & 2\\
2 & 1\\
\end{pmatrix}$$

УСВ: $\begin{pmatrix}
2 & 1\\
0 & 0\\
\end{pmatrix}, x_1 = -\frac{1}{2}x_2$, ФСР$:(-1\ \ 2)$.

Снова нормируем, получив $u_2 = \frac{1}{\sqrt 5} (-1\ \ 2)$

***! Важно:** получившуюся из векторов $u_1$ и $u_2$ систему **не нужно будет ортогонализовывать**. Почему? Собственные пространства, отвечающие различным собственным значениям, попарно ортогональны, а значит, попарно ортогональны и любые два вектора из них. Так и здесь: базисы подпространства, отвечающего 40, и подпространства, отвечающего 45, уже ортогональны друг другу.*

**Шаг 3.** Cчитаем:

$$v_1 = \frac{1}{\sigma_1}A^Tu_1 = \frac{1}{3\sqrt 5}\begin{pmatrix}
2 & 6\\
2 & 1\\
-6 & 2\\
\end{pmatrix}\frac{1}{\sqrt 5}\begin{pmatrix} 2 \\ 1 \\ \end{pmatrix} = \frac{1}{15}\begin{pmatrix} 10 \\ 5 \\ -10\\\end{pmatrix} = \begin{pmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3}\\\end{pmatrix}$$

(заметим, этот вектор уже ортонормированный - $\frac{10^2 + 5^2 + 10^2}{15} = 1$) и

$$v_2 = \frac{1}{\sigma_2}A^Tu_2 = \frac{1}{2\sqrt 10}\begin{pmatrix}
2 & 6\\
2 & 1\\
-6 & 2\\
\end{pmatrix}\frac{1}{\sqrt 5}\begin{pmatrix} -1 \\ 2 \\ \end{pmatrix} = \frac{1}{10 \sqrt 2}\begin{pmatrix} 10 \\ 0 \\ 10\\\end{pmatrix} = \begin{pmatrix} \frac{1}{\sqrt 2} \\ 0 \\ \frac{1}{\sqrt 2}\\\end{pmatrix}$$

(снова можем проверить  убедиться, что этот вектор ортнормирован)

Знаем, что найденные векторы тоже ортогональны друг другу.

**Шаг 4.** В следующем шаге нужно дополнять системы размера $r$ до ортонормированных систем размера $k$ (размер центральной матрицы), но в данном случае нам повезло: $k = r = 2$, значит, этот этап можно пропускать.

***! Важно** а вот если бы мы искали полное разложение, пришлось бы дополнять системы до ортонормированных базисов всего пространства. Система $u_1, u_2$ его уже образует, а вот $v_3$ пришлось бы досчитывать. Например, это можно было бы сделать так:*

- Дополним $v_1 = \begin{pmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3}\\\end{pmatrix}$ и $v_2 = \begin{pmatrix} \frac{1}{\sqrt 2} \\ 0 \\ \frac{1}{\sqrt 2}\\\end{pmatrix}$ до базиса $R^3$ вектором $e_3 = \begin{pmatrix} 0 \\ 0 \\ 1\\\end{pmatrix}$ из стандартного базиса и ортогонализуем его с помощью формулы Грамма-Шмидта:

$$v'_3 = e_3 - \frac{(e_3, v_1)}{(e_3, e_3)}v_1 - \frac{(e_3, v_2)}{(e_3, e_3)}v_2 = \begin{pmatrix} 0 \\ 0 \\ 1\\\end{pmatrix}- (-\frac{2}{3})\begin{pmatrix} \frac{2}{3} \\ \frac{1}{3} \\ -\frac{2}{3}\\\end{pmatrix} - \frac{1}{\sqrt 2}\begin{pmatrix} \frac{1}{\sqrt 2} \\ 0 \\ \frac{1}{\sqrt 2}\\\end{pmatrix}$$

$$v'_3 = \begin{pmatrix} \frac{1}{18} & \frac{2}{9} & -\frac{1}{18} \end{pmatrix}^T = \frac{1}{18}\begin{pmatrix} 1 & 4 & -1 \end{pmatrix}^T$$

- Вектор сразу получился ортонормированным; более того, его попарное перемножение с $v_1$ и $v_2$ всегда даёт $0.$

В нашей задаче, то есть, в процессе поиска *усечённого* сингулярного разложения, дополнять ничего до базисов, опять же, было не нужно. Это просто уточнение с одним из способов поиска дополнения на случай, если выполнять такое понадобится.

**Шаг 5.** Записываем сингулярное разложение: для исходной матрицы $A$ оно выглядит так:

$$A = V \sum U^T = \begin{pmatrix} \frac{2}{3} & \frac{1}{\sqrt 2}\\ \frac{1}{3} & 0\\ -\frac{2}{3} & \frac{1}{\sqrt 2}\\ \end{pmatrix}*\begin{pmatrix}
3\sqrt 5 & 0\\
0 & 2 \sqrt 10\\
\end{pmatrix} * \frac{1}{\sqrt 5}\begin{pmatrix}
2 & -1\\
1 & 2\\
\end{pmatrix}$$



