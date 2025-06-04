## P积分

### 1. 无穷区间上的P积分

$$
\begin{aligned}
	&\int_a^{+\infty}\frac{1}{x^p}\mathrm{d}x
	\begin{cases}
		p>1, 收敛\\[2mm]
		p \leqslant 1, 发散
	\end{cases}
	(a>0)\\
\end{aligned}
$$

###### Proof

$$
\begin{aligned}
	& I. \enspace p=1\\
	& \quad \int_{a}^{+\infty}\frac{1}{x^p} \mathrm{d}x= \int_{a}^{+\infty} \frac{1}{x} \mathrm{d}x
	= \left[ \ln x \right]_{a}^{+\infty} =  +\infty\\
	\newline
	& II. \enspace p \not= 1\\
	& \quad \int_{a}^{+\infty}\frac{1}{x^p} \mathrm{d}x= \left[ \frac{x^{1-p}}{1-p} \right]_{a}^{+\infty} =
	\begin{cases}
		+\infty, & p<1\\[2mm]
		\displaystyle \frac{-a^{1-p}}{1-p}, & p > 1
	\end{cases}
\end{aligned}
$$

### 2. 无界函数的P积分

$$
\begin{aligned}
	&\int_a^{b}\frac{1}{(x-a)^p}\mathrm{d}x
	\begin{cases}
		p<1, 收敛\\[2mm]
		p\geqslant 1, 发散
	\end{cases}\\[2mm]
	&\int_a^{b}\frac{1}{(b-x)^p}\mathrm{d}x
	\begin{cases}
		p<1, 收敛\\[2mm]
		p\geqslant 1, 发散
	\end{cases}\\
	\newline
\end{aligned}
$$

###### Proof

$$
\begin{aligned}
	& I. \enspace p=1\\
	& \quad \int_{a}^{b}\frac{1}{(x-a)^p} \mathrm{d}x= \int_{a}^{b} \frac{1}{(x-a)} \mathrm{d}x
	= [ \ln (x-a) ]_{a}^{b} = \ln(b-a) - \lim\limits_{x\to a^{+}} \ln(x-a) = +\infty\\
	\newline
	& II. \enspace p \not= 1\\
	& \quad \int_{a}^{b}\frac{1}{(x-a)^p} \mathrm{d}x= \left[ \frac{(x-a)^{1-p}}{1-p} \right]_{a}^{b} =
	\begin{cases}
		\displaystyle \frac{(b-a)^{1-p}}{1-p}, & p < 1\\[2mm]
		+\infty, & p>1
	\end{cases}
\end{aligned}
$$
