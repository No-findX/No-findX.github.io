<font face ="仿宋"><font size=3>
<h2><b><div align = "center">级数</div></h2></b><br>

<b>定义:</b>给定数列{a<sub>n</sub>},将其每一项通过加号连接起来的表达式，$a_1+a_2+a_3+...$称为无穷级数，若其每一项为常数，称为常数项级数。记作

$$\sum_{i=1}^{\infty}a_i$$

若为函数，则成为函数项级数。
<br>
<b><h3>级数收敛</h3></b>：若级数$\sum_{i=1}^{\infty}a_i$的部分和数列{$s_n$}收敛于S，则称级数$\sum_{i=1}^{\infty}a_i$收敛，其和为S。<br>
<div align ="center"><b><h2>常数项级数</b></div></h2><br>

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
<b><h3>定理1：</h3></b>级数收敛的必要条件：$lim_{n\rightarrow \infty}a_n=0$

<h3><b>级数与反常积分：</h3></b>
构造函数f(x)=a<sub>n</sub>(n<=x<=n+1),则有

$$S_n=\sum_{k=1}^{n}a_k=\sum_{k=1}^{n}\int_{k}^{k+1}f(x)dx=\int_{1}^{n+1}f(x)dx$$

因此，两者有时可同时考虑敛散性。<br>
但是，两者并不等价
- 级数收敛必有 $lim_{n\rightarrow \infty}a_n=0$
- 但是反常积分并将没有以上性质
<br>
<b><h3>定理2：级数收敛的柯西准则:</b></h3>
对于任意$\epsilon>0$,都存在N,对任意n>N,对于任意p,都有$|a_{n+p}+a_{n+p-1}+...+a_n|<\epsilon$

<h3><b>级数的性质</h3></b>

- 线性性质
- 去掉、添加或改变有限项，不影响敛散性
- 收敛添加括号后仍然收敛，且其和不变(原部分和数列子列)--加括号后收敛，脱括号后不一定收敛。不加括号发散，加括号不一定发散

<details>
<summary>判断级数敛散性：

$$\frac{1}{\sqrt{2}-1}-\frac{1}{\sqrt{2}+1}+\frac{1}{\sqrt{3}-1}-\frac{1}{\sqrt{3}+1}+...+\frac{1}{\sqrt{n}-1}-\frac{1}{\sqrt{n}+1}+...$$

</summary>
<b>hint:</b>
对第1、2项，第3、4项...第2n-1、2n项加括号后得到

$$\frac{2}{2-1}+\frac{2}{3-1}+...+\frac{2}{n-1}+...$$

是调和级数，发散，故原级数发散
<br>
</details>

<div align="center"><b><h2>正项级数:</h2></b></div>
<h3><b>定理3:</h3></b>正项级数收敛的充要条件是，其部分和数列有上界
<br>
<details>
<summary><b>证明：</b>调和级数中把含有9的项去掉后收敛</summary>

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
<h3><b>定理4：比较判别法</h3></b>
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

若a<sub>n</sub>收敛，则存在一个N，当n>N时，有a<sub>n</sub><1/n——<font color=red>错误的</font><br>
e.g. 

$$f(x)=\frac{2}{n},n=10^k$$

$$f(x)=\frac{1}{n^2},n\not= 10^k$$

<b><h3>wallis公式</b></h3>

$$lim_{n\rightarrow \infty}\frac{1}{2n+1} (\frac{(2n)!!}{(2n-1)!!})^2=\frac{\pi}{2}$$

<details>
<summary>e.g.5:判断敛散性

$$\sum \frac{(2n)!}{2^{2n}(n!)^2}$$

</summary>

$$a_n=\frac{(2n)!}{2^{2n}(n!)^2}=\frac{(2n)!}{(2n!!)^2}=\frac{(2n-1)!!}{2n!!}=\frac{1}{2n} \frac{(2n-1)!!}{(2n-2)!!}$$

故发散
</details>