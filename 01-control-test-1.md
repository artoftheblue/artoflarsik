# Контрольная работа 2022-2023

## Задание 1

:::{note} Условие
Рассмотрим линейное отображение $\phi\colon \R[x]_{\leq3}\mapsto \R^3, f\mapsto(f'(-1), f''(-1), f(1))$. Найдите базис $\ebase$ пространства $\R^3$, в которых $\,\phi\,$ имеет диагональный вид с единицами и нулями на диагонали, и выпишите этот вид.
::: 

:::{seealso} Решение
$\exists$ линейное отображение $\phi\colon V\to W$.

$\exists \ker\phi\in V=\langle e_{r_+1},\dots,e_n\rangle$. Дополним ядро до $\langle e_1,\dots,e_r,e_{r+1},\dots, e_n\rangle=V$ — базис отображения.

$\exists \Im\phi\in W=\langle\phi(e_1),\dots,\phi(e_r)\rangle$. Дополним образ до $\langle\phi(e_1),\dots,\phi(e_r),f_{r+1},\dots,f_m\rangle$, где $f_1=\phi(e_1),\dots,f_r=\phi(e_r)$

$\R[x]_{\leq 3}\mapsto\R^3, \phi\colon f\mapsto(f'(-1),f''(-1),f(-1))$

---

Посчитаем значения $\,\phi\,$ для базисных векторов $1, x, x^2, x^3$:

$$\phi(1)=(0,0,1)=f_1,\quad\phi(x^2)=(-2,2,1)=f_3,\\\quad\phi(x)=(1,0,1)=f_2,\quad\phi(x^3)=(3,-6,1)=f_4$$

Теперь выписываем УСВ:

$$\begin{pmatrix}
    0 & 1 & -2 & 3\\
    0 & 0 & 2 & -6\\
    1 & 1 & 1 & 1
\end{pmatrix}\leadsto\begin{pmatrix}
    0 & 1 & 0 & -3\\
    0 & 0 & 1 & -3\\
    1 & 1 & 0 & 4
\end{pmatrix}\leadsto\begin{pmatrix}
    0 & 1 & 0 & -3\\
    0 & 0 & 1 & -3\\
    1 & 0 & 0 & 7
\end{pmatrix}\leadsto\\
\stackrel{d\quad c\quad\ b\quad\ \ \  a \ }{\begin{pmatrix}
    1 & 0 & 0 & 7\\
    0 & 1 & 0 & -3\\
    0 & 0 & 1 & -3
\end{pmatrix}}\implies\begin{align*}
    &c=3a\\
    &b=3a\\
    &d=-7a
\end{align*}$$

Чётвертая координата свободна, выписываем ФСР:

$$\Phi=\overset{\small{\ \ \ d\ \  c\ \  b\ \  a}}{(-7,3,3,1)}$$

Теперь этот вектор нужно дополнить до базиса пространства:

$$\begin{align*}
(-7,3,3,1)\\
(0,0,1,0)\\
(0,1,0,0)\\
(1,0,0,0)
\end{align*}$$

т. е. мы нашли $\langle e_1,\dots,e_r,e_{r+1},\dots,e_n\rangle$

$$\begin{align*}
    &e_4=x^3+3x^2+3x-7\\
    &e_3=x^2\\
    &e_2=x\\
    &e_1=1
\end{align*} - \text{базис в исходном пространстве}$$

Тогда базис в $\R^3\colon\langle f_1,f_2,f_3\rangle$ и матрица отображения будет:

$$\begin{pmatrix}
    1 & 0 & 0 & 0\\
    0 & 1 & 0 & 0\\
    0 & 0 & 1 & 0
\end{pmatrix}$$

:::

## Задание 2

:::{note} Условие
Пусть $V$ — пространство всех верхнетреугольных матриц размера $2\times 2$ с коэффициентами из $\R,S=\begin{pmatrix}1 & 2\\ - 3&0\end{pmatrix},\ v=(1,-1)$. Рассмотрим на $V$ линейные функции $\alpha_1,\alpha_2,\alpha_3$, где

$$\alpha_1(X)=\tr(X),\quad\alpha_2(X)=\tr(XS),\quad\alpha_3(X)=vXv^T,\quad \forall X\in V$$

Найдите базис пространства $V$, для которого набор $(\alpha_1,\alpha_2,\alpha_3)$ является двойственным базисом пространства $V^*$.
:::

:::{seealso}
Введём стандартный базис всех верхнетреугольных матриц:
$$e_1=\stackrel{\displaystyle a}{\begin{pmatrix}
1 & 0\\
0 & 0
\end{pmatrix}},\quad e_2=\stackrel{\displaystyle b}{\begin{pmatrix}
0 & 1\\
0 & 0
\end{pmatrix}},\quad e_3=\stackrel{\displaystyle c}{\begin{pmatrix}
0 & 1\\
0 & 0
\end{pmatrix}}$$

Перейдём к координатам:

$$X=\begin{pmatrix}
    a & b\\
    0 & c
\end{pmatrix}$$

$$XS=\begin{pmatrix}
    a & b\\
    0& c\\
\end{pmatrix}\begin{pmatrix}
    1 & 2\\
    -3 & 0\\
\end{pmatrix}=\begin{pmatrix}
    a - 3b & 2a\\
    -3c & 0
\end{pmatrix}
$$

$$vXb^T=\begin{pmatrix}
    1 & -1\\
\end{pmatrix}\begin{pmatrix}
    1 & 2\\
    -3 & 0
\end{pmatrix}\begin{pmatrix}
    1\\
    -1
\end{pmatrix}=\begin{pmatrix}
    1 & -1\\
\end{pmatrix}\begin{pmatrix}
    a - b\\
    -c
\end{pmatrix}=a-b+c$$

Теперь векторы базиса:

$$\begin{align*}
&\eps_1=\alpha_1(X)=\tr(X)=a+c\\
&\eps_2=\alpha_2(X)=\tr(XS)=a-3b\\
&\eps_3=\alpha_3(X)=vXv^T=a-b+c
\end{align*}$$

Есть двойственный базис, ищем исходный к нему:

$$\begin{matrix}
    \alpha_1(e_1)=1 & \alpha_1(e_2)=0 & \alpha_1(e_3)=0\\
    \alpha_2(e_1)=0 & \alpha_2(e_2)=1 & \alpha_2(e_3)=0\\
    \alpha_3(e_1)=0 & \alpha_3(e_2)=0 & \alpha_3(e_3)=1
\end{matrix}$$

$$\begin{cases}
a+c=1\\
a-3b=0\\
a-b+c=0
\end{cases}\quad\begin{cases}
a+c=0\\
a-3b=1\\
a-b+c=0
\end{cases}\quad\begin{cases}
a+c=0\\
a-3b=0\\
a-b+c=1
\end{cases}$$

$$\begin{pmatrix}
        & & & & e_1& e_2& e_3\\
    1 & 0 & 1 & \bigm| & 1 & 0 & 0\\
    1 & -3 & 0 & \bigm| & 0 & 1 & 0\\
    1 & -1 & 1 & \bigm| & 0 & 0 & 1\\
\end{pmatrix}\leadsto\begin{pmatrix}
    & & & & & e_1& e_2& e_3\\
    1 & 0 & 0 & \bigm| & a& 3 & 1 & -3\\
    0 & 1 & 0 & \bigm| & b&1 & 0 & -1\\
    0 & 0 & 1 & \bigm| & c&-2 & -1 & 3\\
\end{pmatrix}$$

Можно сделать проверку:

$$\begin{cases}
3-2=1\\
3-3=0\\
3-1-2=0
\end{cases}\quad\begin{cases}
1-1=0\\
1-0=1\\
1-0-1=0
\end{cases}\quad\begin{cases}
-3+3=0\\
-3+3=0\\
-3+1+3=1
\end{cases}$$

Запишем наш ответ в терминах матриц:

$$e_1=\begin{pmatrix}
3 & 1\\
0 & -2
\end{pmatrix},\quad e_2=\begin{pmatrix}
    1 & 0\\
    0 & -1
\end{pmatrix},\quad e_3=\begin{pmatrix}
    -3 & 1\\
    0 & 3
\end{pmatrix}$$


:::