## 求相似对角化的可逆矩阵P
### 求可逆矩阵P使$P^{-1}AP=\Lambda$的解题步骤
1. 求出矩阵A(设为3阶)的特征值$\lambda_1, \lambda_2, \lambda_3$(可以有重根)
2. 求出线性无关的特征向量$\alpha_1, \alpha_2, \alpha_3$
3. 构造可逆矩阵$P=(\alpha_1, \alpha_2, \alpha_3)$, 则有$P^{-1}AP=\Lambda=
\begin{bmatrix}
\lambda_1 & &\\
& \lambda_2 & \\
& & \lambda_3
\end{bmatrix}$

$$\begin{aligned}
& \textcolor{red}{注} 由A\alpha_1=\lambda_1\alpha_1, A\alpha_2=\lambda_2\alpha_2, A\alpha_3=\lambda_3\alpha_3 \Rightarrow A(\alpha_1, \alpha_2, \alpha_3)=(\lambda_1\alpha_1, \lambda_2\alpha_2, \lambda_3\alpha_3)=(\alpha_1, \alpha_2, \alpha_3)
\begin{bmatrix}
\lambda_1 & &\\
& \lambda_2 & \\
& & \lambda_3
\end{bmatrix} \\
& \quad 即 AP=P\Lambda \Rightarrow P^{-1}AP=\Lambda
\end{aligned}$$
