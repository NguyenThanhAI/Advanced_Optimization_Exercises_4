# 2. Hãy giải bài toán tối ưu hóa sau sử dụng ít nhất 2 cách khác nhau


$$\min 3 x_1 + 2 x_2 \\ \text{s.t. } x_1^2 - 2 x_1 + x_2^2 = 3$$

Đặt $f(x) = 3 x_1 + 2 x_2$

## Cách 1: Sử dụng phương pháp nhân tử Lagrange:

$$L(x_1, x_2, \lambda) = 3x_1 + 2x_2 + \lambda ( x_1^2 - 2 x_1 + x_2^2 - 3)$$


$$\begin{cases} \dfrac{\partial L}{\partial x_1}=0 \\ \dfrac{\partial L}{\partial x_2}=0 \\ \dfrac{\partial L}{\partial \lambda}=0 \end{cases}$$

$$\Leftrightarrow \begin{cases} \dfrac{\partial L}{\partial x_1}=3 + 2\lambda x_1 - 2\lambda=0 \\ \dfrac{\partial L}{\partial x_2}=2 + 2\lambda x_2=0 \\ \dfrac{\partial L}{\partial \lambda}=x_1^2 - 2 x_1 + x_2^2 - 3=0 \end{cases}$$

$$\Leftrightarrow \begin{cases} x_1 = \dfrac{2\lambda - 3}{2\lambda} \\ x_2 = - \dfrac{1}{\lambda} \\ x_1^2 - 2 x_1 + x_2^2 - 3=0 \end{cases}$$

$$\dfrac{(2\lambda - 3)^2}{(2\lambda)^2}-2 \dfrac{2\lambda -3}{2\lambda} + \dfrac{1}{\lambda^2}-3=0 \\
\Leftrightarrow \dfrac{4\lambda^2 - 12\lambda + 9 - 8\lambda^2 + 12\lambda + 4 - 12\lambda^2}{4\lambda^2}=0 \\ \Leftrightarrow -16\lambda^2 + 13=0 \Leftrightarrow \lambda = -\dfrac{\sqrt{13}}{4} \text{ hoặc } \lambda = \dfrac{\sqrt{13}}{4}$$

- Với $\lambda = -\dfrac{\sqrt{13}}{4}$:

$$\Rightarrow \begin{cases} x_1=\dfrac{-2\dfrac{\sqrt{13}}{4} - 3}{-2\dfrac{\sqrt{13}}{4}}=\dfrac{\sqrt{13} + 6}{\sqrt{13}} \\ x_2 = - \dfrac{1}{-\dfrac{\sqrt{13}}{4}}=\dfrac{4}{\sqrt{13}} \\ \lambda = -\dfrac{\sqrt{13}}{4} \end{cases}$$

$$\Rightarrow f(x) = 3 x_1 + 2 x_2 = \dfrac{3\sqrt{13}+18}{\sqrt{13}} + \dfrac{8}{\sqrt{13}}=\dfrac{3\sqrt{13}+26}{\sqrt{13}} =3 + 2\sqrt{13}$$

- Với $\lambda = \dfrac{\sqrt{13}}{4}$:

$$\Rightarrow \begin{cases} x_1 = \dfrac{2 \dfrac{\sqrt{13}}{4}-3}{2 \dfrac{\sqrt{13}}{4}}=\dfrac{\sqrt{13}-6}{\sqrt{13}} \\ x_2 = - \dfrac{1}{\dfrac{\sqrt{13}}{4}}=-\dfrac{4}{\sqrt{13}} \\ \lambda = \dfrac{\sqrt{13}}{4} \end{cases}$$

$$\Rightarrow f(x)=3x_1 + 2 x_2 = \dfrac{3\sqrt{13}-18}{\sqrt{13}}-\dfrac{8}{\sqrt{13}}=\dfrac{3\sqrt{13}-26}{\sqrt{13}}=3-2\sqrt{13}$$

Vậy $f(x)$ đạt giá trị nhỏ nhất tại:

$$\begin{cases} x_1 = \dfrac{\sqrt{13}-6}{\sqrt{13}} \\ x_2 = -\dfrac{4}{\sqrt{13}}\end{cases}$$

và giá trị nhỏ nhất là:

$$\min f(x)=3x_1 + 2 x_2=3 - 2\sqrt{13} \\ \text{s.t. } x_1^2 - 2 x_1 + x_2^2 = 3$$

