---
toc:
    depth_from: 1
    depth_to: 6
    ordered: false
---

<font face = "仿宋">    

# **logic and proofs 逻辑证明**   

## **propositional logic 命题逻辑**   

**conjunction**:合取——“p $\wedge$ q”即“p and q"   
**disjunction**:析取——“p $\vee$ q”即“p or q”   
**exclusive or**:抑或——“p $\bigoplus$ q”或“p XOR q”   
**hypothesis and conclusion**:“p $\rightarrow$ q”即“if p,then q”    

<details><summary>here is some other ways to say the logic</summary>
 “if p, then q”<br>
 “p implies q”<br>
 “if p, q”     <br>
 “p only if q”   <br>
 “p is sufficient for q”   <br>
 “a sufficient condition for q is p”   <br>
 “q if p”    <br>
 “q whenever p”   <br>
 “q when p”    <br>
 “q is necessary for p”<br>
 “a necessary condition for p is q”     <br>
 “q follows from p”    <br>
 “q unless ¬p”     <br>
 “q provided that p”    
 </details>      

 **biconditional statement**:双条件语句——“p $\leftrightarrow$ q”即“p if and only if q”   

 <details><summary>the same meaning</summary>
 “p is necessary and sufficient for q”<br>
 “if p then q, and conversely”<br>
 “p iff q.”<br> “p exactly when q.”   
 </details>   

### **逻辑优先级**  

 |Operator|Precedence|
 |:------:|:--------:|
 | ¬ | 1 |
 | ∧ | 2 |
 | ∨ | 3 |
 | →  | 4 |
 | ↔  | 5 |   

## **propositional equivalences命题等价**   

**tautology**:一个命题永真 e.g.:p∨¬p   
**contradiction**:一个命题永远为假 e.g.:p∧¬p   
**contingency**:介于上述两者之间的命题 e.g.:p,¬p   
**logically equivalence逻辑等价**:p≡q——p ↔ q is a tautology(永真)     
We can easily say that p→q and ¬p∨q are logically equivalent(using truth table)   
And here are some laws:   

| Equivalence | Laws |
| :---: | :---: |
|p∧T≡p,p∨F≡p | Identity laws|
|p∨T≡T,p∧F≡F | Domination laws|
|p∨p≡p,p∧p≡p | Idempotent laws|
|¬(¬p)≡p | Double negation law|
|p∨q≡q∨p, p∧q≡q∧p | Commutative laws|
|(p∨q)∨r≡p∨(q∨r),(p∧q)∧r≡p∧(q∧r) | Associative laws|
|p∨(q∧r)≡(p∨q)∧(p∨r),p∧(q∨r)≡(p∧q)∨(p∧r) |Distributive laws|
|**¬(p∧q)≡¬p∨¬q,¬(p∨q)≡¬p∧¬q** | **DeMorgan’s laws**|
|p∨(p∧q)≡p,p∧(p∨q)≡p | Absorption laws|
|p∨¬p≡T,p∧¬p≡F | Negation laws|   

**universal quantification**:∀xP(x) means for every x,P(x).If a x makes P(x) false,we say the x is a counterexample(反例) to ∀xP(x).   
**existential quantification**:∃xP(x) means there is a x,P(x).   
So we can find **¬∀xP(x) ≡ ∃x¬P(x)** and **¬∃xQ(x) ≡ ∀x¬Q(x)**