# 线性代数笔记

> 工科数学线性代数(第六版)：https://abook.hep.com.cn/39661

## 1. 行列式

* **逆序数：** 对于$n$个不同的元素，先规定各元素之间有一个标准次序(例如从小到大)，与标准次序不同的元素对构成逆序，逆序总数成为逆序数

  * 奇排列：逆序数为奇数的排列
  * 偶排列：逆序数为偶数的排列

* **对换**：

  * **定理1：**一个排列中的任意两个元素对换，排列改变奇偶性
  * 推论：奇排列对换成标准排列的对换次数为奇数，偶排列对换成标准排列的对换次数为偶数

* **$n$阶行列式：**

  * $D=\left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ a_{21}& a_{22} & \cdots & a_{2n} \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right | $
  * 上(下)三角形行列式和对角行列式的值为行列式对角线元素之积，即$D=a_{11}a_{22}\cdots a_{nn}$

* **行列式的性质：**

  * 性质1：行列式与它的转置行列式相等：$D=D^T$

  * 性质2：对换行列式的两行(列)，行列式变号

    * 推论：如果行列式有两行(列)完全相同，则行列式等于零

      > 证：对换两行后$D=-D$，则$D=0$

  * 性质3：行列式的某一行(列)中所有元素都乘同一数$k$，等于用数$k$乘此行列式

    * 推论：行列式中某一行(列)的所有元素的公因子可以提到行列式记号的外面，即

      $\left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ \vdots & \vdots  &  & \vdots  \\ ka_{i1}& ka_{i2} & \cdots & ka_{in} \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right | \xlongequal{r_i\div k} k \left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ \vdots & \vdots  &  & \vdots  \\ a_{i1}& a_{i2} & \cdots & a_{in} \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right | $

  * 性质4：行列式中如果有两行(列)元素成比例，则此行列式等于零

  * 性质5：若行列式的某一行(列)元素都是两数之和，则行列式等于两个行列式之和，即

    $\left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ \vdots & \vdots  &  & \vdots  \\ a_{i1}+a_{i1}'& a_{i2}+a_{i2}' & \cdots & a_{in}+a_{i1}' \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right | =\left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ \vdots & \vdots  &  & \vdots  \\ a_{i1}& a_{i2} & \cdots & a_{in} \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right | +\left | \begin{array}{cccc} a_{11}& a_{12} & \cdots & a_{1n} \\ \vdots & \vdots  &  & \vdots  \\ a_{i1}'& a_{i2}' & \cdots & a_{i1}' \\ \vdots & \vdots  &  & \vdots  \\ a_{n1}& a_{n2} & \cdots & a_{nn} \end{array} \right |  $ 

  * 性质6：把行列式的某一行(列)的各元素乘同一数然后加到另一行(列)对应的元素上去，行列式不变

* **计算行列式：**

  * $D=\left | \begin{array}{cccc}& & & a_{1n} \\ 0 &  &  a_{2,n-1} & a_{2n}  \\  & \cdot^{\cdot^{\cdot}}  & \vdots & \vdots  \\ a_{n1}& \cdots & a_{n-1,n1} & a_{n,n} \end{array} \right | = (-1)^{\frac{1}{2}n(n-1)}a_{1n}a_{2,n-1}\cdots a_{n1}$
  * $D=\left| \begin{array}{cc} D_1 & 0 \\ D_3 & D_2 \end{array} \right| = D_1D_2$

* **余子式：**

  * $n$阶行列式$det(a_{ij})$中，把第$i$行和第$j$列划去后，留下来的$n-1$阶行列式叫做$a_{ij}$的余子式$M_{ij}$
  * $a_{ij}$的**代数余子式**：$A_{ij}=(-1)^{i+j}M_{ij}$

* **行列式展开：**

  * 引理：$n$阶行列式如果第$i$行所有元素除$a_{ij}$外都为零，则行列式等于$a_{ij}$与它的代数余子式的乘积，即$D=a_{ij}A_{ij}$
  * **定理2：**行列式等于它的任一行(列)的各元素与其对应的代数余子式乘积之和，即$D=\sum_{j=1}^n a_{ij}A_{ij}(i=1,2,\cdots,n)$或$D=\sum_{i=1}^n a_{ij}A_{ij}(j=1,2,\cdots,n)$
  * 范德蒙德行列式：$D_{n}=\left|\begin{array}{cccc} 1 & 1 & \cdots & 1 \\ x_1 & x_2 & \cdots & x_n \\ x_1^2 & x_2^2 & \cdots & x_n^2 \\ \vdots & \vdots & & \vdots  \\  x_1^{n-1} & x_2^{n-1} & \cdots & x_n^{n-1}   \end{array} \right| =\underset{n\geq i > j \geq 1}{\prod} (x_i-x_j)$
  * 推论：行列式某一行(列)的元素与另一行(列)的对应元素的代数余子式乘积之和等于零
  * 代数余子式的性质：
    * $\sum_{k=1}^{n}a_{ki}A_{kj}=\begin{cases} D& i=j,\\ 0& i\neq j \end{cases}$
    * $\sum_{k=1}^{n}a_{ik}A_{jk}=\begin{cases} D& i=j,\\ 0& i\neq j \end{cases}$

---

## 2. 矩阵及其运算

* **非齐次线性方程组的矩阵：**
  * $Ax=b,B=(A,b)$
  * $A$系数矩阵，$x$未知数矩阵，$b$常数项矩阵，$B$增广矩阵
* **一些特殊矩阵：**
  * 对角矩阵：$A=diag(\lambda_1,\lambda_2,\cdots,\lambda_n)$
  * 单位阵：$E$
  * 对称矩阵：$A^T=A$
* **矩阵运算：**
  * 矩阵加法：
    * $A+B=B+A$
    * $(A+B)+C=A+(B+C)$
  * 数乘：
    * $(\lambda \mu)A=\lambda (\mu A)$
    * $(\lambda+ \mu)A=\lambda A+\mu A$
    * $\lambda(A+B)=\lambda A+\lambda B$
  * 矩阵乘法：
    * $(AB)C=A(BC)$
    * $\lambda (AB)=(\lambda A)B=A(\lambda B)$
    * $A(B+C)=AB+AC,(B+C)A=BA+CA$
    * $EA=AE=A$
    * $A^kA^l=A^{k+l},(A^k)^l=A^{kl}$
  * 转置：
    * $(A^T)^T=A$
    * $(A+B)^T=A^T+B^T$
    * $(\lambda A)^T=\lambda A^T$
    * $(AB)^T=B^TA^T$
* **方阵的行列式：**
  * $|A^T|=|A|$
  * $|\lambda A|=\lambda^n|A|$
  * $|AB|=|A||B|$
  * $|AB|=|BA|$
* **伴随矩阵：**
  * $A^*=\left( \begin{matrix} A_{11} & A_{21} & \cdots & A_{n1} \\ A_{12} & A_{22} & \cdots & A_{n2} \\ \vdots & \vdots & & \vdots \\ A_{1n} & A_{2n} & \cdots & A_{nn} \end{matrix} \right)$
  * $AA^*=A^*A=|A|E$
* **逆矩阵：**
  * **定理1：** 若矩阵$A$可逆，则$|A|\neq 0$
  * **定理2：** $A^{-1}=\frac{1}{|A|}A^{*}$
  * 奇异矩阵：$|A|=0$
  * 非奇异矩阵：$|A|\neq 0$
  * 运算：
    * $(A^{-1})^{-1}=A$
    * $(\lambda A)^{-1}=\frac{1}{\lambda}A^{-1}$
    * $(AB)^{-1}=B^{-1}A^{-1}$
    * $(A^T)^{-1}=(A^{-1})^T$
* **矩阵多项式：**
  * 如果$A=P\Lambda P^{-1}$，则$A^k=P\Lambda^k P^{-1}$，$\varphi(A)=P\varphi(\Lambda)P^{-1}$
  * $\Lambda=diag(\lambda_1,\lambda_2,\cdots,\lambda_n)$，则$\Lambda^k=diag(\lambda_1^k,\lambda_2^k,\cdots,\lambda_n^k)$，$\varphi(\Lambda)=diag(\varphi(\lambda_1),\varphi(\lambda_2),\cdots,\varphi(\lambda_n))$
* **克拉默法则：**
  * 如果线性方程组$$ \begin{equation} \begin{cases} a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1, \\ a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2, \\ \cdots\cdots\cdots \\ a_{n1}x_1+a_{n2}x_2+\cdots+a_{nn}x_n=b_n \end{cases}  \end{equation}  $$的系数矩阵$A$的行列式不为零，那么方程组有唯一解$$x_1=\frac{A_1}{A},x_2=\frac{A_2}{A},\cdots,x_n=\frac{A_n}{A}$$
    * $$A_j=\left( \begin{matrix} a_{11} & \cdots & a_{1,j-1} & b_1 & a_{1,j+1} & \cdots & a_{1n} \\ \vdots&&\vdots&\vdots&\vdots&&\vdots \\a_{n1} & \cdots & a_{n,j-1} & b_n & a_{n,j+1} & \cdots & a_{nn} \end{matrix} \right)$$ 
* **矩阵分块法：**
  * $A=\left( \begin{matrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{matrix} \right)$，$A^T=\left( \begin{matrix} A_{11}^T & A_{12}^T \\ A_{21}^T & A_{22} ^T\end{matrix} \right)$
  * 分块对角矩阵：
    * $A=\left( \begin{matrix} A_{1} & & & O \\ & A_{2} & & \\ &&\ddots&\\ O &&&A_s  \end{matrix} \right),|A|=|A_1||A_2|\cdots|A_s| $
    * $ A^{-1}=\left( \begin{matrix} A_{1}^{-1} & & & O \\ & A_{2}^{-1} & & \\ &&\ddots&\\ O &&&A_s^{-1}  \end{matrix} \right)$   
  * 按列分块：$A=(a_1,a_2,\cdots,a_n),a_{j} =\left( \begin{array}{c} a_{1j}\\a_{2j}\\ \vdots\\ a_{mj} \end{array} \right)$
  * 按行分块：$A =\left( \begin{array}{c} \alpha_1^T \\\alpha_2^T\\ \vdots\\ \alpha_m^T\end{array} \right),\alpha_i^T=(a_{i1},a_{i2},\cdots,a_{in} )$ 
  * $A=(a_{ij})_{m\times s},B=(b_{ij})_{s\times n},C=(c_{ij})_{m\times n},c_{ij}=\alpha_{i}^Tb_{j}$  

---

## 3. 矩阵的初等变换与线性方程组

* **矩阵的初等变换：**

  1. 对换两行(列)
  2. 以数$k\neq 0$乘以某一行(列)中的所有元
  3. 把某一行(列)所有元的$k$倍加到另一行(列)对应的元上

* **矩阵的等价关系：**

  * 矩阵$A$经有限次初等变换变成矩阵$B$，称矩阵$A$与$B$等价，记作$A\sim B$
  * 性质：
    * 反身性：$A\sim A$
    * 对称性：$A\sim B \Rightarrow B\sim A$
    * 传递性：$A\sim B,B\sim C\Rightarrow A\sim C$

* **行阶梯形矩阵：**

  * 非零矩阵
  * 非零行在零行的上面
  * 非零行的首非零元所在列在上一行的首非零元所在列的右面

* **行最简形矩阵：**

  * 行阶梯形矩阵
  * 非零行的首非零元为1
  * 首非零元所在的列的其他元均为0

* **标准形矩阵：**

  * 左上角是一个单位矩阵，其余元全为0

  > 利用初等行变换，能把一个矩阵化为行阶梯形矩阵和行最简形矩阵；加上初等列变换能化成标准形矩阵

* **初等变换的性质：**

  * **定理1：**设$A$与$B$为$m\times n$矩阵,那么
    * $A \overset{r}{\sim}B$ 的充分必要条件是存在$m$阶可逆矩阵$P$,使$PA=B$
    * $A \overset{c}{\sim}B$ 的充分必要条件是存在$n$阶可逆矩阵$Q$,使$AQ=B$
    * $A\sim B$ 的充分必要条件是存在$m$阶可逆矩阵$P$及$n$阶可逆矩阵$Q$,使$PAQ= B$
  * 初等矩阵：$E$经过一次初等变换得到的矩阵
  * 性质1：设$A$是一个$m\times n$矩阵，对$A$施行一次初等行变换，相当于在$A$的左边乘相应的$m$阶初等矩阵；对$A$施行一次初等列变换，相当于在$A$的右边乘相应的$n$阶初等矩阵
  * 性质2：方阵A可逆的充分必要条件是存在有限个初等矩阵$P_1,P_2,\cdots,P_i$，使$A=P_1P_2\cdots P_i$ 
  
* **矩阵的秩：**

  * $k$阶子式：在$m\times n$矩阵$A$中，任取$k$行与$k$列($k\leq m,k\leq n$)，位于这些行列交叉处的$k^2$个元素，不改变它们在$A$中所处的位置次序而得的$k$阶行列式，称为矩阵$A$的$k$阶子式
  * 设在矩阵$A$中有一个不等于0的$r$阶子式$D$，且所有$r+1$阶子式（如果存在的话）全等于0，那么$D$称为矩阵$A$的最高阶非零子式，数$r$称为矩阵$A$的秩，记作$R（A）$，并规定零矩阵的秩等于 0
  * **定理2：**若$A\sim B$， 则$R(A)=R(B)$
  * 矩阵秩的性质：
    1. $0\leq R(A_{m\times n})\leq min\{m,n\}$
    2. $R(A^T)=R(A)$
    3. 若$A\sim B$，则$R(A)=R(B)$
    4. 若$P,Q$可逆，则$R(PAQ)=R(A)$ 
    5. $max\{R(A),R(B)\}\leq R(A,B)\leq R(A)+R(B)$ 
    6. $R(A+B)\leq R(A)+R(B)$
    7. $R(AB)\leq min\{R(A),R(B)\}$
    8. 若$A_{m\times n}B_{n\times l},$则$R(A)+R(B)\leq n$ 
  * 矩阵乘法的消去律：设$AB=O$，若$A$为列满秩矩阵，则$B=O$

* **线性方程组的解：**

  * **定理3：**n 元线性方程组$Ax=b$

    1. 无解的充分必要条件是$R(A)<R(A,b)$

    2. 有惟一解的充分必要条件是$R(A)=R(A,b)=n$ 
    3. 有无限多解的充分必要条件是$R(A)=R(A,b)<n$ 

  * **定理4：**n元齐次线性方程组$Ax =0$有非零解的充分必要条件是$R(A)<n$

  * **定理5：**线性方程组$Ax=b$有解的充分必要条件是$R(A)=R(A,b)$

  * **定理6：**矩阵方程$AX=B$有解的充分必要条件是$R(A)=R(A,B)$ 

  * **定理7：**设$AB=C$，则$R(C)\leq min\{R(A),R(B)\}$ 

---

## 4. 向量组的线性相关性

* **向量组及其线性组合：**

  * 向量组：若干个同维数的列向量（或同维数的行向量）所组成的集合叫做向量组
  * 线性组合：
    * 给定向量组$A:a_1,a_2,\cdots,a_m$，对于任何一组实数$k_1,k_2,\cdots,k_m$，表达式$$k_1a_1+k_2a_2+\cdots+k_ma_m$$称为向量组$A$的一个**线性组合**，$k_1,k_2,\cdots,k_m$称为这个**线性组合的系数**
    * 给定向量组$A:a_1,a_2,\cdots,a_m$和向量$b$，若存在一组数$\lambda_1,\lambda_2,\cdots,\lambda_m$，使$b=\lambda_1a_1+\lambda_2a_2+\cdots+\lambda_ma_m$，则向量$b$是向量组$A$的线性组合，这是称向量$b$能由向量$A$线性表示
      * 向量$b$能由向量组$A$线性表示，也就是方程组$$x_1a_1+x_2a_2+\cdots+x_ma_m=b$$有解
  * **定理1：**向量$b$能由向量组$A:a_1,a_2,\cdots,a_m$线性表示的充分必要条件是矩阵$A=(a_1,a_2,\cdots,a_m)$的秩等于矩阵$B=(a_1,a_2,\cdots,a_m,b)$的秩
  * 设有两个向量组$A:a_1,a_2,\cdots,a_m$及$B:b_1,b_2,\cdots,b_l$若$B$组中的每个向量都能由向量组$A$线性表示，则称向量组$B$能由向量组$A$线性表示。若向量组$A$与向量组$B$能**相互线性表示**，则称这两个**向量组等价**
  * **定理2：**向量组$B:b_1,b_2,\cdots,b_l$能由向量组$A:a_1,a_2,\cdots,a_m$线性表示的充分必要条件是矩阵$A=(a_1,a_2,\cdots,a_m)$的秩等于矩阵$(A,B)=(a_1,a_2,\cdots,a_m,b_1,b_2,\cdots,b_l)$的秩，即$R(A)=R(A,B)$ 
  * 向量组$A:a_1,a_2,\cdots,a_m$与向量组$B:b_1,b_2,\cdots,b_l$等价的充分必要条件是$R(A)=R(B)=R(A,B)$ 
  * **定理3：**设向量组$B:b_1,b_2,\cdots,b_l$能由向量组$A:a_1,a_2,\cdots,a_m$线性表示，则$R(b_1,b_2,\cdots,b_l)\leq R(a_1,a_2,\cdots,a_m)$ 

* **向量组与矩阵的对应：**

  * 向量组$B:b_1,b_2,\cdots,b_l$能由向量组$A:a_1,a_2,\cdots,a_m$线性表示（几何语言）
  * $\Longleftrightarrow$有矩阵$K$，使$B=AK$（矩阵语言）
  * $\Longleftrightarrow$方程$AX=B$有解（矩阵语言）
  * 充分必要条件：$R(A)=R(A,B)$
  * 必要条件$R(A)\geq R(B)$ 

* **向量组的线性相关性：**

  * **线性相关：**给定向量组$A:a_1,a_2,\cdots,a_m$，如果存在不全为零的数$k_1,k_2,\cdots,k_m$，使$$k_1a_1+k_2a_2+\cdots+k_ma_m=\mathbf{0}$$，则称向量组$A$是**线性相关**的，否则称它**线性无关**
    * 向量组$A$线性相关，也就是在向量组$A$中至少有一个向量能由其余$m-1$个向量线性表示
  * **定理4**：向量组$A:a_1,a_2,\cdots,a_m$线性相关的充分必要条件是它所构成的矩阵$A:(a_1,a_2,\cdots,a_m)$的秩小于向量个数$m$；向量组$A$线性无关的充分必要条件是$R(A)=m$
  * **定理5：**
    1. 若向量组$A:a_1,a_2,\cdots,a_m$**线性相关**，则向量组$B:a_1,a_2,\cdots,a_m,a_{m+1}$也**线性相关**；反之，若向量组$B$**线性无关**，则向量组$A$也**线性无关**
    2. $m$个$n$维向量组成的向量组，当维数$n$小于向量个数$m$时一定**线性相关**。特别地$n+1$个$n$维向量一定线性相关
    3. 若向量组$A:a_1,a_2,\cdots,a_m$**线性无关**，而向量组$B:a_1,a_2,\cdots,a_m,b $ **线性相关**，则向量$b$必能由向量组$A$**线性表示**，且表示式是惟一的

* **向量组的秩：**

  * **最大线性无关向量组：**设有向量组$A$，如果在$A$中能选出$r$个向量$a_1,a_2,\cdots,a_r$，满足：

    1. 向量组$A_0:a_1,a_2,\cdots,a_r$线性无关
    2. 向量组$A$中任意$r+1$个向量都线性相关

    那么称向量组$A_0$是向量组$A$的一个最大线性无关向量组，最大无关组所含向量个数$r$称为向量组$A$的秩，记作$R_A$ 

    * 向量组$A$和它自己的最大无关组$A_0$是**等价**的
    * 能与向量组自身**等价**的**线性无关部分组**一定是最大无关组

  * **最大无关组的等价定义：**设向量组$A_0:a_1,a_2,\cdots,a_r$是向量组$A$的一个部分组，且满足：

    1. 向量组$A_0$线性无关
    2. 向量组$A$的任一向量都能由向量组$A_0$线性表示

    那么向量组$A_0$便是向量组$A$的一个最大无关组

  * **定理6：**矩阵的秩等于它的列向量组的秩，也等于它的行向量组的秩

  * **定理2'：**向量组$b_1,b_2,\cdots,b_l$能由向量组$a_1,a_2,\cdots,a_m$线性表示的充分必要条件是$$R(a_1,a_2,\cdots,a_m)=R(a_1,\cdots,a_m,b_1,\cdots,b_l)$$ 

    > $R(a_1,a_2,\cdots,a_m)$既可理解为矩阵的秩，也可理解成向量组的秩

  * **定理3'：**若向量组$B$能由向量组$A$线性表示，则$R_B\leq R_A$ 

* **线性方程组的解的结构：**

  * 解向量的性质：
    * 性质1：若$x=\xi_1,x=\xi_2$为向量方程$Ax=0$的解，则$x=\xi_1+\xi_2$也是该向量方程的解
    * 性质2：若$x=\xi_1$为向量方程$Ax=0$的解，$k$为实数，则$x=k\xi_1$也是该向量方程的解
  * 基础解系：齐次线性方程组的解集的最大无关组称为该齐次线性方程组的基础解系
  * **定理7：**设$m\times n$矩阵$A$的秩$R(A)=r$，则$n$元齐次线性方程组$Ax=0$的解集$S$的秩$R_S=n-r$ 
    * $Ax=0$与$Bx=0$同解$\Rightarrow$ $R(A)=R(B)$
    * $Ax=0$与$(A^TA)x=0$同解$\Rightarrow R(A^TA)=R(A)$ 
  * 性质3：设$x=\eta_1$及$x=\eta_2$都是向量方程$Ax=b$的解，则$x =\eta_1-\eta_2$为对应的齐次线性方程组$Ax=0$的解
  * 性质4：设$x=\eta$是方程$Ax=b$的解，$x=\xi$是方程$Ax=0$的解，则$x=\xi+\eta$仍是方程$Ax=b$的解
  * 非齐次线性方程的解的结构：
    * 非齐次方程的通解=对应的齐次方程的通解+非齐次方程的一个特解

* **向量空间：**

  * **向量空间：**设$V$为$n$维向量的集合，如果集合$V$非空，且集合$V$对于向量的加法及数乘两种运算封闭，那么就称集合$V$为向量空间

  * 由向量组$a_1,a_2,\cdots,a_m$所生成的向量空间为$L=\{x=\lambda_1a_1+\lambda_2a_2+\cdots+\lambda_ma_m|\lambda_1,\lambda_2,\cdots,\lambda_m\in\mathbb{R}\}$ 

  * **基和维数：**设$V$为向量空间，如果$r$个向量$a_1,a_2,\cdots,a_r\in V$，且满足

    1. $a_1,a_2,\cdots,a_r$线性无关
    2. $V$中任一向量都可由$a_1,a_2,\cdots,a_r$线性表示

    则$a_1,a_2,\cdots,a_r$称为向量空间$V$的一个基，$r$称为向量空间$V$的维数，并称$V$为$r$维向量空间

  * **坐标：**如果在向量空间$V$中取定一个基$a_1,a_2,\cdots,a_r$，那么$V$中任一向量$x$可唯一地表示为$$x=\lambda_1a_1+\lambda_2a_2+\cdots+\lambda_ra_r$$，数组$\lambda_1,\lambda_2,\cdots,\lambda_r$称为向量$x$在基$a_1,a_2,\cdots,a_r$中的坐标

  * 自然基：$n$维向量空间$\mathbb{R}^n$中的取单位坐标向量组$e_1,e_2,\cdots,e_n$为基

  * 基变换和坐标变换：

    * 在$\mathbb{R}$中取两个基$a_1,a_2,a_3$和$b_1,b_2,b_3$，设$A=(a_1,a_2,a_3)$，$B=(b_1,b_2,b_3)$，向量$x$在两个基中的坐标分别为$y_1,y_2,y_3$和$z_1,z_2,z_3$
    * 基变换公式：$(b_1,b_2,b_3)=(a_1,a_2,a_3)P$ 
      * $P=A^{-1}B$称为从旧基到新基的过渡矩阵
    * 坐标变换公式：$\left (\begin{array}{c} z_1 \\ z_2 \\ z_3 \end{array} \right )= P^{-1} \left (\begin{array}{c} y_1 \\ y_2 \\ y_3 \end{array} \right ) $ 

---

## 5. 相似矩阵及二次型

* **向量的内积：**

  * 定义：设有$n$维向量$x=\left (\begin{array}{c} x_1 \\ x_2 \\ \vdots \\ x_n \end{array} \right ),y=\left (\begin{array}{c} y_1 \\ y_2 \\ \vdots \\ y_n \end{array} \right )$  ，$x$与$y$的内积为$[x,y]=x^Ty=x_1y_1+x_2y_2+\cdots+x_ny_n$ 
  * 内积的性质：
    1. $[x,y]=[y,x]$
    2. $[\lambda x,y]=\lambda [x,y]$
    3. $[x+y,z]=[x,z]+[y,z]$
    4. 当$x=0$时，$[x,x]=0$；当$x\neq 0$时，$[x,x]>0$

* **向量的长度(范数)：** 

  * 定义：$\|x\|=\sqrt{[x,x]}=\sqrt{x^2_1+x^2_2+\cdots+x^2_n}$
  * 性质：
    * 非负性：$||x||\geq0$
    * 齐次性：$\| \lambda x \|=|\lambda| \| x  \|$  
  * 单位向量：$\|x\|=1$
  * 单位化：若$a\neq0$，取$x=\frac{a}{\|a\|}$
  * 向量的夹角：当$x\neq 0,y\neq 0$时，$\theta = arccos\frac{[x,y]}{\| x \| \| y \|}$ 
  * 正交：当$[x,y]=0$时，向量$x$与$y$正交；若$x=0$，则$x$与任何向量都正交

* **正交向量组：**

  * **定理1：**若$n$为向量$a_1,a_2,\cdots,a_r$是一组两两正交的非零向量，则$a_1,a_2,\cdots,a_r$线性无关

  * 标准正交基：设$n$维向量$e_1,e_2,\cdots,e_r$是向量空间$V(V\subseteq  R^n)$的一个基，如果$e_1,\cdots,e_r$两两正交，且都是单位向量，则称$e_1,\cdots,e_r$是$V$的一个标准正交基

  * 标准正交化：找一组等价的标准正交基

    * 施密特正交化：

      * 正交化：

        $\begin{equation}
        \begin{array}{l}
        b_{1}=a_{1}, \\
        b_{2}=a_{2}-\frac{\left[b_{1}, a_{2}\right]}{\left[b_{1}, b_{1}\right]} b_{1}, \\
        \ldots \ldots \ldots \ldots \\
        b_{r}=a_{r}-\frac{\left[b_{1}, a_{r}\right]}{\left[b_{1}, b_{1}\right]} b_{1}-\frac{\left[b_{2}, a_{r}\right]}{\left[b_{2}, b_{2}\right]} b_{2}-\cdots-\frac{\left[b_{r-1}, a_{r}\right]}{\left[b_{r-1}, b_{r-1}\right]} b_{r-1}
        \end{array}
        \end{equation}$  

      * 单位化：

        $\begin{equation}
        \boldsymbol{e}_{1}=\frac{1}{\left\|\boldsymbol{b}_{1}\right\|} \boldsymbol{b}_{1}, \boldsymbol{e}_{2}=\frac{1}{\left\|\boldsymbol{b}_{2}\right\|} \boldsymbol{b}_{2}, \cdots, \boldsymbol{e}_{r}=\frac{1}{\left\|\boldsymbol{b}_{r}\right\|} \boldsymbol{b}_{r}
        \end{equation}$

  * 正交矩阵：$n$阶矩阵$A$满足$A^TA=E$
    * 方阵$A$为正交矩阵的充分必要条件是$A$的列(行)向量都是单位向量，且两两正交
    * 性质：
      * 若$A$为正交矩阵，则$A^{-1}=A^T$也是正交矩阵，且$|A|=1$或（-1）
      * 若$A$和$B$都是正交矩阵，则$AB$也是正交矩阵
  * 正交变换：若$P$为正交矩阵，则线性变换$y=Px$称为正交变换
    
    * $\|y\|=\|x\|$ 

* **方阵的特征值与特征向量：**

  * 特征值与特征向量：

    * 设$A$是$n$阶矩阵，如果数$\lambda$和$n$维非零列向量$x$使$Ax=\lambda x$成立，$\lambda$称为矩阵$A$的**特征值**，$x$称为$A$对应于特征值$\lambda$的特征向量

  * 特征方程：$|A-\lambda E|=0$

  * 特征多项式：$|A-\lambda E|$是$\lambda$的$n$次多项式，记作$f(\lambda)$ 

    > $A$的特征值就是特征方程的解，特征方程在复数范围内恒有解，其个数为方程的次数，$n$阶矩阵$A$在复数范围内有$n$个特征值

  * 矩阵的迹：$A$的特征值为$\lambda_1,\lambda_2,\cdots,\lambda_n$，矩阵的迹为$\lambda_1+\lambda_2+\cdots+\lambda_n$ 

    * $\lambda_1+\lambda_2+\cdots+\lambda_n=a_{11}+a_{22}+\cdots+a_{nn}$
    * $\lambda_{1}\lambda_{2}\cdots\lambda_{n}=|A|$ 

  * 性质：

    * 若$p_i$是矩阵$A$的对应于特征$\lambda_i$的特征向量，则$kp_i(k\neq0)$也是对应$\lambda_i$的特征向量
    * 若$\lambda$是$A$的特征值，则$\lambda^k$是$A^k$的特征值；$\varphi(\lambda)$是$\varphi(A)$的特征值

  * **定理2：**设$\lambda_1,\lambda_2,\cdots,\lambda_m$是方阵$A$的$m$个特征值，$p_1,p_2,\cdots,p_m$依次是与之对应的特征向量，如果$\lambda_1,\lambda_2,\cdots,\lambda_m$各不相等，则$p_1,p_2,\cdots,p_m$线性无关

    * 设$\lambda_1$和$\lambda_2$是方阵$A$的两不同特征值，$\xi_1,\xi_2,\cdots,\xi_s$和$\eta_1,\eta_2,\cdots,\eta_l$ 分别是对应于$\lambda_1,\lambda_2$的线性无关的特征向量，则$\xi_1,\xi_2,\cdots,\xi_s,\eta_1,\eta_2,\cdots,\eta_l$线性无关
    * 对应于两个不同特征值的线性无关的特征向量组，合起来仍是线性无关的

* **相似矩阵：**

  * 相似矩阵：$A,B$为$n$阶方阵，有可逆矩阵$P$，使$P^{-1}AP=B$，则$B$为$A$的**相似矩阵**，对$A$进行运算$P^{-1}AP$称为对$A$进行**相似变换**，$P$称为**相似变换矩阵**
  * **定理3：**若$n$阶矩阵$A$与$B$相似，则$A$与$B$的特征多项式相同，从而$A$与$B$的特征值亦相同
  * 若$n$阶矩阵$A$与对角矩阵$\begin{equation}
    \Lambda=\left(\begin{array}{llll}
    \lambda_{1} & & & \\
    & \lambda_{2} & & \\
    & & \ddots & \\
    & & & \lambda_{n}
    \end{array}\right) 
    \end{equation}$ 相似，则$\lambda_1,\lambda_2,\cdots,\lambda_n$即是$A$的$n$个特征值
  * **定理4：**$n$阶矩阵$A$与对角矩阵相似（即$A$能对角化）的充分必要条件是$A$有$n$个线性无关的特征向量
    * 如果$n$阶矩阵$A$的$n$个特征值互不相等，则$A$与对角矩阵相似

* **对称矩阵的对角化：**

  * 对称矩阵的性质：
    * 对称矩阵的特征值为实数
    * 设$\lambda_1,\lambda_2$是对称矩阵$A$的两个特征值，$p_1,p_2$是对应的特征向量。若$λ_1\neqλ_2$，则$p_1$与$p_2$正交
  * **定理5：**设$A$为$n$阶对称矩阵，则必有正交矩阵$P$，使$P^{-1}AP=P^TAP=\Lambda$，其中$\Lambda$是以$A$的$n$个特征值为对角元的对角矩阵
    * 设$A$为$n$阶对称矩阵，$\lambda$是$A$的特征方程的$k$重根，则矩阵$A-\lambda E$的秩$R(A-\lambda E)=n-k$，从而对应特征值$\lambda$恰有$k$个线性无关的特征向量

* **二次型及其标准形：**

  * 二次型：含有n个变量的二元齐次函数$f(x_1,x_2,\cdots,x_n)=a_{11}x_1^2+a_{22}x_2^2+\cdots+a_{nn}x_n^2+2a_{12}x_1x_2+2a_{13}x_1x_3+\cdots+2a_{n-1,n}x_{n-1}x_n$
  * 标准形：$f=k_1y_1^2+k_2y_2^2+\cdots+k_ny_n^2$ 
  * 规范形：标准形的系数$k_1,k_2,\cdots,k_n$只在1，-1，0三个数中取值，使$f=y_1^2+\cdots+y_p^2-y_{p+1}^2-\cdots-y_r^2$ 
  * 复二次型：$a_{ij}$为复数
  * 实二次型：$a_{ij}$为实数
  * 二次型的矩阵表示：$f=x^TAx$，$\begin{equation}
    A=\left(\begin{array}{cccc}
    a_{11} & a_{12} & \cdots & a_{1 n} \\
    a_{21} & a_{22} & \cdots & a_{2 n} \\
    \vdots & \vdots & & \vdots \\
    a_{n 1} & a_{n 2} & \cdots & a_{n n}
    \end{array}\right), x=\left(\begin{array}{c}
    x_{1} \\
    x_{2} \\
    \vdots \\
    x_{n}
    \end{array}\right)
    \end{equation}$ ，$A$为对称矩阵
    * 二次型与对称矩阵之间一一对应
    * 对称矩阵$A$叫做二次型$f$的矩阵
    * $f$称为对称矩阵$A$的二次型
    * 对称矩阵$A$的秩就称为二次型$f$的秩
  
* **合同：**设$A$和$B$是$n$阶矩阵，若有可逆矩阵$C$，使$B=C^TAC$，则称矩阵$A$与$B$合同

  * $A$为对称矩阵，则$B=C^TAC$也为对称矩阵，且$R(B)=R(A)$
  * 经可逆变换$x=Cy$后，二次型$f$的矩阵由$A$变为与$A$合同的矩阵$C^TAC$，且二次型的秩不变
  * **定理6：**任给二次型$f=\sum^n_{i,j=1}a_{ij}x_ix_j(a_{ij}=a{ji})$，总有正交变换$x=Py$，使$f$化为标准形$f=\lambda_1y_1^2+\lambda_2y_2^2+\cdots+\lambda_ny_n^2$，其中$\lambda_1,\lambda_2,\cdots,\lambda_n$是$f$的矩阵$A=(a_{ij})$的特征值
    * 任给$n$元二次型$f(x)=x^TAx(A^T=A)$，总有可逆变换$x=Cz$，使$f(Cz)$为规范形 

* **正定二次型：**

  * **定理7(惯性定理)：**设二次型$f=x^TAx$的秩为$r$，且有两个可逆变换$x=Cy$及$x=Pz$使$f=k_1y_1^2+k_2y_2^2+\cdots+k_ry_r^2(k_i\neq0)$及$f=\lambda_1z_1^2+\lambda_2z_2^2+\cdots+\lambda_rz_r^2(\lambda_i\neq0)$ ，则$k_1,\cdots,k_r$中正数的个数与$\lambda_1,\cdots,\lambda_r$中正数的个数相等 
  * 惯性指数：
    * 二次型的标准形中正系数的个数称为二次型的**正惯性指数**
    * 负系数的个数称为**负惯性指数**
  * 正定二次型：
    * 设二次型$f(x)=x^TAx$，如果对任何$x\neq0$，都有$f(x)＞0$，则称$f$为**正定二次型**，并称对称矩阵$A$是正定的
    * 如果对任何$x\neq0$都有$f(x)＜0$，则称$f$为**负定二次型**，并称对称矩阵$A$是负定的
  * **定理8：**$n$元二次型$f=x^TAx$为正定的充分必要条件是：它的标准形的$n$个系数全为正，即它的规范形的$n$个系数全为 1，亦即它的正惯性指数等于$n$ 
    * 对称矩阵$A$为正定的充分必要条件是：$A$的特征值全为正
  * **定理9(赫尔维茨定理)：**
    * 对称矩阵$A$为正定的充分必要条件是：$A$的各阶主子式都为正
    * 对称矩阵$A$为负定的充分必要条件是：奇数阶主子式为负，而偶数阶主子式为正

  > 设$f(x,y)$是二元正定二次型，则$f(x,y)=c$（c＞0为常数）的图形是以原点为中心的椭圆。当把c看作任意常数时则是一族椭圆，这族椭圆随着c→0而收缩到原点。当$f$为三元正定二次型时，$f(x,y,z)= c(c＞0)$的图形是一族椭球

 