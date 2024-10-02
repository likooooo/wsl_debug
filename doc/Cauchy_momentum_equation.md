# Cauchy momentum equation 
[Cauchy momentum equations](https://en.wikipedia.org/wiki/Cauchy_momentum_equation). $\sigma$ 是 [cauchy stress tensor](https://en.wikipedia.org/wiki/Cauchy_stress_tensor)
$$
    \begin{equation}
    \rho \left( \frac{\partial \mathbf{u}}{\partial t} + \mathbf{u} \cdot \nabla \mathbf{u} \right) = \nabla \cdot \boldsymbol{\sigma} + \mathbf{f}
    \end{equation}
$$
$$
    \begin{equation}
    \boldsymbol{\sigma} = 
    \begin{pmatrix}
    \sigma_{xx} & \sigma_{xy} & \sigma_{xz} \\
    \sigma_{yx} & \sigma_{yy} & \sigma_{yz} \\
    \sigma_{zx} & \sigma_{zy} & \sigma_{zz}
    \end{pmatrix}
    \end{equation}
$$

- $\sigma$ 能够描述不可压缩流体 Naviar Stokes equation
$$
\begin{equation}
\sigma_{ij} = -p \delta_{ij} + \tau_{ij}
\end{equation}
$$
$$
\begin{equation}
\tau_{ij} = \mu \left( \frac{\partial u_i}{\partial x_j} + \frac{\partial u_j}{\partial x_i} \right) - \frac{2}{3} \mu (\nabla \cdot \mathbf{u}) \delta_{ij}
\end{equation}
$$

Q : 正定矩阵 $\sigma$可以转为对角矩阵，即: $sigma_{xy}$ 可以分解到 $sigma_{xx}$和 $sigma_{yy}$, 这样是不是说明剪切应力实际上可以用力的分解来替代呢? 
```
不能，因为转为对角矩阵后, 正交基也会发生变化。也就是说在某一组基的视角上确实只存在法向应力, 但是我们在讨论力的时候通常会和其他 term 一起考虑， 那么最后还是要转回到 Cartesian coordinates !
```
## Conservation form 守恒形式