# Questionário: Introdução às Matrizes

### Questão 1

No contexto da álgebra linear, o que é uma matriz?

- A) Uma lista unidimensional de variáveis inteiras organizadas em colunas.
- B) Um arranjo retangular de valores escalares organizados em linhas e colunas.
- C) Uma função exponencial utilizada apenas na área de cálculo avançado.
- D) Uma sequência de equações algébricas dependentes sem representação gráfica.

**Resposta Correta:** B  
> **Justificativa:** No contexto da álgebra linear, uma matriz é compreendida como um arranjo retangular de valores escalares dispostos em linhas e colunas.

### Questão 2

Na notação formal de uma matriz $A = [a_{ij}]$ de ordem $m \times n$, o que indicam os elementos $i$ e $j$?

- A) $i$ representa o número total de elementos e $j$ o valor máximo.
- B) $i$ representa a coluna e $j$ representa a linha do elemento.
- C) $i$ representa a linha e $j$ representa a coluna do elemento.
- D) $i$ representa o determinante e $j$ o escalar multiplicador.

**Resposta Correta:** C  
> **Justificativa:** Em $a_{ij}$, o índice $i$ representa a $i$-ésima linha e o índice $j$ representa a $j$-ésima coluna onde o elemento se encontra.

### Questão 3

Considere a matriz $A = \begin{pmatrix} -2 & 10 & -7 & 0 \\ 3 & 1 & -5 & -1 \end{pmatrix}$. Qual é o valor do elemento $a_{1,3}$?

- A) $0$
- B) $3$
- C) $-5$
- D) $-7$

**Resposta Correta:** D  
> **Justificativa:** O elemento $a_{1,3}$ localiza-se na 1ª linha e 3ª coluna da matriz $A$. Olhando para a matriz, o elemento nessa posição é $-7$.

### Questão 4

O que especifica a ordem de uma matriz?

- A) O valor da soma de todos os seus elementos.
- B) O par ordenado que indica o número de linhas ($m$) e de colunas ($n$), denotado por $m \times n$.
- C) Apenas a quantidade de elementos contidos na diagonal principal.
- D) O determinante resultante da multiplicação de suas linhas.

**Resposta Correta:** B  
> **Justificativa:** A ordem de uma matriz refere-se ao par ordenado que especifica o número de linhas ($m$) e o número de colunas ($n$), denotado por $m \times n$.

### Questão 5

Uma matriz $A_{m \times n}$ é classificada como **quadrada** quando:

- A) Possui mais linhas do que colunas ($m > n$).
- B) O número de linhas é igual ao número de colunas ($m = n$).
- C) Todos os seus elementos são maiores que zero.
- D) O número de colunas é o dobro do número de linhas ($n = 2m$).

**Resposta Correta:** B  
> **Justificativa:** A matriz é classificada como quadrada quando $m = n$ , ou seja, o número de linhas é igual ao número de colunas.

### Questão 6

Uma matriz de ordem $m \times 1$ que possui apenas uma coluna é denominada:

- A) Matriz linha.
- B) Matriz retangular.
- C) Matriz coluna.
- D) Matriz nula.

**Resposta Correta:** C  
> **Justificativa:** Uma matriz coluna é aquela que possui apenas uma coluna, ou seja, ordem $m \times 1$.

### Questão 7

Qual é a ordem da matriz $M = \begin{pmatrix} 1 & 0 & 0 & 1 & \sqrt{2} \\ 2 & 3 & -1 & 4 & \sqrt{3} \\ 9 & 0,1 & \pi & 0 & -3 \end{pmatrix}$?

- A) $5 \times 3$
- B) $3 \times 5$
- C) $3 \times 3$
- D) $5 \times 5$

**Resposta Correta:** B
> **Justificativa:** A matriz $M$ possui $3$ linhas e $5$ colunas. Portanto, sua ordem é $3 \times 5$.

### Questão 8

Duas matrizes $A = [a_{ij}]$ e $B = [b_{ij}]$ são consideradas iguais se, e somente se:

- A) Tiverem ordens diferentes, mas a soma de seus elementos for idêntica.
- B) Ambas forem quadradas e tiverem elementos não nulos na diagonal principal.
- C) Possuírem a mesma ordem $m \times n$ e todos os seus elementos correspondentes forem iguais ($a_{ij} = b_{ij}$).
- D) A transposta de $A$ for igual à matriz nula de $B$.

**Resposta Correta:** C  
> **Justificativa:** Duas matrizes são iguais se, e somente se, possuírem a mesma ordem $m \times n$ e todos os seus elementos correspondentes forem iguais ($a_{ij} = b_{ij}$).

### Questão 9

Sobre a **matriz nula**, é correto afirmar que:

- A) É uma matriz cujos elementos da diagonal principal são iguais a $1$ e os demais iguais a $0$.
- B) É uma matriz em que todos os elementos são iguais a zero.
- C) Apenas matrizes quadradas podem ser matrizes nulas.
- D) Atua como elemento neutro exclusivamente na multiplicação matricial.

**Resposta Correta:** B  
> **Justificativa:** Uma matriz nula possui todos elementos iguais a zero, atuando como elemento neutro na adição e na subtração de matrizes.

### Questão 10

Qual é o valor da norma de Frobenius da matriz $A = \begin{pmatrix} 0 & 9 \\ 5 & -2 \\ 0 & -1 \end{pmatrix}$?

- A) $\sqrt{110}$
- B) $110$
- C) $\sqrt{111}$
- D) $111$

**Resposta Correta:** C
> **Justificativa:** Aplicando a fórmula $\|A\|_F = \sqrt{0^2 + 9^2 + 5^2 + (-2)^2 + 0^2 + (-1)^2} = \sqrt{81 + 25 + 4 + 1} = \sqrt{111} \approx 10{,}53$.

### Questão 11

Dada uma matriz $A$ de ordem $m \times n$, qual será a ordem da sua **matriz transposta** $A^T$?

- A) $m \times n$
- B) $n \times m$
- C) $m \times m$
- D) $n \times n$

**Resposta Correta:** B  
> **Justificativa:** A matriz transposta $A^T$ de uma matriz $A_{m \times n}$ é obtida trocando linhas por colunas, resultando em uma ordem $n \times m$.

### Questão 12

Qual é a transposta da matriz $A = \begin{pmatrix} 0 & 9 \\ 5 & -2 \\ 0 & -1 \end{pmatrix}$?

- A) $A^T = \begin{pmatrix} 9 & 0 \\ -2 & 5 \\ -1 & 0  \end{pmatrix}$
- B) $A^T = \begin{pmatrix} 9 & -2 & -1 \\ 0 & 5 & 0 \end{pmatrix}$
- C) $A^T = \begin{pmatrix} 0 & 5 & 0 \\ 9 & -2 & -1 \end{pmatrix}$
- D) $A^T = \begin{pmatrix} 0 & -1 \\ 5 & -2 \\ 0 & 9 \end{pmatrix}$

**Resposta Correta:** C
> **Justificativa:** A primeira linha de $A$ $(0, 9)$ passa a ser a primeira coluna de $A^T$, a segunda linha de $A$ $(5, -2)$ passa a ser a segunda coluna de $A^T$ e a terceira linha de $A$ $(0, -1)$ passa a ser a terceira coluna de $A^T$.

### Questão 13

Uma matriz quadrada $A$ é dita **simétrica** quando satisfaz qual relação?

- A) $A = -A$
- B) $A = A^T$
- C) $A = 0$
- D) $A^T = I$

**Resposta Correta:** B  
> **Justificativa:** Matriz simétrica é uma matriz quadrada que é igual à sua própria transposta, ou seja, $A = A^T$.

### Questão 14

Em uma matriz quadrada de ordem $n$, os elementos $a_{ij}$ que pertencem à **diagonal principal** cumprem qual condição?

- A) $i + j = n + 1$
- B) $i > j$
- C) $i < j$
- D) $i = j$

**Resposta Correta:** D  
> **Justificativa:** A diagonal principal de uma matriz quadrada compreende o conjunto de elementos $a_{ij}$ onde $i = j$ (ex.: $a_{11}, a_{22}, \ldots, a_{nn}$).

### Questão 15

Uma matriz quadrada em que todos os elementos fora da diagonal principal são nulos é chamada de:

- A) Matriz triangular superior.
- B) Matriz diagonal.
- C) Matriz linha.
- D) Matriz escalar.

**Resposta Correta:** B  
> **Justificativa:** A matriz diagonal é definida como uma matriz quadrada em que todos os elementos fora da diagonal principal são nulos.

### Questão 16

Qual é a característica fundamental de uma **matriz triangular superior**?

- A) Todos os elementos acima da diagonal principal são iguais a zero.
- B) Todos os elementos abaixo da diagonal principal são nulos ($a_{ij} = 0$ para $i > j$).
- C) Todos os elementos da diagonal principal são iguais a $1$.
- D) Todos os seus elementos são estritamente positivos.

**Resposta Correta:** B  
> **Justificativa:** Em uma matriz triangular superior, todos os elementos abaixo da diagonal principal são nulos, ou seja, $a_{ij} = 0$ para $i > j$.

### Questão 17

O que define uma **matriz unitária** (ou **matriz identidade** $I_n$)?

- A) Matriz quadrada com todos os elementos iguais a $1$.
- B) Matriz retangular cujos elementos da diagonal secundária valem $1$.
- C) Matriz quadrada em que todos os elementos da diagonal principal são iguais a $1$ e os demais são $0$.
- D) Matriz nula multiplicada por $1$.

**Resposta Correta:** C  
> **Justificativa:** Uma matriz unitária/identidade é uma matriz quadrada em que todos os elementos da diagonal principal são iguais a $1$ e todos os demais são $0$.

### Questão 18

Qual é a condição obrigatória para que seja possível realizar a **adição** ou a **subtração** entre duas matrizes?

- A) Ambas devem ser matrizes quadradas.
- B) Ambas devem possuir a mesma ordem.
- C) O número de linhas de uma deve ser igual ao número de colunas da outra.
- D) Nenhuma das matrizes pode conter elementos nulos.

**Resposta Correta:** B  
> **Justificativa:** A adição e a subtração de matrizes são operações definidas apenas para matrizes de mesma ordem.

### Questão 19

Dadas as matrizes $A = \begin{pmatrix} 0 & -2 \\ 1 & -4 \\ 2 & -6 \end{pmatrix}$ e $B = \begin{pmatrix} -1 & 6 \\ 9 & 0 \\ 3 & -3 \end{pmatrix}$, qual é o resultado da operação $A - B$?

- A) $\begin{pmatrix} 1 & -8 \\ -8 & -4 \\ -1 & -3 \end{pmatrix}$
- B) $\begin{pmatrix} -1 & 8 \\ -8 & 4 \\ -1 & -9 \end{pmatrix}$
- C) $\begin{pmatrix} 1 & 8 \\ 8 & 4 \\ 1 & 3 \end{pmatrix}$
- D) $\begin{pmatrix} -1 & -4 \\ -8 & -4 \\ 1 & 9 \end{pmatrix}$

**Resposta Correta:** A  
> **Justificativa:** A subtração de matrizes é realizada subtraindo elemento a elemento. Assim, teremos: $A - B = \begin{pmatrix} 0 & -2 \\ 1 & -4 \\ 2 & -6 \end{pmatrix} - \begin{pmatrix} -1 & 6 \\ 9 & 0 \\ 3 & -3 \end{pmatrix} = \begin{pmatrix} 0-(-1) & (-2)-6 \\ 1-9 & (-4)-0 \\ 2-3 & (-6)-(-3) \end{pmatrix} = \begin{pmatrix} 1 & -8 \\ -8 & -4 \\ -1 & -3 \end{pmatrix}$.

### Questão 20

Dada a matriz $A = \begin{pmatrix} \sqrt{3} & -1 & 0 \\ -2 & 5 & \sqrt{2} \end{pmatrix}$ e o escalar $k = 3$, qual é a matriz resultante de $k \cdot A$?

- A) $\begin{pmatrix} 3\sqrt{3} & -3 & 0 \\ -6 & 15 & 3\sqrt{2} \end{pmatrix}$
- B) $\begin{pmatrix} 3 & -3 & 0 \\ -6 & 15 & \sqrt{6} \end{pmatrix}$
- C) $\begin{pmatrix} 3\sqrt{3} & 3 & 0 \\ 6 & 15 & 3\sqrt{2} \end{pmatrix}$
- D) $\begin{pmatrix} 6 & 3 & 0 \\ 6 & 15 & \sqrt{6} \end{pmatrix}$

**Resposta Correta:** A
> **Justificativa:** Para encontrar a matriz resultantem, multiplicamos cada elemento de $A$ por $3$: $k \cdot A = 3 \cdot \begin{pmatrix} \sqrt{3} & -1 & 0 \\ -2 & 5 & \sqrt{2} \end{pmatrix} = \begin{pmatrix} 3 \cdot \sqrt{3} & 3 \cdot (-1) & 3 \cdot 0 \\ 3 \cdot (-2) & 3 \cdot 5 & 3 \cdot \sqrt{2} \end{pmatrix} = \begin{pmatrix} 3\sqrt{3} & -3 & 0 \\ -6 & 15 & 3\sqrt{2} \end{pmatrix}$
