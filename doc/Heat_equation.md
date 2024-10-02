# [Heat equation](https://en.wikipedia.org/wiki/Heat_equation) & [Diffusion equation](https://en.wikipedia.org/wiki/Diffusion_equation)
$$
    \frac{\partial u}{\partial t} = \alpha (\nabla^2 u) \tag 1 
$$
- 温度/浓度 $u$ 是一个标量
- $\alpha$ 是正的扩散系数, 如果介质不是均质且各向同性的，$\alpha$将不是一个固定系数.
- $\alpha$作为常数考虑时, 可以将 $\alpha$ 幅值藏到 $\partial t$ 中 

## 扩散方程求解
傅里叶变换:
$$
    \mathcal{F}(u(x, t)) = \int_{-\infty}^{+\infty} u(x, t) e^{-ikx} dx \tag2
$$

对等式 (1) 左右两边做傅里叶变换
- 由于傅里叶变换时线性的， 左侧的时间导数可以直接提到积分的外面
$$
    \mathcal{F} \left[ \frac{\partial u(x,t)}{\partial t} \right] = \frac{\partial \tilde{u}(k,t)}{\partial t} 
$$
- 右侧的空间导数带入 (2) 可得
$$
    \mathcal{F} \left[ \frac{\partial^2 u(x,t)}{\partial x^2} \right] = -k^2 \tilde{u}(k,t)  
$$
在频域内可将偏微分方程转为常微分方程
$$
    \frac{\partial \tilde{u}(k,t)}{\partial t} =  -k^2 \tilde{u}(k,t) \tag 3
$$
结合扩散方程的边界条件  
$$
    u(x,0) = \delta(x - x_0) \rightarrow   \tilde{u}(k,0) = e^{-ikx_0} $$
$$
    \tilde{u}(k,t) = e^{-ikx_0} e^{-D k^2 t} 
$$
$$
    u(x,t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} \tilde{u}(k,t) e^{ikx} dk 
$$
对空间向量 $x$ 做傅里叶变换
将 (3) 带入等式 (1) 得到
$$

$$



## Parabola

