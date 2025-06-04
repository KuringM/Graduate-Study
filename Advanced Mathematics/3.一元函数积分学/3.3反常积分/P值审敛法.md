## P值审敛法

### 1. 无穷区间上的P值审敛法

设$f(x)$在$[a, +\infty)$上**非负连续**,

1. 若存在常数$M>0, p>1$, 使得$\displaystyle f(x) \leqslant \frac{M}{x^{p}}$, 则$\displaystyle\int_a^{+\infty} f(x)\mathrm{d}x$收敛.
2. 若存在常数$M>0, p \leqslant 1$, 使得$\displaystyle f(x) \geqslant \frac{M}{x^{p}}$, 则$\displaystyle\int_a^{+\infty} f(x)\mathrm{d}x$发散.
3. 若$p>1$,且$\lim\limits_{x\to +\infty}x^p f(x)=\textcolor{red}{c < +\infty}$, 则$\displaystyle\int_a^{+\infty} f(x)\mathrm{d}x$收敛.
4. 若$p \leqslant 1$,且$\lim\limits_{x\to +\infty}x^p f(x)=c, \textcolor{red}{0< c \leqslant +\infty}$, 则$\displaystyle\int_a^b f(x)\mathrm{d}x$发散.

> 1,2为比较形式; 3,4为极限形式 <BR>
> 极限 $c< +\infty$ 表示极限c存在 <BR>
> 极限 $0< c< +\infty$ 表示极限c存在且大于0或不存在

### 2. 暇积分的P值审敛法

设$f(x)$在$[a, b)$上**非负连续**,以b为瑕点

1. 若存在常数$M>0, p<1$, 使得$\displaystyle f(x) \leqslant \frac{M}{(b-x)^{p}}$, 则$\displaystyle\int_a^{+\infty} f(x)\mathrm{d}x$收敛.
2. 若存在常数$M>0, p \geqslant 1$, 使得$\displaystyle f(x) \geqslant \frac{M}{(b-x)^{p}}$, 则$\displaystyle\int_a^{+\infty} f(x)\mathrm{d}x$发散.
3. 若$p<1$,且$\lim\limits_{x\to b^{-}}(b-x)^p f(x)= c < +\infty$, 则$\displaystyle\int_a^b f(x)\mathrm{d}x$收敛.
4. 若$p \geqslant 1$,且$\lim\limits_{x\to b^{-}}(b-x)^p f(x)= c , 0 < c \leqslant +\infty$, 则$\displaystyle\int_a^b f(x)\mathrm{d}x$发散.
