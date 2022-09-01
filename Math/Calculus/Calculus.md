## 第一章 极限与连续

### 映射与函数

* **映射：**
  * 定义：
    * 原像
    * 像
  * 类型：单射、满射、一一映射
  * 运算：
    * 逆映射
    * 复合映射
* **函数：**
  * 定义：
    * 自变量
    * 因变量
    * 定义域
    * 值域
  * 特性：
    * 有界性：上界、下界
      * 有界：同时有上界和下界
    * 单调性
    * 奇偶性
    * 周期性
  * 运算：
    * 反函数
    * 复合函数
  * 初等函数：
    * 幂函数：$y=x^\mu$
    * 指数函数：$y=a^x(a>0,a\neq1)$
    * 对数函数：$y=log_a x(a>0,a\neq1)$
    * 三角函数：$y=sin\ x,y=cos\ x,y=tan\ x$
    * 反三角函数：$y=arcsin\ x,y=arccos\ x,y=arctan\ x$ 
    * 常用：
      * 双曲函数：
        * 双曲正弦：$sinh\ x=\frac{e^x-e^{-x}}{2}$ 
        * 双曲余弦：$cosh\ x=\frac{e^x+e^{-x}}{2}$ 

---

### 极限

* **极限：**
  * 数列的极限：
    * 收敛数列：$x_n\rightarrow a (n\rightarrow \infin)$ 
    * 发散数列：$lim_{n\rightarrow \infin}x_n$ 不存在
    * 收敛数列的性质：
      * 唯一性
      * 有界性
      * 保号性：$lim_{n\rightarrow \infin}x_n=a,a>0,$存在正整数$N,$当$n>N$时，$x_n>0$ 
  * 函数的极限：
    * 性质：
      * 唯一性
      * 局部有界性
      * 局部保号性
  * 无穷小和无穷大：
    * 无穷小：极限为零
    * 无穷大：极限不存在
  * 极限的**运算法则**：
    * 两个(有限个)无穷小的和是无穷小
    * 有界函数与无穷小的乘积是无穷小
      * 常数与无穷小的乘积是无穷小
      * 有限个无穷小的乘积是无穷小
    * 符合四则算术运算
    * 复合函数的极限运算法制
  * 极限存在准则：
    * 夹逼准则：$g(x)\leq f(x) \leq h(x),lim\ g(x)=A,lim\ h(x)=A,$则$lim\ f(x)=A$ 
    * 单调有界数列必有极限
      * 函数在某个点的左领域内单调有界，则在该点处的左极限必定存在
  * 无穷小的比较：
    * 高阶无穷小：$lim\frac{\beta}{\alpha}=0,\beta=o(\alpha)$
    * 低阶无穷小：$lim\frac{\beta}{\alpha}=\infin$
    * 同阶无穷小：$lim\frac{\beta}{\alpha}=c\neq0$
    * k阶无穷小：$lim\frac{\beta}{\alpha^k}=c\neq0,k>0$ 
    * 等价无穷小：$lim\frac{\beta}{\alpha}=1,a\sim \beta$  
    * 定理：
      * $\beta\sim\alpha\Leftrightarrow\beta=\alpha+o(\alpha)$ 
      * $\alpha\sim\alpha',\beta\sim\beta'\Rightarrow lim\frac{\beta}{\alpha}=lim\frac{\beta'}{\alpha'}$ 

---

### 连续

* **连续：**
  * 定义：
    * 自变量增量趋于零时，函数对应增量也趋于零
      * $lim_{\Delta x\rightarrow0}\Delta y=lim_{\Delta x\rightarrow0}[f(x_0+\Delta x)-f(x_0)]=0$
    * 极限存在且等于函数值
      * $lim_{x\rightarrow x_0}f(x)=f(x_0)$ 
  * 函数的间断点：
    * 三种情形：
      * 在某点处没有定义
      * 在某点处有定义，但该点处极限不存在
      * 在某点处有定义，极限也存在，但极限值与函数值不相等
    * 分类：
      * 第一类间断点：左右极限都存在的间断点
        * 可去间断点：左右极限相等
        * 跳跃间断点：左右极限不相等
      * 第二类间断点：
        * 无穷间断点
        * 振荡间断点
    * 初等函数在其定义域内都是连续的
    * 闭区间上连续函数的性质：
      * 有界性与最大值最小值定理：在闭区间上连续的函数在该区间上有界且一定能取得它的最大值和最小值
      * 零点定理：函数在某个闭区间上连续，且两个端点的函数值异号，则在该开区间内存在零点
      * 介值定理：函数在某个闭区间上连续，则能在该开区间内取得两个端点的函数值之间的值

---

## 第二章 一元微分学

### 导数

* 导数：
  * 定义：函数的变化率
    * $f'(x_0)=lim_{\Delta x\rightarrow0}\frac{\Delta y}{\Delta x}=lim_{\Delta x\rightarrow0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$ 
  * 单侧导数：
    * 可导的必要条件：左导数和右导数都存在且相等
    * 左导数：$f'_-(x_0)=lim_{\Delta x\rightarrow0^-}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$ 
    * 右导数：$f'_+(x_0)=lim_{\Delta x\rightarrow0^+}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$ 
  * 几何意义：切线斜率
    * 切线方程：$y-y_9=f'(x_0)(x-x_0)$ 
    * 法线方程：$y-y_9=-\frac{1}{f'(x_0)}(x-x_0)$ 
  * 可导性与连续性：
    * 可导必连续
    * 连续不一定可导
  * 求导法则：<img src="Pic/求导法则.jpg" style="zoom: 67%;" />
  * 反函数的求导法则：$[f^{-1}(x)]'=\frac{1}{f'(y)},\frac{\Delta y}{\Delta x}=\frac{1}{\frac{\Delta x}{\Delta y}}$ 
  * 复合函数的求导法则：$\frac{\Delta y}{\Delta x}=f'(u)g'(x),y=f(u),u=g(x)$ 
  * 初等函数导数公式：<img src="Pic/导数公式.jpg" style="zoom: 50%;" />
  * 高阶导数：
    * 莱布尼茨公式：<img src="Pic/高阶导数.jpg" style="zoom:50%;" />
  * 隐函数的导数
    * 对数求导法：先对两边取对数，再求导
  * 参数方程求导：$\frac{\Delta y}{\Delta x}=\frac{\frac{\Delta y}{\Delta t}}{\frac{\Delta x}{\Delta t}}$ 

---

### 微分

* 微分：
  * 定义：
    * $\Delta y=f(x_0+\Delta x)-f(x_0)=A\Delta x+o(\Delta x)$ 
    * $A\Delta x$为$f(x)$在点$x_0$相对于自变量增量$\Delta x$的微分
    * $A=lim_{x_0\rightarrow 0}\frac{\Delta y}{\Delta x}=f'(x_0)$ 
    * $\Delta y=dy+o(dy),dy=f'(x_0)\Delta x$
    * $dy$ 为$\Delta y$ 的线性主部 
  * 可微的充分必要条件是可导
  * 微商：$\frac{dy}{dx}=f'(x)$，函数的微分$dy$与自变量的微分$dx$之商等于该函数的导数，导数也叫微商
  * 几何意义：曲线的切线上点的纵坐标的增量

---

### 导数的应用

* 微分中值定理：
  * 费马引理：函数在$x_0$的某邻域内$U(x_0)$有定义，且在$x_0$处可导，$\forall x\in U(x_0),f(x)\leq f(x_0)(或f(x)\geq f(x_0))$ ，则$f'(x_0)=0$ 
  * 驻点：导数为零的点
  * 罗尔定理：<img src="Pic/罗尔定理.jpg" style="zoom:67%;" />
  * 拉格朗日中值定理：<img src="Pic/拉格朗日中值定理.jpg" style="zoom: 67%;" />
    * 几何意义：弧$AB$上至少有一点的切线平行于弦$AB$
    * 证明：引入辅助函数
      * $\phi(x)=f(x)-f(a)-\frac{f(b)-f(a)}{b-a}(x-a)$
      * $\phi'(x)=f'(x)-\frac{f(b)-f(a)}{b-a}$ 
      * $\phi'(\theta)=0$ 
  * 柯西中值定理：<img src="Pic/柯西中值定理.jpg" style="zoom: 60%;" />
* 洛必达法则：
  * <img src="Pic/洛必达法则1.jpg" style="zoom:60%;" />
  * <img src="Pic/洛必达法则1.jpg" style="zoom:60%;" />
* 泰勒公式：
  * 泰勒公式：
    * 佩亚诺余项：<img src="Pic/泰勒中值定理.jpg" style="zoom: 50%;" />
    * 拉格朗日余项：<img src="Pic/泰勒中值定理2.jpg" style="zoom: 50%;" />
    * 麦克劳林公式：$x_0=0$
      * <img src="Pic/麦克劳林公式1.jpg" style="zoom:50%;" />
      * <img src="Pic/麦克劳林公式2.jpg" style="zoom:50%;" />
  * 意义：
    * 用高阶多项式近似函数
    * 高阶导数与函数相同
* 函数的单调性与曲线的凹凸性：
  * 单调性：<img src="Pic/函数单调性.jpg" style="zoom: 60%;" />
  * 凹凸性：
    * 定义：
      * 凹弧：$f(\frac{x_1+x_2}{2})<\frac{f(x_1)+f(x_2)}{2}$
      * 凸弧：$f(\frac{x_1+x_2}{2})>\frac{f(x_1)+f(x_2)}{2}$ 
      * 拐点：凹凸性改变的点
    * 判定定理：
      * 凹弧：$f''(x)>0$
      * 凸弧：$f''(x)<0$ 
* 极值：
  * 定义：
    * 极大值：领域内$f(x)<f(x_0)$
    * 极小值：领域内$f(x)>f(x_0)$
  * 极值与驻点($f'(x_0)=0$)：
    * 必要条件：$f(x_0)$为极值，则$f'(x_0)=0$
    * 第一充分条件：<img src="Pic/极值第一充分条件.jpg" style="zoom: 50%;" />
    * 第二充分条件：<img src="Pic/极值第二充分条件.jpg" style="zoom: 40%;" />
  * 最值：比较驻点和不可导点
* 曲率：
  * 弧微分公式：$ds=\sqrt{1+y'^2}dx$ 
  * 曲率：度量弯曲程度
    * 单位弧段上切线转过的角度的大小
    * $K=|\frac{d\alpha}{ds}|$ 
    * 圆曲率：$K=\frac{1}{a},a$为半径
  * 曲率计算公式：$K=\frac{|y''|}{(1+y'^2)^{3/2}}$ 
    * $tan\alpha =y'\Rightarrow sec^2\alpha \frac{d\alpha}{dx}=y''\Rightarrow \frac{d\alpha}{dx}=\frac{y''}{1+tan^2\alpha}=\frac{y''}{1+y'^2}\Rightarrow d\alpha =\frac{y''}{1+y'^2}dx$  
    * $ds=\sqrt{1+y'^2}dx$
    * $K=|\frac{d\alpha}{ds}|=\frac{|y''|}{(1+y'^2)^{3/2}}$ 
  * 曲率圆：在凹的一侧法线上距离$\rho=\frac{1}{K}$处取一点做半径为$\rho$的圆
    * 曲率中心：圆心
    * 曲率半径：$\rho$

---

## 第三章 一元函数积分学

### 不定积分

* 原函数：连续函数一定有原函数
* 不定积分：原函数带任意常数项
  * $\int f(x)dx=F(x)+C$ 
  * 性质：
    * 加减法
    * 数乘
* 换元积分法：
  * <img src="Pic/不定积分第一类换元法.jpg" style="zoom:50%;" />
  * <img src="Pic/不定积分第二类换元法.jpg" style="zoom:50%;" />
* 分部积分法：$\int uv'dx=uv-\int u'vdx$ 
* 积分表：教材附录

---

### 定积分

* 定积分：
  * 曲边梯形面积
  * 区域面积
  * 函数值的积累
  * 部分量累加
* 性质：
  * <img src="Pic/定积分性质1.jpg" style="zoom:60%;" />
  * <img src="Pic/定积分性质2.jpg" style="zoom:60%;" />
  * <img src="Pic/定积分性质3.jpg" style="zoom:60%;" />
  * <img src="Pic/定积分性质4.jpg" style="zoom:60%;" />
  * <img src="Pic/定积分性质5.jpg" style="zoom:60%;" />
  * <img src="Pic/定积分性质6.jpg" style="zoom:60%;" />
* 微积分基本定理：$\int^b_a f(x)dx=F(b)-F(a)$ 
* 反常积分：
  * 无穷限的反常积分：上下限为无穷
    * $\int_{-\infin}^{+\infin}f(x)dx$收敛的条件：$\int_{-\infin}^{0}f(x)dx$和$\int_{0}^{+\infin}f(x)dx$均收敛
    * $\int_{-\infin}^{+\infin}f(x)dx=\int_{-\infin}^{0}f(x)dx+\int_{0}^{+\infin}f(x)dx$ 
  * 无界函数的反常积分：瑕点，任一邻域内都无界
* 几何应用：
  * 平面图形的面积
  * 体积
  * 平面曲线的弧长
* 物理应用：
  * 变力沿直线所作的功
  * 水压力
  * 引力

---

## 第四章 微分方程

* 定义：表示未知函数、未知函数的导数与自变量之间的关系的方程
* 微分方程的阶：最高阶导数的阶数
* 微分方程的通解：解中含有任意常数，且任意常数的个数与微分方程的阶数相同
* 微分方程类型：
  * 一阶微分方程：
    * 可分离变量的微分方程：$g(y)dy=f(x)dx$
    * 齐次方程：$\frac{dy}{dx}=\phi(\frac{y}{x}),u=\frac{y}{x},u+x\frac{du}{dx}=\phi(u)$ 
    * 一阶线性微分方程：$\frac{dy}{dx}+P(x)y=Q(x)$ 
      * 齐次：$Q(x)=0,y=Ce^{-\int P(x)dx}$
      * 非齐次：$Q(x)\neq0,y=Ce^{-\int P(x)dx}+e^{-\int P(x)dx}\int Q(x)e^{\int P(x)dx}dx$  
  * 高阶微分方程：
    * 可降阶的高阶微分方程：
      * $y^{(n)}=f(x)$：两边积分
      * $y''=f(x,y'),y'=p,p'=f(x,p),$求$p$再求$y$ 
      * $y''=f(y,y'),y'=p,y''=p\frac{dp}{dy},p\frac{dp}{dy}=f(y,p)$ 
    * 高阶线性微分方程：
      * 二阶线性微分方程：$y''+P(x)y'+Q(x)y=0$ 
      * 常系数齐次线性微分方程：$y''+py'+qy=0,p,q$为常数
        * 特征方程：$r^2+pr+q=0$
        * 两个不等实根：$y=C_1e^{r_1x}+C_2e^{r_2x}$
        * 两个相等实根：$y=(C_1+C_2x)e^{r_1x}$ 
      * 常系数非齐次线性微分方程：$y''+py'+qy=f(x)$ 
        * 先求$y''+py'+qy=0$通解
        * 根据$f(x)$形式用待定系数法求特解
* 应用：数学建模

---

## 第五章 向量代数与空间解析几何

* 向量：
  * $\vec{b}\parallel \vec{a} \Leftrightarrow \vec{b}=\lambda \vec{a},\lambda$ 唯一
  * 混合积：$[\vec a\  \vec b\ \vec c]=(\vec a\times \vec b)\cdot \vec c$ 
* 平面：
  * 平面方程：
    * 点法式方程：$\vec n \cdot \vec{M_0M}=0,\vec n=(A,B,C),\vec{M_0M}=(x-x_0,y-y_0,z-z_0),A(x-x_0)+B(y-y_0)+C(z-z_0)=0$
    * 一般方程：$Ax+By+Cz+D=0$
  * 两平面的夹角：$cos\theta=\frac{|A_1A_2+B_1B_2+C_1C_2|}{\sqrt{A^2_1+B_1^2+C_1^2}{\sqrt{A^2_2+B_2^2+C_2^2}}}$ 
    * 互相垂直：$A_1A_2+B_1B_2+C_1C_2=0$
    * 互相平行或重合：$\frac{A_1}{A_2}=\frac{B_1}{B_2}=\frac{C_1}{C_2}$ 
  * 点到平面的距离公式：$d=\frac{Ax_0+By_0+Cz_0+D}{\sqrt{A^2+B^2+C^2}}$  
* 空间直线：
  * 直线方程：
    * 一般方程：$\begin{equation}
      \left\{\begin{array}{l}
      A_{1} x+B_{1} y+C_{1} z+D_{1}=0 \\
      A_{2} x+B_{2} y+C_{2} z+D_{2}=0
      \end{array}\right.
      \end{equation}$
    * 对称式(点向式)方程：$\frac{x-x_{0}}{m}=\frac{y-y_{0}}{n}=\frac{z-z_{0}}{p}$
    * 参数方程：$\begin{equation}
      \left\{\begin{array}{l}
      x=x_{0}+m t, \\
      y=y_{0}+n t \\
      z=z_{0}+p t
      \end{array}\right.
      \end{equation}$
  * 两直线的夹角：方向向量夹角
  * 直线与平面的夹角：方向向量与法向量的夹角的余角
* 曲面：
  * 旋转曲面：$f(y,z)=0$绕$z$轴旋转一周，$d=\sqrt{x^2+y^2}=|y_1|,f(±\sqrt{x^2+y^2,z})=0$ 
    * 双曲线：旋转单叶双曲面，旋转双叶双曲面
  * 柱面：定曲线→准线，动直线→母线
  * 二次曲面：三元二次方程表示的曲面
* 空间曲线：两个曲面的交线
  * 一般方程：$\begin{equation}
    \left\{\begin{array}{l}
    F(x,y,z)=0 \\ G(x,y,z)=0
    \end{array}\right.
    \end{equation}$ 
  * 参数方程：$\begin{equation}
    \left\{\begin{array}{l}
    x=x(t) \\
    y=y(t) \\
    z=z(t)
    \end{array}\right.
    \end{equation}$   
  * 空间曲线在做坐标面上的投影：消去一个变量

---

## 第六章 多元函数微分学

### 多元函数

* 领域和点集的关系：内点、外点、边界点、聚点(内点+边界点)
* 平面点集：
  * 开集、闭集
  * 连通集：任意两内点都可用折线连接，且折线上的点属于该点集
  * 区域：连通的点集，开区域、闭区域
  * 有界集：$\exist r>0,E \subset U(O,r)$
  * 无界集：非有界集
* 多元函数：
  * 多元函数的极限(二重极限)：$lim_{P\rightarrow P_0}f(P)=A$ ，以任意方式趋近$P_0$时，$f(x,y)$无限接近$A$
  * 多元函数的连续性：$lim_{(x,y)\rightarrow (x_0,y_0)}f(x,y)=f(x_0,y_0)$
  * 性质：
    * 有界性与最小值最大值定理：有界闭区域上的多元连续函数必定有界且有最小值最大值
    * 介质定理：有界闭区域上的多元连续函数必取得介于最小值最大值之间的任何值

---

### 多元函数导数与微分

* 偏导数
  * 定义：固定其它变量，对一个变量的导数，$f_x(x_0,y_0)=\lim _{\Delta x \rightarrow 0} \frac{f\left(x_{0}+\Delta x, y_{0}\right)-f\left(x_{0}, y_{0}\right)}{\Delta x}$
  * 意义：切线对某一个轴的斜率，关于某一个自变量的变化率
  * 偏导函数：$\frac{\part z}{\part x},\frac{\part f}{\part x},z_x,f_x(x,y)$
  * 高阶偏导数
    * 二阶混合偏导数在连续的条件下与求导次序无关
* 全微分：
  * 偏增量：$f(x+\Delta x,y)-f(x,y)$
  * 偏微分：$f_x(x,y)\Delta x$
  * 全增量：$\Delta z=f(x+\Delta x,y+\Delta y)-f(x,y)$ 
  * 可微分：$\Delta z=A\Delta x+B\Delta y+o(\rho),\rho=\sqrt{(\Delta x)^2+(\Delta y)^2},dz=A\Delta x+B\Delta y$ 为全微分
  * 可微分与偏导数：
    * 必要条件：可微分$\Rightarrow$偏导数存在，且$dz=\frac{\part z}{\part x}\Delta x+\frac{\part z}{\part y}\Delta y$
    * 充分条件：偏导数连续$\Rightarrow$可微分
* 多元复合函数求导：
  * 一元函数与多元函数复合：$u=\phi(t),v=\omega(t),z=f(u,v),\frac{dz}{dt}=\frac{\part z}{\part u}\frac{du}{dt}+\frac{\part z}{\part v}\frac{dv}{dt}$ ,$\frac{dz}{dt}$为全导数
  * 多元函数与多元函数复合：$u=\phi(x,y),v=\omega(x,y),z=f(u,v),\frac{dz}{dx}=\frac{\part z}{\part u}\frac{du}{dx}+\frac{\part z}{\part v}\frac{dv}{dx},\frac{dz}{dy}=\frac{\part z}{\part u}\frac{du}{dy}+\frac{\part z}{\part v}\frac{dv}{dy}$ 
* 隐函数求导：
  * 一个方程：
    * $F(x,y)=0,y=f(x) \Rightarrow \frac{dy}{dx}=-\frac{F_x}{F_y}$
    * $F(x,y,z)=0,z=f(x,y)\Rightarrow \frac{\part z}{\part x}=-\frac{F_x}{F_z},\frac{\part z}{\part y}=-\frac{F_y}{F_z}$
  * 方程组

---

### 多元函数微分学的几何应用

* 向量值函数：函数值为向量
* 方向导数与梯度：
  * 方向导数：沿一个方向的变化率，梯度与方向向量积
    * $$\left.\frac{\partial f}{\partial l}\right|_{\left(x_{0} , y_{0}\right)}=f_{x}\left(x_{0}, y_{0}\right) \cos \alpha+f_{y}\left(x_{0}, y_{0}\right) \cos \beta$$ 
  * 梯度：方向导数最大的方向；函数值增加最快的方向；等高线方向
    * $$\operatorname{grad} f\left(x_{0}, y_{0}\right)=\nabla f\left(x_{0}, y_{0}\right)=f_{x}\left(x_{0}, y_{0}\right) i+f_{y}\left(x_{0}, y_{0}\right) j$$ 
    * $\left.\frac{\partial f}{\partial l}\right|_{\left(x_{0} , y_{0}\right)}=grad f(x_0,y_0)\cdot e_l,e_l=(cos\alpha,cos\beta)$   
* 空间曲线：
  * 切向量：某一点处的方向向量
  * 法平面：以切向量为法向量的平面
* 曲面：
  * 法线：梯度
  * 切平面

---

### 极值

* 极值：
  * 必要条件：偏导为0，$f_x(x_0,y_0)=0,f_y(x_0,y_0)=0$ 
  * 充分条件：海森矩阵为正定矩阵，极小值；负定矩阵，极大值
    * $f_{xx}(x_0,y_0)=A,f_{xy}(x_0,y_0)=B,f_{yy}(x_0,y_0)=C$ 
    * $AC-B^2>0$有极值，$A<0$极大值，$A>0$极小值
    * $AC-B^2<0$无极值
    * $AC-B^2=0$不确定
* 条件极值：求$f(x,y)$在$\phi(x,y)=0$条件下的极值，拉格朗日乘子法
  * $L(x,y)=f(x,y)+\lambda \phi(x,y)$
  * $$\left\{\begin{array}{l}f_{x}(x, y)+\lambda \varphi_{x}(x, y)=0 \\ f_{y}(x, y)+\lambda \varphi_{y}(x, y)=0 \\ \varphi(x, y)=0\end{array}\right.$$

---

## 第七章 重积分 

* 二重积分：
  * 定义：微小面积与函数值乘积之和的极限；$\iint_D f(x,y)dxdy,\iint_D f(x,y)d\sigma$
  * 性质：同定积分
  * 计算方法：
    * 化为二次积分：
      * 直角坐标：$\psi_{1}(y) \leqslant x \leqslant \psi_{2}(y),c \leqslant y \leqslant d,\iint_{D} f(x, y) \mathrm{d} \sigma=\int_{c}^{d}\left[\int_{\psi_{1}(y)}^{\psi_{2}(y)} f(x, y) \mathrm{d} x\right] \mathrm{d} y$ 
      * 极坐标：
        * $x=\rho cos\theta,y=\rho sin\theta,dxdy=\rho d\rho d\theta$
        * $\varphi_{1}(\theta) \leqslant \rho \leqslant \varphi_{2}(\theta), \alpha \leqslant \theta \leqslant \beta$
        * $\iint_{D} f(\rho \cos \theta, \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta=\int_{\alpha}^{\beta}\left[\int_{\varphi_{1}(\theta)}^{\varphi_{2}(\theta)} f(\rho \cos \theta, \rho \sin \theta) \rho \mathrm{d} \rho\right] \mathrm{d} \theta$
  * 应用：曲顶柱体的体积，平面薄片的质量
* 三重积分：
  * 定义：微小体积与函数值乘积之和的极限；$\iiint_\Omega f(x,y,z)dxdydz,\iiint_\Omega f(x,y,z)dv$
  * 计算方法：化为三次积分
    * 直角坐标：
      * 坐标投影法：化为二重积分
        * $\iint_{D_{x y}} F(x, y) \mathrm{d} \sigma=\iint_{D_{x y}}\left[\int_{z_{1}(x, y)}^{z_{2}(x, y)} f(x, y, z) \mathrm{d} z\right] \mathrm{d} \sigma$
        * $\iiint_{\Omega} f(x, y, z) \mathrm{d} v=\int_{a}^{b} \mathrm{~d} x \int_{y_{1}(x)}^{y_{2}(x)} \mathrm{d} y \int_{z_{1}(x, y)}^{z_{2}(x, y)} f(x, y, z) \mathrm{d} z$
      * 坐标轴投影/截面法：先二重积分后单积分
    * 柱面坐标：
      * $0 \leqslant \rho<+\infty,0 \leqslant \theta \leqslant 2 \pi,-\infty<z<+\infty$
      * $\left\{\begin{array}{l}x=\rho \cos \theta \\ y=\rho \sin \theta \\ z=z\end{array}\right.$
      * $dv=\rho d\rho d\theta dz$
    * 球面坐标：
      * $0 \leqslant r<+\infty,0 \leqslant \varphi \leqslant \pi,0 \leqslant \theta \leqslant 2 \pi$
      * $\left\{\begin{array}{l}x=r \sin \varphi \cos \theta \\ y=r \sin \varphi \sin \theta \\ z=r \cos \varphi\end{array}\right.$
      * $dv=r^2 sin\varphi dr d\varphi d\theta$

## 第八章 曲线积分与曲面积分

### 曲线积分

* 曲线积分：积分区域为一条曲线
* 对弧长的曲线积分(第一类曲线积分)：微小弧长与函数值乘积之和的极限；线密度
  * 计算：
    * 参数方程：
      * $\left\{\begin{array}{l}x=\varphi(t) \\ y=\psi(t)\end{array} \quad(\alpha \leqslant t \leqslant \beta)\right.$
      * $\int_{L} f(x, y) \mathrm{d} s=\int_{\alpha}^{\beta} f[\varphi(t), \psi(t)] \sqrt{\varphi^{\prime 2}(t)+\psi^{\prime 2}(t)} \mathrm{d} t \quad(\alpha<\beta)$
    * $y=\phi(x)\rightarrow x=t,y=\phi(t)$ 
* 对坐标的曲线积分(第二类曲线积分)：有向曲线弧分别对坐标$x,y$做积分；变力做功
  * $\int_L F(x,y)\cdot dr=\int_L P(x,y)dx + Q(x,y)dy,dr=dxi+dyj$ 
  * 计算：
    * $\left\{\begin{array}{l}x=\varphi(t) \\ y=\psi(t)\end{array} \quad(\alpha \leqslant t \leqslant \beta)\right.$
    * $\begin{aligned} & \int_{\iota} P(x, y) \mathrm{d} x+Q(x, y) \mathrm{d} y \\=& \int_{\alpha}^{\beta}\left\{P[\varphi(t), \psi(t)] \varphi^{\prime}(t)+Q[\varphi(t), \psi(t)] \psi^{\prime}(t)\right\} \mathrm{d} t \end{aligned}$
* 两类曲线积分的关系：$\int_{L} P \mathrm{~d} x+Q \mathrm{~d} y=\int_{L}(P \cos \alpha+Q \cos \beta) \mathrm{d} s$
* 格林公式：在平面闭区域D上的二重积分可以通过沿闭区域D的边界曲线L上的曲线积分来表达
  * 应用：用二重积分来计算曲线积分

---

### 曲面积分

* 对面积曲面积分(第一类曲面积分)：微小面积与函数值乘积之和的极限；面密度
  * 计算：
    * $\begin{aligned} & \iint_{\Sigma} f(x, y, z) \mathrm{d} S \\=& \iint_{D_{x y}} f[x, y, z(x, y)] \sqrt{1+z_{x}^{2}(x, y)+z_{y}^{2}(x, y)} \mathrm{d} x \mathrm{~d} y \end{aligned}$
* 对坐标的曲面积分(第二类曲面积分)：有向曲面分别对坐标$x,y,z$做积分；流向曲面一侧的流量
  * $\iint_{\Sigma} P(x, y, z) \mathrm{d} y \mathrm{~d} z+Q(x, y, z) \mathrm{d} z \mathrm{~d} x+R(x, y, z) \mathrm{d} x \mathrm{~d} y$
  * 计算：化为投影区域的二重积分
* 高斯公式：空间闭区域上的三重积分与其边界曲面上的曲面积分之间的关系
  * $\iiint_{\Omega}\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right) \mathrm{d} v=\oiint_{\Sigma} P \mathrm{~d} y \mathrm{~d} z+Q \mathrm{~d} z \mathrm{~d} x+R \mathrm{~d} x \mathrm{~d} y$
  * 散度：流量密度，流体的源头强度，微小区域单位时间产生的流体质量
    * $\operatorname{div} \boldsymbol{v}(M)=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}$
* 斯托克斯公式：曲面上的曲面积分和边界曲线的曲线积分之间的关系
  * $\iint_{\Sigma}\left|\begin{array}{ccc}\mathrm{d} y \mathrm{~d} z & \mathrm{~d} z \mathrm{~d} x & \mathrm{~d} x \mathrm{~d} y \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R\end{array}\right|=\oint_{\Gamma} P \mathrm{~d} x+Q \mathrm{~d} y+R \mathrm{~d} z$
  * $\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right) \mathrm{d} y \mathrm{~d} z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right) \mathrm{d} z \mathrm{~d} x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right) \mathrm{d} x \mathrm{~d} y$
  * 旋度：闭合曲线的环流量密度
    * $\operatorname{rot} \boldsymbol{A}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right) \boldsymbol{i}+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right) \boldsymbol{j}+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right) \boldsymbol{k}$
  * $\iint_{\Sigma} \operatorname{rot} \boldsymbol{A} \cdot \boldsymbol{n} \mathrm{d} S=\oint_{\Gamma} \boldsymbol{A} \cdot \boldsymbol{\tau} \mathrm{d} s$

---

## 第九章 无穷级数

### 常数项无穷级数

* 无穷级数：
  * 定义：数列求和极限
  * 部分和数列：前n项和构成的数列
  * 级数的和：部分和数列$\{s_n\}$有极限$s$，则无穷级数收敛，极限$s$为级数的和；否则级数发散
  * 收敛级数的性质：
    * <img src="Pic/收敛级数性质1.jpg" style="zoom:50%;" />
    * <img src="Pic/收敛级数性质2.jpg" style="zoom:50%;" />
    * <img src="Pic/收敛级数性质3.jpg" style="zoom:50%;" />
    * <img src="Pic/收敛级数性质4.jpg" style="zoom:50%;" />
    * <img src="Pic/收敛级数性质5.jpg" style="zoom:50%;" />
* 正项级数：各项都是正数或零的级数
  * 性质：
    * 部分和数列单调增加
  * 审敛法：
    * <img src="Pic/正项级数审敛法1.jpg" style="zoom:50%;" />
    * <img src="Pic/正项级数审敛法2.jpg" style="zoom:50%;" />
    * <img src="Pic/正项级数审敛法3.jpg" style="zoom:50%;" />
    * <img src="Pic/正项级数审敛法4.jpg" style="zoom:50%;" />
    * <img src="Pic/正项级数审敛法5.jpg" style="zoom:50%;" />
* 交错级数：各项正负交错
  * 审敛法：
    * <img src="Pic/交错级数审敛法1.jpg" style="zoom:50%;" />
  * 绝对收敛：各项绝对值所构成的正项级数收敛
  * 条件收敛：级数收敛而不绝对收敛
  * 绝对收敛$\Rightarrow$条件收敛
  * 绝对收敛级数的性质：
    * 可交换性。各项交换后仍收敛，和不变
    * 绝对收敛级数之间的乘法，柯西乘积构成的级数收敛，和为原来和的乘积

---

### 函数项级数

* 函数项无穷级数：
  * 收敛点
  * 发散点
  * 收敛域：收敛点的全体
  * 发散域：发散点的全体
  * 和函数：$s(x)$
  * 余项：$s(x)-s_n(x)$
* 幂级数：各项都是常数乘幂函数，$\sum_{n=0}^{\infin}a_nx^n$
  * 系数：常数$a_n$
  * 收敛性：
    * <img src="Pic/幂级数定理1.jpg" style="zoom:50%;" />
    * <img src="Pic/幂级数收敛半径.jpg" style="zoom:50%;" />
    * 收敛半径：$R$
    * 收敛区间：$(-R,R)$ 
    * <img src="Pic/幂级数定理2.jpg" style="zoom:50%;" />
  * 和函数性质：在收敛域上连续、可积、可导
* 泰勒级数：函数展开成幂级数，和函数为原函数
  * 泰勒展开式：<img src="Pic/泰勒展开式.jpg" style="zoom:50%;" />
  * 能展开的充分必要条件：<img src="Pic/泰勒展开条件.jpg" style="zoom:50%;" />
  * 麦克劳林级数和麦克劳林展开式：<img src="Pic/麦克劳林展开式.jpg" style="zoom:50%;" />
  * 应用：
    * 近似计算函数值
    * 解微分方程
    * 欧拉公式：$\mathrm{e}^{x i}=\cos x+i \sin x$
* 三角级数：由三角函数组成的函数项级数
  * 物理意义：把一个复杂的周期运动看成是许多不同频率的简谐振动的叠加
  * 三角级数：
    * $f(t)=A_{0}+\sum_{n=1}^{\infty} A_{n} \sin \left(n \omega t+\varphi_{n}\right)$
    * $\frac{a_{0}}{2}=A_{0}, a_{n}=A_{n} \sin \varphi_{n}, b_{n}=A_{n} \cos \varphi_{n}, \omega=\frac{\pi}{l},T=2l$
    * $\frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left(a_{n} \cos \frac{n \pi t}{l}+b_{n} \sin \frac{n \pi t}{l}\right)$
    * $\frac{\pi t}{l}=x\Rightarrow\frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left(a_{n} \cos n x+b_{n} \sin n x\right)$
* 傅里叶级数：周期函数展开成三角级数
  * $f(x)=\frac{a_{0}}{2}+\sum_{k=1}^{\infty}\left(a_{k} \cos k x+b_{k} \sin k x\right)$，$f(x)$的周期为$2\pi$
  * $\left.\begin{array}{l}a_{n}=\frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos n x \mathrm{~d} x \quad(n=0,1,2,3, \cdots) \\ b_{n}=\frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin n x \mathrm{~d} x \quad(n=1,2,3, \cdots)\end{array}\right\}$
  * 奇函数的傅里叶级数为正弦级数
  * 偶函数的傅里叶级数为余弦级数