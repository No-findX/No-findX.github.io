---
toc:
  depth_from: 1
  depth_to: 6
  ordered: false

---
<font face ="仿宋"><font size=3>

# <div align="center">**级数**</div>  

<b>定义:</b>给定数列{a<sub>n</sub>},将其每一项通过加号连接起来的表达式，$a_1+a_2+a_3+...$称为无穷级数，若其每一项为常数，称为常数项级数。记作

$$\sum_{i=1}^{\infty}a_i$$

若为函数，则成为函数项级数。
<br>

## **级数收敛**：
若级数$\sum_{i=1}^{\infty}a_i$的部分和数列{$s_n$}收敛于S，则称级数$\sum_{i=1}^{\infty}a_i$收敛，其和为S。<br>
## <div align ="center">**常数项级数**</div><br>

<details>
<summary><b>e.g.1</b>:判断级数的敛散性：

$$\sum_{k=1}^{\infty} \frac{1}{k(k+1)(k+2)...(k+p)}$$

</summary>
<br>
<b>hint:</b>

$$\frac{1}{k(k+1)(k+2)...(k+p)}=\frac{1}{p} (\frac{1}{k(k+1)...(k+p-1)}-\frac{1}{(k+1)(k+2)...(k+p)})$$

所以

$$lim_{n\rightarrow \infty}\sum_{i=1}^{n}a_n=\frac{1}{p*p!}$$
</details>
<br>
<details>
<summary><b>e.g.2</b>:判断级数敛散性，并求其和：

$$\sum_{i=1}^{\infty}arctan\frac{1}{2n^2}$$
</summary>
<b>hint:</b>

$$arctanx-arctany=arctan\frac{x-y}{1+xy}$$<br>
$$arctan\frac{1}{2n^2}=arctan\frac{1}{2n-1}-arctan\frac{1}{2n+1}$$

<br></details>

### **定理1：级数收敛的必要条件：**  
$lim_{n\rightarrow \infty}a_n=0$

### **级数与反常积分：** 
构造函数f(x)=a<sub>n</sub>(n<=x<=n+1),则有

$$S_n=\sum_{k=1}^{n}a_k=\sum_{k=1}^{n}\int_{k}^{k+1}f(x)dx=\int_{1}^{n+1}f(x)dx$$

因此，两者有时可同时考虑敛散性。<br>
但是，两者并不等价
- 级数收敛必有 $lim_{n\rightarrow \infty}a_n=0$
- 但是反常积分并将没有以上性质
<br>

### **定理2：级数收敛的柯西准则:**  
对于任意$\epsilon>0$,都存在N,对任意n>N,对于任意p,都有$|a_{n+p}+a_{n+p-1}+...+a_n|<\epsilon$

### **级数的性质**  

- 线性性质
- 去掉、添加或改变有限项，不影响敛散性
- 收敛添加括号后仍然收敛，且其和不变(原部分和数列子列)--加括号后收敛，脱括号后不一定收敛。不加括号发散，加括号不一定发散

<details>
<summary>判断级数敛散性：

$$\frac{1}{\sqrt{2}-1}-\frac{1}{\sqrt{2}+1}+\frac{1}{\sqrt{3}-1}-\frac{1}{\sqrt{3}+1}+...+\frac{1}{\sqrt{n}-1}-\frac{1}{\sqrt{n}+1}+...$$

</summary>
** hint: **
对第1、2项，第3、4项...第2n-1、2n项加括号后得到

$$\frac{2}{2-1}+\frac{2}{3-1}+...+\frac{2}{n-1}+...$$

是调和级数，发散，故原级数发散
<br>
</details>

## <div align="center">**正项级数:**</div>
### **定理3:单调有界**  
正项级数收敛的充要条件是，其部分和数列有上界  

<details>
<summary> 证明: 调和级数中把含有9的项去掉后收敛</summary>

一位数中不含九的：8种<br>
二位数中不含九的：8*9种(十位数有8种选择，个位数有9种选择)<br>
三位数中不含九的：8*9*9种<br>
...<br>
n位数中不含九的：$8*9^{n-1}$种<br>
所以，

$$1+\frac{1}{2}+\frac{1}{3}+...+\frac{1}{8}<8$$

<br>

$$\frac{1}{10}+\frac{1}{11}+...+\frac{1}{88}<\frac{8*9}{10}$$

<br>
<div align ="center"><b>......</b><br></div>

$$\frac{1}{10^n}+\frac{1}{10^n+1}+...+\frac{1}{8...8}<\frac{8*9^n}{10^n}$$

<br>
所以，原式小于

$$\sum_{i=0}^{\infty} 8*(\frac{9}{10})^i$$

<br>
</details>

<details>
<summary><b>e.g.3</b></summary>
<b>已知</b>

$$a_1=1,a_{n+1}=\frac{1}{2}(a_n+\frac{1}{a_n})$$

证明：（1）数列a<sub>n</sub>收敛（2）级数收敛

$$\sum_{n=1}^{\infty} \frac{a_n}{a_n+1}-1$$

<b>解：</b>1.可知a<sub>n</sub>>=1;且

$$a_{n+1}-a_n=\frac{1-2*{a_n}^2}{2*a_n}<0$$

所以其单调递减有下界，所以其收敛,且极限为1<br>
2.

$$ S_n=\sum_{k=1}^{n} \frac{a_n}{a_{n+1}}-1<=\frac{1}{a_{n+1}} \sum_{k=1}^{n}(a_n-a_{n+1})=\frac{1}{a_{n+1}}(a_1-a_{n+1})<=2 $$

所以收敛
<br>
</details>

### **定理4：比较判别法**  

<ul><li>对于正项级数a<sub>n</sub>,b<sub>n</sub>,若存在 N, 对任意n>N,有a<sub>n</sub><b<sub>n</sub>，则:<ol>
  <li>若b收敛，则a收敛</li>
  <li>若a发散，则b发散</li>
  </ol>
<li>若 

$$lim_{n\rightarrow \infty}\frac{a_n}{b_n}=m$$

则：<ol>
<li>若

$$0 < m < \infty,$$

则a<sub>n</sub>,b<sub>n</sub>同敛散</li>
<li>若

$$m=0,$$

若b<sub>n</sub>收敛，则a<sub>n</sub>收敛</li>
<li>若

$$m=\infty,$$

若a<sub>n</sub>收敛，则b<sub>n</sub>收敛</li></ol></ul>
<br>
<details>
<summary><font color = red>e.g.4:</font>判断p级数的敛散性</summary>

<ul><li>当p=1时，调和级数，发散</li>
<li>当p < 1时，有

$$ \frac{1}{n^p}>\frac{1}{n}$$

发散</li>
<li>当p>1时，
<ol><li>由Lagrange中值定理，考虑函数

$$f(x)=\frac{1}{x^{p-1}}$$
$$f(n+1)-f(n)=\frac{1}{(n+1)^{p-1}}-\frac{1}{n^{p-1}}=\frac{1-p}{(n+\theta)^p}$$
$$\frac{1}{(n+1)^p}<\frac{1}{p-1}(\frac{1}{n}-\frac{1}{n+1})$$

之后进行累和，根据比较判别法，收敛</li>
<li>令

$$\frac{1}{2^{p-1}}=r$$

有：

$$\frac{1}{2^p}+\frac{1}{3^p}<2*\frac{1}{2^p}=r$$
$$\frac{1}{4^p}+\frac{1}{5^p}+\frac{1}{6^p}+\frac{1}{7^p}<4*\frac{1}{4^p}=r^2$$
$$...$$
$$\frac{1}{(2^n)^p}+\frac{1}{(2^n+1)^p}+...+\frac{1}{(2^{n+1})*p}<2^n*\frac{1}{(2^n)^p}=r^n$$

因此，

$$S_n< S_{2^n-1}< 1+r+...+r^{n-1}< \frac{1}{1-r}$$

故收敛</li></ol>
</details>

注意：请善用泰勒展开进行敛散性的判别。
<details>
<summary>判断

$$\sum{a^\frac{1}{n}+a^{-\frac{1}{n}}-2}$$

的敛散性</summary>
由泰勒展开可知

$$a^x=e^{xlna}=1+xlna+\frac{1}{2}(xlna)^2+...+\frac{1}{n!}(xlna)^n+...$$
$$a^\frac{1}{n}=1+\frac{1}{n}lna+\frac{1}{2}(\frac{1}{n}lna)^2+\frac{1}{3!}(\frac{1}{n+\theta}lna)^3$$
$$a^{-\frac{1}{n}}=1-\frac{1}{n}lna+\frac{1}{2}(\frac{1}{n}lna)^2-\frac{1}{3!}(\frac{1}{n-\theta}lna)^3$$

所以原式等价于二阶调和，故收敛
</details>

若a<sub>n</sub>收敛，则存在一个N，当n>N时，有a<sub>n</sub><1/n——<font color=red>错误的,足够稀疏</font><br>
e.g. 

$$f(x)=\frac{2}{n},n=10^k$$

$$f(x)=\frac{1}{n^2},n\not= 10^k$$

### **wallis公式**

$$lim_{n\rightarrow \infty}\frac{1}{2n+1} (\frac{(2n)!!}{(2n-1)!!})^2=\frac{\pi}{2}$$

<details>
<summary>e.g.5:判断敛散性

$$\sum \frac{(2n)!}{2^{2n}(n!)^2}$$

</summary>

$$a_n=\frac{(2n)!}{2^{2n}(n!)^2}=\frac{(2n)!}{(2n!!)^2}=\frac{(2n-1)!!}{2n!!}=\frac{1}{2n} \frac{(2n-1)!!}{(2n-2)!!}$$

故发散
</details><br>
<details>
<summary>e.g.6:

$$a_n=\int_{0}^{\frac{\pi}{4}}tan^nxdx$$

{补充桥}(1)求a<sub>n</sub>+a<sub>n+2</sub>的值(2)证明级数收敛：

$$\lambda > 0,\sum_{n=1}^{\infty}\frac{a_n}{n^\lambda}$$

</summary>
(1)

$$\int_{0}^{\frac{\pi}{4}}tan^nx+tan^{n+2}xdx=\int_{0}^{\frac{\pi}{4}}tan^nx(1+tan^2x)dx=\int_{0}^{\frac{\pi}{4}}tan^nxdtanx=\left.\frac{tan^{n+1}x}{n+1}\right|_0^{\frac{\pi}{4}}=\frac{1}{n+1}$$

(2)比较判别法

$$\frac{1}{2n-2}>a_n>\frac{1}{2n+2}$$<br>
$$lim_{n\rightarrow \infty}\frac{\frac{a_n}{n^{\lambda}}}{\frac{1}{n^{\lambda+1}}} \rightarrow lim_{n\rightarrow \infty}\frac{n^{\lambda+1}}{2n(n^\lambda)}=\frac{1}{2}$$

</details>

### **定理5：正项级数的比值判别**

$$lim_{n\rightarrow \infty}\frac{a_{n+1}}{a_n}=l$$

(1)l< 1,级数收敛<br>
(2)l>1,级数发散<br>

<details>
<summary>e.g.7:讨论级数敛散性

$$\sum_{n=1}^{\infty}\frac{a^n*n!}{n^n}$$

</summary>
令

$$b_n=\frac{a^n*n!}{n^n}$$  
$$lim_{n\rightarrow \infty}\frac{b_{n+1}}{b_n}=\frac{an^n}{(n+1)^n}=\frac{a}{e}$$  

当a< e时，收敛；当a>=e时，发散  
</details>

### **定理6：根值判别法**   
若有

$$lim_{n\rightarrow \infty}\sqrt[n]{a_n}=p$$  

1. 当p> 1时，级数发散   
2. 当p< 1时，级数收敛  

<details>
<summary>e.g.8:求级数的敛散性

$$\sum_{n=1}^{\infty}\frac{(n+1)^2}{3^n}$$

</summary>
不给出证明，级数收敛
</details>

### **定理7：积分判别法**  
设函数f(x)在x>1时单调递减，且对任意x >= 1,有f(x)>0,则级数
$\sum_{n=1}^{\infty}f(n)$
与广义积分
$\int_{1}^{\infty}f(x)dx$
有相同的敛散性  

<details>
<summary>证明：</summary>

$$f(k+1)\leq f(x)\leq f(k)$$  
$$f(k+1)\leq \int_k^{k+1}f(x)dx\leq f(k)$$  
$$\sum_{k=1}^{n-1}f(k+1)\leq \int_1^{n} f(x)dx\leq \sum_{k=1}^{n-1}f(k)$$  

</details>

<details>
<summary>e.g.9:判断级数敛散性

$$\sum_{n=2}^{\infty}\frac{1}{nln^pn}$$

</summary>
由积分判别法易得p>1,收敛；p<=1,发散    
<br>
进而讨论

$$\sum_{n=2}^{\infty}\frac{1}{n^plu^qn}$$

的敛散性<br>
当p>1时,有N，当n>N,有如下关系

$$p=1+2\alpha$$  
$$\frac{1}{n^{1+2\alpha}ln^qn}=\frac{1}{n^{1+\alpha}}\frac{1}{n^\alpha ln^qn}\leq \frac{1}{n^{1+\alpha}}$$

易得收敛；<br>
当p<1时，我们可以发现：

$$p=1-\alpha$$  
$$\frac{1}{n^{1-\alpha}ln^qn}=\frac{1}{n}\frac{n^{\alpha}}{ln^qn}\geq \frac{1}{n}$$

所以发散;<br>
当p=1时，同上

</details>

> 思考   
> 1. 正项级数：a<sub>n+1</sub>/a<sub>n</sub>,级数收敛——错；   
> 2. $|\frac{a_{n+1}}{a_n}|\geq 1$ 级数发散——对；  
> 3. 若正项级数收敛，则存在a>0,满足 $lim_{n\to \infty}n^{1+a}a_n=c>0$ ——错；

## <div align="center">**一般项级数**</div>   

### **交错级数**
若 $a_n>0$ ,则取 $\sum_{n=1}^{\infty}(-1)^{n-1}a_n$ 为交错级数，实为

$$a_1-a_2+a_3-a_4+...+a_{2n-1}-a_{2n}+...$$

### **定理8：leibniz判别**
若交错级数 $\sum(-1)^{n-1}a_n$ 满足如下条件   
1. $a_n>0$   
2. $a_n$单调递减   
3. $lim_{n\to \infty}a_n=0$  
则有交错级数收敛且 $S\leq a_1$

<details>
<summary>

$$\sum_{n=2}^{\infty} \frac{(-1)^n}{\sqrt{n}+(-1)^n}$$

</summary>

$$\frac{(-1)^n}{\sqrt{n}+(-1)^n}=\frac{(-1)^n[\sqrt{n}-(-1)^n]}{n-1}=(-1)^n\frac{\sqrt{n}}{n-1}-\frac{1}{n-1}$$

</details>