# Unidade 1: Álgebra Linear e Vetores em Aprendizado de Máquina
## Questionário

### Questão 1
Qual é a definição matemática fundamental de um escalar?
- A) Uma sequência ordenada de números reais com direção e sentido.
- B) Um único número real ou complexo que indica magnitude.
- C) Uma matriz com apenas uma linha ou uma coluna.
- D) Uma função que transforma vetores de alta dimensão em pontos.

**Resposta Correta:** B
> **Justificativa:** Conforme o material, um escalar é um único número real (ou complexo), como $3$, $-0{,}5$ ou $\pi$, que representa magnitude sem direção.

### Questão 2
No contexto de Aprendizado de Máquina, o que um vetor de características tipicamente representa?
- A) O número total de épocas de treinamento de um modelo preditivo.
- B) A taxa de aprendizado usada pelo algoritmo de otimização.
- C) Uma amostra individual descrita por seus atributos.
- D) A acurácia global obtida por um classificador após o ajuste.

**Resposta Correta:** C
> **Justificativa:** Em Aprendizado de Máquina, um vetor de características representa tipicamente uma amostra (por exemplo, um paciente com $n$ exames ou uma casa com $n$ atributos) ou um conjunto de parâmetros do modelo.

### Questão 3
Considerando o vetor $\mathbf{x} = \begin{pmatrix} -4 & 2 & 9 \end{pmatrix}$, qual é a sua dimensão?
- A) $1$
- B) $2$
- C) $3$
- D) $5$

**Resposta Correta:** C
> **Justificativa:** A dimensão (ou dimensionalidade) de um vetor é o número de elementos ou componentes que ele possui. Como $\mathbf{x}$ possui 3 elementos, sua dimensão é 3 ($\mathbf{x} \in \mathbb{R}^3$).

### Questão 4
Como é denominado um vetor cujos componentes estão dispostos na horizontal?
- A) Vetor coluna
- B) Vetor nulo
- C) Vetor ortogonal
- D) Vetor linha

**Resposta Correta:** D
> **Justificativa:** Quando os elementos de um vetor estão dispostos na horizontal, ele é chamado de vetor linha. Quando estão dispostos na vertical, chama-se vetor coluna.

### Questão 5
Qual é a propriedade fundamental do vetor nulo $\mathbf{0}$?
- A) Todos os seus componentes são iguais a zero.
- B) Ele possui norma $L_2$ igual a $1$.
- C) Ele pode ter dimensões variáveis durante operações de adição.
- D) Seu produto escalar com qualquer outro vetor resulta em $1$.

**Resposta Correta:** A
> **Justificativa:** O vetor nulo, denotado por $\mathbf{0}$, é definido como o vetor em que todos os seus componentes são estritamente iguais a zero.

### Questão 6
Como a norma de um vetor é conceitualmente definida?
- A) Uma função que associa o vetor a um valor não negativo.
- B) A soma escalar dos componentes dividida pela dimensão do vetor.
- C) A diferença absoluta entre o maior e o menor elemento do vetor.
- D) A multiplicação de todas as suas componentes pelo número de dimensões.

**Resposta Correta:** A
> **Justificativa:** A norma de um vetor é uma função que atribui um valor real não negativo ao vetor, quantificando seu comprimento, tamanho ou magnitude a partir da origem do espaço vetorial.

**Resposta Correta:** B
> **Justificativa:** A norma $L_2$ (norma Euclidiana) é dada pela raiz quadrada da soma dos quadrados dos componentes: $\|\mathbf{x}\|_2 = \sqrt{(-2)^2 + 1^2 + 3^2} = \sqrt{4 + 1 + 9} = \sqrt{14}$.

### Questão 7
Geometricamente, o que a norma $L_2$ de um vetor representa?
- A) A distância percorrida apenas ao longo de eixos ortogonais.
- B) A distância em linha reta do ponto até a origem.
- C) O ângulo formado entre o vetor e o eixo horizontal.
- D) A área do retângulo delimitado pelas componentes do vetor.

**Resposta Correta:** B
> **Justificativa:** Geometricamente, enquanto a norma $L_1$ mede o deslocamento ao longo de eixos ortogonais, a norma $L_2$ mede a distância em linha reta do ponto até a origem do espaço vetorial.

### Questão 8
O que acontece com a magnitude e a direção de um vetor ao ser multiplicado por um escalar negativo $s < 0$?
- A) A magnitude é sempre reduzida e a direção é mantida.
- B) A magnitude muda e o sentido é invertido.
- C) O vetor torna-se perpendicular ao vetor original.
- D) A magnitude permanece idêntica e o sentido é mantido.

**Resposta Correta:** B
> **Justificativa:** Um escalar negativo ($s < 0$), além de alterar a magnitude do vetor, inverte o seu sentido no espaço vetorial.

### Questão 9
Qual é a restrição para que seja possível realizar a adição ou subtração entre dois vetores?
- A) Pelo menos um dos vetores deve ser um vetor nulo.
- B) Ambos os vetores precisam ter a mesma dimensão.
- C) O produto escalar entre os dois vetores deve ser diferente de zero.
- D) Ambas as normas $L_2$ devem ser iguais a $1$.

**Resposta Correta:** B
> **Justificativa:** Não é possível adicionar ou subtrair vetores de dimensões diferentes; eles precisam pertencer ao mesmo espaço $\mathbb{R}^n$.

### Questão 10
Qual é a natureza do resultado obtido ao calcular o produto escalar entre dois vetores de mesma dimensão?
- A) Um novo vetor de dimensão igual ao dobro da original.
- B) Uma matriz quadrada $n \times n$.
- C) Um único valor escalar.
- D) Um vetor coluna ortogonal aos dois originais.

**Resposta Correta:** C
> **Justificativa:** O produto escalar (ou produto interno) combina dois vetores elemento por elemento e os soma, resultando em um único valor escalar.

### Questão 11
Se dois vetores possuem comprimento unitário (normas $L_2$ iguais a $1$), o cosseno do ângulo entre eles é igual a quê?
- A) À soma de suas normas $L_1$.
- B) Ao seu produto escalar.
- C) À sua distância Euclidiana.
- D) A zero.

**Resposta Correta:** B
> **Justificativa:** Como a norma de cada vetor é $1$, o denominador na fórmula do cosseno fica $\|\mathbf{a}\|_2 \|\mathbf{b}\|_2 = 1 \cdot 1 = 1$, tornando $\cos \theta = \mathbf{a} \cdot \mathbf{b}$.

### Questão 12
Qual é a condição necessária e suficiente para que dois vetores $\mathbf{a}$ e $\mathbf{b}$ sejam ortogonais ($\mathbf{a} \perp \mathbf{b}$)?
- A) A distância Euclidiana entre eles deve ser igual a $1$.
- B) Suas normas $L_1$ devem ser exatamente iguais.
- C) O produto escalar entre eles deve ser igual a zero.
- D) A similaridade de cosseno deve ser igual a $1$.

**Resposta Correta:** C
> **Justificativa:** Dois vetores são ditos ortogonais se e somente se o produto escalar entre eles for igual a zero ($\mathbf{a} \cdot \mathbf{b} = 0$), formando um ângulo de $90^\circ$.

### Questão 13
Quando dois vetores são ortogonais e ambos possuem comprimento unitário, como são chamados?
- A) Lineares
- B) Escalares
- C) Ortonormais
- D) Colineares

**Resposta Correta:** C
> **Justificativa:** Por definição, quando dois vetores são ortogonais ($\mathbf{a} \cdot \mathbf{b} = 0$) e ambos têm norma unitária ($\|\mathbf{a}\|_2 = 1$ e $\|\mathbf{b}\|_2 = 1$), eles são denominados ortonormais.

### Questão 14
Qual técnica de Aprendizado de Máquina utilizada para redução de dimensionalidade fundamenta-se no conceito de ortogonalidade?
- A) Análise de Componentes Principais (PCA)
- B) Algoritmos Genéticos
- C) Regressão Linear Simples
- D) k-Nearest Neighbors

**Resposta Correta:** A
> **Justificativa:** A ortogonalidade é fundamental para a Análise de Componentes Principais (PCA), que busca eixos ortogonais para eliminar a redundância de informações entre as variáveis.

### Questão 15
Em qual intervalo varia o valor da Similaridade de Cosseno entre dois vetores?
- A) $[0; \infty)$
- B) $[-1; 1]$
- C) $[0; 1]$
- D) $(-\infty; \infty)$

**Resposta Correta:** B
> **Justificativa:** Como a similaridade de cosseno corresponde ao valor trigonométrico do cosseno do ângulo entre os vetores, seus valores variam estritamente no intervalo de $[-1; 1]$.

### Questão 16
O que indica um valor de Similaridade de Cosseno igual a $1$ entre dois vetores?
- A) Que os vetores são ortogonais entre si.
- B) Que os vetores apontam em direções opostas.
- C) Que os vetores apontam na mesma direção e sentido.
- D) Que um dos vetores é obrigatoriamente o vetor nulo.

**Resposta Correta:** C
> **Justificativa:** A similaridade é máxima ($\cos \theta = 1$) quando o ângulo entre os vetores é $0^\circ$, significando que apontam exatamente na mesma direção e sentido.

### Questão 17
Se a similaridade de cosseno entre dois vetores $\mathbf{b}$ e $\mathbf{c}$ for aproximadamente $0{,}081$, qual é a relação geométrica aproximada entre eles?
- A) Apontam para direções idênticas.
- B) São quase ortogonais entre si.
- C) São vetores paralelos com sentidos opostos.
- D) Possuem normas exatamente iguais a zero.

**Resposta Correta:** B
> **Justificativa:** Um valor de similaridade próximo de $0$ (como $-0{,}081$) indica que o ângulo entre eles está próximo de $90^\circ$, o que significa que são quase ortogonais (independentes).

### Questão 18
Dados os vetores $\mathbf{a} = \begin{pmatrix} -3 & 2 \end{pmatrix}$, $\mathbf{b} = \begin{pmatrix} -1 & 0 \end{pmatrix}$ e $\mathbf{c} = \begin{pmatrix} 1 & 1 & -1 \end{pmatrix}$, é correto afirmar que
- A) $\mathbf{a}, \mathbf{b}, \mathbf{c} \in \mathbb{R}^2$.
- B) $\mathbf{a} \in \mathbb{R}$, $\mathbf{b} \in \mathbb{R}^2$ e $\mathbf{c} \in \mathbb{R}^3$.
- C) $\mathbf{a}, \mathbf{b} \in \mathbb{R}^2$ e $\mathbf{c} \in \mathbb{R}^3$.
- D) $\mathbf{a}, \mathbf{b} \in \mathbb{R}^3$ e $\mathbf{c} \in \mathbb{R}^2$.

**Resposta Correta:** C
> **Justificativa:** Como os vetores $\mathbf{a}$ e $\mathbf{b}$ possuem duas dimensões, ambos pertencem ao conjunto $\mathbb{R}^2$. Como o vetore $\mathbf{c}$ possui três dimensões, ele pertence ao conjunto $\mathbb{R}^3$.

**Questão 19**: Dados os vetores $\mathbf{a} = \begin{pmatrix} 10 & -5 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 0 & 2 \end{pmatrix}$, qual é o valor do produto escalar $\mathbf{a} \cdot \mathbf{b}$?
- A) $58$
- B) $42$
- C) $-58$
- D) $-10$

**Resposta Correta:** D
> **Justificativa:** O produto escalar é a soma dos produtos dos componentes correspondentes: $\mathbf{a} \cdot \mathbf{b} = 10 \cdot 0 + (-5) \cdot 2 = 0 - 10 = -10$.

**Questão 20**: Dados os vetores $\mathbf{a} = \begin{pmatrix} 0 & 10 & -3 & 1 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} -6 & 1 & 3 & -2 \end{pmatrix}$, qual é o vetor resultante da adição $\mathbf{a} + \mathbf{b}$?
- A) $\begin{pmatrix} -6 & 11 & -6 & 1 \end{pmatrix}$
- B) $\begin{pmatrix} -6 & 11 & 0 & -1 \end{pmatrix}$
- C) $\begin{pmatrix} 0 & 9 & 0 & 1 \end{pmatrix}$
- D) $\begin{pmatrix} -6 & 11 & 0 & 3 \end{pmatrix}$

**Resposta Correta:** B
> **Justificativa:** A adição de vetores é feita somando componente a componente: $\mathbf{a} + \mathbf{b} = \begin{pmatrix} 0+(-6) & 10+1 & -3+3 & 1+(-2) \end{pmatrix} = \begin{pmatrix} -6 & 11 & 0 & -1 \end{pmatrix}$.