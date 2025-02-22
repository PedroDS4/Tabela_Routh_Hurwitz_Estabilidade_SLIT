# **Tabela_Routh_Hurwitz_Estabilidade_SLIT**
Este repositório contempla um projeto que implementa computacionalmente a verificação de estabilidade em um polinômio de grau $n$ qualquer

##**Atividade Modelagem**
**Implementação computacional do cálculo da tabela de Routh-Hurwitz**
Seja um sistema LIT representado pela seguinte função de transferência

$$
G(s) = \frac{N(s)}{D(s)} = \frac{N(s)}{\sum_{j = 0}^{M} a_j \cdot s^j}
$$

dizemos que o sistema é estável se todas as raízes de $D(s)$ estão no semiplano complexo esquerdo, ou seja, todas tem parte real menos que zero.

Para isso existem métodos para verificar a estabilidade desses sistemas, um deles é a tabela de Routh Hurwitz, que nos permite por meio de alguns cálculos verificar se um sistema é BIBO-estável ou não.

A tabela para o polinômio genérico $D(s)$ é dada por

$$
\begin{array}{c|cccc}
s^n & a_n & a_{n-2} & a_{n-4} & \cdots \\
s^{n-1} & a_{n-1} & a_{n-3} & a_{n-5} & \cdots \\
s^{n-2} & c_1 & c_2 & c_3 & \cdots \\
\vdots & \vdots & \vdots & \vdots & \ddots \\
s^1 & \cdot & \cdot & \cdot & \\
s^0 & \cdot & \cdot & \cdot &
\end{array}
$$

onde os termos abaixo das duas primeiras linhas seguem a lógica
$$
c_1 =
\begin{vmatrix}
a_n & a_{n-2} \\
a_{n-1} & a_{n-3}
\end{vmatrix}
$$

Por fim verificamos se há mudança de sinal na primeira coluna da tabela montada, em casa afirmativo dizemos que o sistema não é BIBO-estável e o número de raízes no semi-plano direito é igual ao número de mudanças de sinal.
Em caso negativo, dizemos que o sistema é BIBO-estável.





