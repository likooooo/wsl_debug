# Material derivative
对于标量或向量物理量会随时间和空间变化, 即 $\phi = f(x,y,z,t)$ 的偏微分方程可以用  [Material derivative](https://en.wikipedia.org/wiki/Material_derivative)  来建模：
$$
\frac{D\phi}{Dt} = \frac{\partial \phi}{\partial t} + \mathbf{u} \cdot \nabla\phi
$$
$\phi$ 随时间 $t$ 的变化由以下两部分组成
- 当位置不改变时, 物理量随时间的变化的率 $\frac{\partial \phi}{\partial t}$
- 当位置改变时, 物理量梯度场与速度共同决定了变化的趋势
## Scalar and vector fields
### 标量场
- $\mathbf{u} = (u,v,w)$
$$
\mathbf{u} \cdot \nabla\phi = u \frac{\partial \phi}{\partial u} + v \frac{\partial \phi}{\partial v} + w \frac{\partial \phi}{\partial w}
$$
### 向量场
- $\mathbf{u} = (u,v,w)$
- $\phi = (\phi_x, \phi_y, \phi_z)$
- $\nabla \phi$ 是 [Covariant derivative](https://en.wikipedia.org/wiki/Covariant_derivative)
$$
\mathbf{u} \cdot \nabla\phi =  \begin{pmatrix}
u\frac{\partial \phi_x}{\partial x} + v\frac{\partial \phi_x}{\partial y} + w\frac{\partial \phi_x}{\partial z} \\
u\frac{\partial \phi_y}{\partial x} + v\frac{\partial \phi_y}{\partial y} + w\frac{\partial \phi_y}{\partial z} \\
u\frac{\partial \phi_z}{\partial x} + v\frac{\partial \phi_z}{\partial y} + w\frac{\partial \phi_z}{\partial z} 
\end{pmatrix}
$$  
### Tensor(TODO)
- $\sigma =  \begin{pmatrix} \sigma_xx \end{pmatrix}$
[Upper-convected time derivative](https://en.wikipedia.org/wiki/Upper-convected_time_derivative)
- $ (\mathbf{u} \cdot \nabla)\phi$

- Tensor 的表达式可以应用于 $ \phi $ 是一个向量场的情况, 并且与 $ \mathbf{u} \cdot \nabla \phi$ 等价

## Other names
There are many other names for the material derivative, including:
- advective derivative
- convective derivative
- derivative following the motion
- hydrodynamic derivative
- Lagrangian derivative
- particle derivative
- substantial derivative
- substantive derivative
- Stokes derivative
- total derivative, although the material derivative is actually a special case of the total derivative



$$
\mathbf{u} \cdot \nabla\phi = \sum_{i}^{n} u_i \frac{\partial \phi}{\partial u_i}
$$

## 等价性证明

1. **表达式 $ \mathbf{u} \cdot \nabla \phi $**：
   - 先计算向量场 $ \phi $ 的雅可比矩阵 $ \nabla \phi $。
   - 然后用向量 $ \mathbf{u} $ 与雅可比矩阵 $ \nabla \phi $ 进行点积运算。
   - 结果是一个向量，表示向量场 $ \phi $ 在向量 $ \mathbf{u} $ 方向上的变化率。

2. **表达式 $ (\mathbf{u} \cdot \nabla) \phi $**：
   - $ \mathbf{u} \cdot \nabla $ 是一个方向导数算子，作用在向量场 $ \phi $ 的每个分量上。
   - 结果也是一个向量，表示向量场 $ \phi $ 在向量 $ \mathbf{u} $ 方向上的变化率。

- 结果一致性

对于这两种表达式，最终结果是相同的，并且都是一个向量，表示向量场 $ \phi $ 在向量 $ \mathbf{u} $ 方向上的变化率。

- 示例

假设 $ \mathbf{u} = (u_1, u_2, u_3) $，$ \phi = (\phi_1, \phi_2, \phi_3) $，那么：
$$
\mathbf{u} \cdot \nabla \phi = \begin{pmatrix}
   u_1 \frac{\partial \phi_1}{\partial x} + u_2 \frac{\partial \phi_1}{\partial y} + u_3 \frac{\partial \phi_1}{\partial z}\\
   u_1 \frac{\partial \phi_2}{\partial x} + u_2 \frac{\partial \phi_2}{\partial y} + u_3 \frac{\partial \phi_2}{\partial z}\\
   u_1 \frac{\partial \phi_3}{\partial x} + u_2 \frac{\partial \phi_3}{\partial y} + u_3 \frac{\partial \phi_3}{\partial z}
\end{pmatrix}
$$
