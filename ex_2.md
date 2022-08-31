# 2. Hãy giải bài toán tối ưu hóa sau sử dụng ít nhất 2 cách khác nhau


$$\min 3 x_1 + 2 x_2 \\ \text{s.t. } x_1^2 - 2 x_1 + x_2^2 = 3$$

## Cách 1: Sử dụng phương pháp nhân tử Lagrange:

$$L(x_1, x_2, \lambda) = 3x_1 + 2x_2 + \lambda ( x_1^2 - 2 x_1 + x_2^2 - 3)$$


$$\begin{cases} \dfrac{\partial L}{\partial x_1}=0 \\ \dfrac{\partial L}{\partial x_2}=0 \\ \dfrac{\partial L}{\partial \lambda}=0 \end{cases}$$

$$\iff \begin{cases} \dfrac{\partial L}{\partial x_1}=3 + 2\lambda x_1 - 2\lambda=0 \\ \dfrac{\partial L}{\partial x_2}=2 + 2\lambda x_2=0 \\ \dfrac{\partial L}{\partial \lambda}=x_1^2 - 2 x_1 + x_2^2 - 3=0 \end{cases}$$

$$\iff \begin{cases} x_1 = \dfrac{2\lambda - 3}{2\lambda} \\ x_2 = - \dfrac{1}{\lambda} \\ x_1^2 - 2 x_1 + x_2^2 - 3=0 \end{cases}$$

$$\dfrac{(2\lambda - 3)^2}{(2\lambda)^2}-2 \dfrac{2\lambda -3}{2\lambda} + \dfrac{1}{\lambda^2}-3=0 \\
\iff \dfrac{4\lambda^2 - 12\lambda + 9 - 8\lambda^2 + 12\lambda + 4 - 12\lambda^2}{4\lambda^2}=0 \\ \iff -16\lambda^2-20\lambda + 25=0$$