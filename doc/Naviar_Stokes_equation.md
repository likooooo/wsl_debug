# Cauchy stress tensor
[Navier–Stokes equations](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations)
$v = f(x,y,z,t)$ 的偏微分方程可以用  [Material derivative](Material_derivative.md)  来建模
包含三部分 : 
1. 压强差
2. 粘连项有时也称剪切力, 在某些模型下不存在部分

$$
\frac{Du}{Dt} = \frac{\partial u}{\partial t} + (\mathbf{u} \cdot \nabla)u = \frac{-\nabla P}{\rho} + \nabla \cdot \tau + a \tag 1
$$

## 1. 压强差
压强是一个标量, $\nabla P$ 是一个向量
$$
\nabla P = \begin{pmatrix}
\frac{\partial P}{\partial x} \\
\frac{\partial P}{\partial y} \\
\frac{\partial P}{\partial z}
\end{pmatrix}
$$

## 2. 粘连项
$$
\tau = \mu (\nabla u + \nabla u^T - \frac{2}{3}(\nabla \cdot u)\mathbf{I}) \tag2
$$
TODO : $\tau$ 的推导参考 wiki, 主要用 $ \text{tr}(\boldsymbol{\sigma}) $ 将各个方向力合到一起

由(1), (2) 推出(3)
$$
\frac{Du}{Dt} = \frac{\partial u}{\partial t} + (\mathbf{u} \cdot \nabla)u = \frac{-\nabla P}{\rho} + \mu\nabla^2u + a \tag 3
$$

### laplace operator
Assume the velocity vector field $\mathbf{u}$ is given by:
$\mathbf{u} = (u_x, u_y, u_z)$

The Laplacian operator $\nabla^2$ applied to each component of the velocity vector $\mathbf{u}$ is:
$\nabla^2 \mathbf{u} = \begin{pmatrix} \nabla^2 u_x \\ \nabla^2 u_y \\ \nabla^2 u_z \end{pmatrix}$

where,
$$\nabla^2 u_x = \frac{\partial^2 u_x}{\partial x^2} + \frac{\partial^2 u_x}{\partial y^2} + \frac{\partial^2 u_x}{\partial z^2}$$
$$\nabla^2 u_y = \frac{\partial^2 u_y}{\partial x^2} + \frac{\partial^2 u_y}{\partial y^2} + \frac{\partial^2 u_y}{\partial z^2}$$
$$\nabla^2 u_z = \frac{\partial^2 u_z}{\partial x^2} + \frac{\partial^2 u_z}{\partial y^2} + \frac{\partial^2 u_z}{\partial z^2}$$

## Navier–Stokes equations 是 [Cauchy momentum equation](Cauchy_momentum_equation.md) 特殊形式
stress tensor $\sigma$ 的对角线部分为压强， 非对角线部分是剪切力(粘连项)

