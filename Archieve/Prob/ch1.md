### **概率导论 1 - 样本空间和概率**

### 1 集合

将一些研究对象放在一起，形成**集合**，而这些对象就称为集合的**元素**。设$S$是一个集合，$x$是$S$的元素，我们将元素和集合的这种关系写成$x\in S$。若$x$不是$S$的元素，就写成 $x \notin S$. 一个集合可以没有元素，这个特殊的集合就称为**空集**。

将我们感兴趣的所有元素放在一起，形成一个集合，这个集合称为**空间**，记做$\Omega$。当$\Omega$确定以后，我们所讨论的集合$S$都是$\Omega$的子集。

### 2 概率模型

概率模型是对不确定现象的数学描述。概率模型的基本构成：

* **样本空间**$\Omega$，这是一个试验的所有可能结果的集合。
* **概率律**，概率律为试验结果的集合A（称之为**事件**）确定一个非负数$P(A)$（称为事件A的**概率**)。

#### 概率律

概率律确定了任何结果或者任何结果的集合(称之为事件)的似然程度。更精确一点说，它给每一个事件$A$，确定一个数$P(A)$，称之为事件$A$的概率。

概率公理(Probability axioms):

* 非负性: 对一切事件$A$，满足$P(A)\ge 0$
* 可加性： 若$A$和$B$为互不相容的事件，则它们的并满足$P(A \cup B) = P(A)+P(B)$
* 归一化：整个样本空间$\Omega$的概率为1，即$P(\Omega)=1$

#### 离散模型

**离散概率律**：设样本空间由有限个可能的结果组成，则事件的概率可由组成这个事件的试验结果的概率所决定。事件$\{s_1, s_2,...,s_n\}$的概率是$P(s_i)$之和，即

$$P(\{s_1,s_2,...,s_n\}) = P(s_1)+P(s_1)P(s_2)+P(s_n)$$

**离散均匀概率律(古典概型)**：设样本空间由$n$个等可能性的试验结果组成，因此每个试验结果组成的事件(称为基本事件)的概率是相等的。由此得到

$$P(A) = \frac{\text{含于事件A的试验结果数}}{n}$$


### 3  条件概率

给定$B$发生之下事件$A$的条件概率，记做$P(A|B)$,

$$P(A|B) = \frac{P(A\cap B)}{P(B)}$$

条件概率满足概率的3条公理

* 非负性和归一化是明显的
* 可加性：$P(A_1\cup A_2|B) = P(A_1|B) + P(A_2|B)$


### 4 全概率定理和贝叶斯准则

**全概率定理**：设$A_1, A_2,..., A_n$是一组互不相容的事件，它形成样本空间的一个分割(每一个试验结果必定使得其中一个事件发生!). 又假定对每一个$i, P(A_i)>0$. 则对于任何事件$B$，下列公式成立：
<small>
$$P(B) = P(A_1\cap B) + ...+ P(A_n\cap B) = P(A_1)P(B|A_1) + ...+ P(A_n)P(B|A_n)=\sum P(B|A_i)P(A_i) $$
</small>
**贝叶斯准则**：设$A_1, A_2,..., A_n$是一组互不相容的事件，它形成样本空间的一个分割(每一个试验结果必定使得其中一个事件发生!). 又假定对每一个$i, P(A_i)>0$. 则对于任何事件$B$，只要它满足$P(B)>0$，下列公式成立：

$$P(A_i|B) = \frac{P(A_i)P(B|A_i)}{P(B)} =\frac{P(A_i)P(B|A_i)}{\sum P(A_i)P(B|A_i)} $$

为证明贝叶斯准则，只需注意到$P(A_i)P(B|A_i)$与$P(A_i|B)P(B)$是相等的，它们都等于$P(A_i\cap B)$。



$P(A_i|B)$为由于代表新近得到的信息$B$之后$A_i$出现的概率，称之为**后验概率**，而原来的$P(A_i)$就称为**先验概率**。


### 5 独立性

如果$P(A|B)=P(A)$，则称事件$A$**独立**于事件$B$。即事件$B$的发生并没有给事件$A$带来新的信息，没有改变事件$A$发生的概率。

条件独立：特别地，在给定$C$之下，若事件$A$和事件$B$满足$P(A\cap B|C) = P(A|C)P(B|C)$，则称$A$和$B$在给定$C$之下**条件独立**。






