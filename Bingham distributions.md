# Bingham distributions in SO(3) space



### 

Bingham分布可以用于对旋转矩阵进行建模。旋转矩阵可以表示为一个特殊的正交矩阵，满足行列式为1，因此可以看做是三个互相垂直的单位向量组成的矩阵。

Bingham分布的概率密度函数可以写成如下形式：
```math
                                                 f(\mathbf{x}; \mathbf{A}) = Z(\mathbf{A}) \exp(\mathbf{x}^\top \mathbf{A} \mathbf{x})  
```
其中，$\mathbf{x}$是一个3维的单位向量，$\mathbf{A}$是一个$3 \times 3$的半正定矩阵，$Z(\mathbf{A})$是一个归一化常数。在旋转矩阵的应用中，我们可以将旋转矩阵的每个列向量归一化得到三个单位向量，然后将它们堆成一个3行3列的矩阵$\mathbf{R}$。然后，我们可以计算出$\mathbf{R}$的3个列向量，分别表示为$\mathbf{r}_1, \mathbf{r}_2, \mathbf{r}_3$，并将它们视为三个向量$\mathbf{x}_1, \mathbf{x}_2, \mathbf{x}_3$，然后我们就可以用Bingham分布来对它们建模，即：
```math
                                 f(\mathbf{r}_1, \mathbf{r}_2, \mathbf{r}_3; \mathbf{A}) = Z(\mathbf{A}) \exp(\mathbf{x}_1^\top \mathbf{A} \mathbf{x}_1 + \mathbf{x}_2^\top \mathbf{A} \mathbf{x}_2 + \mathbf{x}_3^\top \mathbf{A} \mathbf{x}_3) 
```
通过最大似然估计或贝叶斯估计，我们可以求出$\mathbf{A}$的估计值，从而得到一个Bingham分布，用于对旋转矩阵进行建模。


