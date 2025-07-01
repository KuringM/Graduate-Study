# 阿贝尔(Abel)定理

1. 若$\sum\limits_{n=1}^{\infty}a_n x^n$当$x=x_0(x_0\not=0)$时收敛,则当$|x|< |x_0|$时, $\sum\limits_{n=0}^{\infty}a_nx^n$绝对收敛; ^262ecc
2. 若$\sum\limits_{n=0}^{\infty}a_nx^n$当$x=x_0$时发散,则当$|x| > |x_0|$时, $\sum\limits_{n=0}^{\infty}a_nx^n$时发散. ^5dc68a

> 幂级数在某点条件收敛,由阿贝尔定理知该点为收敛区间区间端点,则知收敛半径

###### Proof

先设 $x_0$ 是幂级数 $\sum\limits_{n=1}^{\infty}a_n x^n$ 的收敛点, <BR>
即级数$a_0 + a_1 x_0 + a_2 x_0^2 + \cdots + a_n x_0^n + \cdots$收敛. <BR>
根据级数收敛的必要条件, 这时有

$$
\lim_{n \to \infty} a_n x_0^n = 0,
$$

于是存在一个常数 $M$, 使得

$$
|a_n x_0^n| \leqslant M \quad (n = 0, 1, 2, \cdots).
$$

这样级数的一般项的绝对值

$$
|a_n x^n|
= \left| a_n x_0^n \cdot \frac{x^n}{x_0^n} \right|
= |a_n x_0^n| \cdot \left| \frac{x}{x_0} \right|^n
\leqslant M \left| \frac{x}{x_0} \right|^n.
$$

因为当 $|x| < |x_0|$ 时,
等比级数 $\sum\limits_{n=0}^{\infty} M \left| \frac{x}{x_0} \right|^n$ 收敛 (公比 $\left| \frac{x}{x_0} \right| < 1$),
所以级数 $\sum\limits_{n=0}^{\infty} |a_n x^n|$ 收敛,
也就是级数 $\sum\limits_{n=0}^{\infty} a_n x^n$ 绝对收敛.

定理的第二部分可用反证法证明. <BR>
假设幂级数当 $x = x_0$ 时发散而有一点 $x_1$ 适合 $|x_1| > |x_0|$ 使级数收敛, <BR>
则根据本定理的第一部分, 级数当 $x = x_0$ 时应收敛, 这与假设矛盾. 定理得证.
