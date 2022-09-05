# 1. Cho $A \in \mathbb{R}^{m\times n}$ và $rank(A)=m$. Xét bài toán tối ưu hóa

$$ \min \dfrac{1}{2} \lVert x \rVert_2^2 \\ \text{s.t. }Ax=y$$

## 1. Hãy chứng minh rằng bài toán tối ưu trên là một bài toán lồi.

Ta chứng minh $f(x)=\dfrac{1}{2} \lVert x \rVert_2^2$ là một hàm lồi.

Ta có $dom(f)=\mathbb{R}^n$ là tập lồi

$$f(x)=\dfrac{1}{2} \lVert x \rVert_2^2=\dfrac{1}{2}x^T x=\dfrac{1}{2}x^T I x$$

Ta tính gradient của $f(x)$ theo $x$:

$$\nabla f(x)=\dfrac{1}{2} \Big\lbrack I + I^T \Big\rbrack x=\dfrac{1}{2}2Ix=x$$

Ta tính ma trận Hessian của $f(x)$ theo $x$:
$$\nabla^2 f(x)=I$$

Ta xét:

$$p^T \nabla^2 f(x) p=p^T I p = p^T p \geq 0 \forall p \in \mathbb{R}^n$$

nên:

$$\nabla^2 f(x) \succeq 0 \forall x \in \mathbb{R}^n$$

Vì $dom(f)$ là tập lồi và $\nabla^2 f(x) \succeq 0$ nên $f(x)=\dfrac{1}{2} \lVert \rVert_2^2$ là một hàm lồi


## 2. Hàm Lagrange của bài toán

$$L(x, v)=f(x) + v^T\Big \lbrack Ax - y \Big \rbrack=\dfrac{1}{2}\lVert x \rVert_2^2 + v^T \Big \lbrack Ax - y \Big \rbrack \text{ (do không có ràng buộc bất đẳng thức) } v \in \mathbb{R}^m$$

## 3. Các điều kiện KKT của bài toán là:


$$\begin{cases} 0 \in \partial \Big ( f(x) + v^T\Big \lbrack Ax - y \Big \rbrack \Big) \\ Ax - y = 0 \end{cases}$$

## 4. Từ điều kiện KKT hãy tìm nghiệm tối ưu của bài toán:

$$\begin{cases} 0 \in \partial \Big ( f(x) + v^T\Big \lbrack Ax - y \Big \rbrack \Big) \\ Ax - y = 0 \end{cases} \Leftrightarrow \begin{cases} \nabla f(x) + \nabla \Big ( v^T \Big \lbrack Ax - y \Big \rbrack \Big) = 0\\ Ax - y = 0 \end{cases}$$

$$\begin{cases} x + A^Tv=0 \\ Ax - y = 0 \end{cases} \Leftrightarrow \begin{cases} x = -A^T v \\ Ax = y \end{cases}$$

$$\begin{cases} x = -A^T v \\ - A A^T v =y \end{cases} $$ 

Ta xét hệ phương trình:

$$A A^T v = 0 \Rightarrow v^T A A^T v = 0 \Leftrightarrow (A^T v)^T (A^T v)=0 \Leftrightarrow \lVert A^T v \rVert_2^2 = 0$$

Do $rank(A)=m$ nên các cột của ma trận $A^T$ (các hàng của ma trận $A$) độc lập tuyến tính vậy để $A^T v = 0 \Leftrightarrow v = 0$. Vậy $AA^Tv=0 \Leftrightarrow v =0$ nên các cột của ma trận $AA^T$ độc lập tuyến tính, ta suy ra $A A^T$ khả ngịch

$$ \Rightarrow \begin{cases} x = A^T  (A A^T)^{-1}y \\ v = - (A A^T)^{-1}y \end{cases}$$