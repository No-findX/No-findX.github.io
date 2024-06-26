---
toc:
    depth_from: 1
    depth_to: 6
    ordered: false
---

<font face = "仿宋">

# <b> <div align="center">多元函数 </div></b>

## <b><div align = "center">平面点集</b></div>
### **点**   
**内点：**对于点P，若存在P的邻域，使得P以及P的邻域属于D，则P称为D的内点,D的所有内点组成的集合称为D的**内部**，记为*intD*   
**外点：**对于点P，若存在P的邻域，使得P的邻域交D为空集，则称P为D的外点   
**界点：**对于点P，若P的邻域内既有D中的点，又有不属于D中的点，则称P为D的界点，所有D的界点组成的集合成为D的**边界**，记作$\partial D$   
**聚点：**对于点P，若P的任意去心邻域内都有D中的点，则称P为D的聚点。***聚点可以属于D，也可以不属于D***   
**孤立点：**P属于D，但存在P的邻域，使得P的去心邻域不属于D    
显然我们有如下结论：   

- 孤立点是界点   
- 内点是聚点   
- 既不是聚点又不是孤立点的点是外点   

**闭包：**点集D与其聚点的并称为闭包，记作$\overline{\text{D}}$    

### **点集**   
**开集：**若D中所有点都是D的内点   
**闭集：**若D的所有聚点都属于D(或D没有聚点)
**连通：**若D中任意两点P、Q可以通过有限折线连接起来，则称D为连通的   
**开域：**连通的开集  
**闭域：**开域以及其边界上的点  

### **平面点集的完备性理论**   

**cauchy收敛准则：**对任意 $\epsilon>0$ ,都存在N，当n>N时，对任意p,有 $d(P_{n+p},P_n)< \epsilon$    

<details>
<summary> cauchy收敛的充分性证明 </summary>
令

$P_n=(x_n,y_n)$   

则有

$$|x_{n+p}-x_n|\leq d(P_{n+p},P_n)< \epsilon,|y_{n+p}-y_n|\leq d(P_{n+p},P_n)< \epsilon$$

所以x,y均收敛，有

$$lim_{n\to \infty}x_n=x,lim_{n\to \infty}y_n=y$$

则有点列P<sub>n</sub>收敛于(x,y)
</details>

**闭域套定理：**设D<sub>n</sub>是非空闭域列且有(1)$D_{n+1}\in D_n$ (2)$d_n=d(D_n),lim_{n\to \infty}d_n=0$,则有唯一的点属于D<sub>n</sub>

**聚点定理：**设D为有界无限点集，则D中至少有一个聚点——有界无限点列一定存在收敛子列    

**有限覆盖定理**(反证)

## **多元函数的极限与连续**
### **多元函数极限**   
**定义**：P<sub>0</sub>为D的一个聚点，若对任意$\epsilon>0$,都存在$\delta>0$,当$P\in U(P_0,\delta)\cap D$,有$|f(P)-A|<\epsilon$,则称A为f在D上，当点P趋向于P<sub>0</sub>时的极限，记为$lim_{P\to P_0}f(P)=A$

<details><summary>求证：

$$lim_{(x,y)\to (2,1)}(x^2+2y^2+2x-1)=9$$

</summary>
讨论1< x< 3,0< y< 2,

$$|x^2+2y^2+2x-1-9|=|(x-2)(x+4)+2(y-1)(y+1)|\leq |x-2||x+4|+2|y-1||y+1|\leq 7\epsilon_1 +6\epsilon_2<\epsilon$$

故存在邻域

$$|x-2|\leq \frac{\epsilon}{13},|y-1|\leq \frac{\epsilon}{13}$$

</details>

<details>
<summary>求证：

$$lim_{(x,y)\to (0,0)}\frac{xy^2}{x^2+y^2}=0$$

</summary>
可以通过基本不等式做即

$$x^2+y^2\geq 2|xy|$$

也可以通过极坐标变换

$$0\leq \frac{xy^2}{x^2+y^2}\leq \frac{|rcos\theta r^2sin^2 \theta|}{r^2}\leq |r|$$

</details>

### **多元函数极限存在的充要条件**   
极限$lim_{P\to P_0}f(P)$存在$\longleftrightarrow$对D的任意子集E，只要$P_0$时E的聚点，必有$lim_{P\to P_0}f(P)=A$   

<details>
<summary><font color = red>e.g.</font>

$$f(x)=\begin{cases}
\frac{xy^2}{x+y} & (x,y)\not=(0,0)\\
0 & (x,y)=(0,0)
\end{cases}$$

</summary>
取

$$x+y=ky^n$$

很容易得到极限不存在。
但是下面下面解法是错误的

$$|xy|\leq \frac{1}{4}(x+y)^2,\frac{xy^2}{x+y}\leq \frac{1}{4}|y(x+y)|=0$$

原因，第一步添加绝对值导致错误
</details>

### **累次极限**   
顾名思义不过多赘述    
**重极限与累次极限并无绝对蕴含关系**

但是可以发现   
**如果重极限与累次极限均存在，则累次极限与重极限相等**   

### **多元函数的连续**   
定义类比一元函数很容易得出    
*全增量*:$\Delta z=f(x+\Delta x,y+\Delta y)-f(x,y)$   
*偏增量*:$\Delta_x z=f(x+\Delta x,y)-f(x,y)$   

**复合函数连续性定理**   
若u=g(x.y),v=q(x,y)在x-y平面内P$(x_0,y_0)$点的邻域内有定义且在P点连续，f(u,v)在u—v平面内Q$(u_0,v_0)$的某邻域内有定义且连续：$u_0=g(x_0,y_0),v_0=q(x_0,y_0)$,则:    
复合函数f(g(x,y),q(x,y))在P点连续。   

### **有界闭区域上连续函数的性质**   

- 最值定理   
- 零点存在定理
- 有界性
- 介质定理
- 一致连续性   

## <b>全微分</b>:  
设y=f(x<sub>1</sub>,x<sub>2</sub>...x<sub>n</sub>)是R<sup>n</sup>的x=(x<sub>10</sub>,x<sub>20</sub>,...,x<sub>n0</sub>)的邻域上有定义的n元函数，若存在A使得

$$ f(x+\Delta x)-f(x)=A\Delta x+o(\sqrt{(\Delta x)^2}) ,\Delta x\rightarrow 0 $$

则记f(x)在x处可微。其线性主要部分即为f在点x处的微分。更进一步的，当$\Delta x_i = 0$(i=2,3,...)时，可以得到

 $$f(x_1+\Delta x_1,x_2,...)-f(x_1,x_2,...)=A_1\Delta x +o(\sqrt{\Delta x^2}) $$

 所以$A_1=\partial f / \partial x_1$ ......<br>

 **函数连续不一定可偏导，不一定可微；可微一定可偏导、连续；偏导数连续则可微**   



</font>
