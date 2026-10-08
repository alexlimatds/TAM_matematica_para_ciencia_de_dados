# Unidade 1: Álgebra Linear, Vetores e Aprendizado de Máquina

## Introdução

A álgebra linear é a linguagem fundamental por trás dos algoritmos modernos de inteligência artificial. Neste capítulo, você compreenderá a relação direta entre a álgebra linear e o aprendizado de máquina, aprendendo a diferenciar escalares de vetores e a dominar suas representações. Além de explorar a interpretação geométrica dos vetores, você aprenderá a executar e aplicar suas principais operações no contexto prático da ciência de dados. Prepare-se para sua jornada na construção de uma base matemática fundamental para a compreensão sólida dos modelos que revolucionaram a inteligência artificial.

## Álgebra Linear e Aprendizado de Máquina

A **álgebra linear** é o ramo da matemática que estuda vetores, matrizes, espaços vetoriais e transformações 
lineares. Historicamente, surgiu da necessidade de resolver sistemas de equações lineares, mas hoje é uma das 
áreas mais fundamentais para praticamente todas as disciplinas científicas e de engenharia.

Podemos pensar na álgebra linear como a "matemática dos dados". Sempre que organizamos informações em tabelas, 
listas ou grades de números, estamos, na verdade, trabalhando com estruturas da álgebra linear. Por exemplo:

- Uma planilha com as notas de vários alunos em diferentes disciplinas é uma matriz.
- O registro de consumo de energia elétrica ao longo das horas do dia é um vetor.
- O conjunto de pesos de uma rede neural é composto por vetores e matrizes.

Um conceito central nessa área é o de **combinação linear**: a ideia de que podemos criar novos objetos a partir de 
outros, multiplicando-os por escalares e somando-os. Essa noção simples é a base de quase todos os algoritmos de 
Aprendizado de Máquina.

O **Aprendizado de Máquina** (Machine Learning, ML) constrói modelos matemáticos a partir de dados para realizar 
previsões. Esses dados são, quase sempre, representados como vetores e matrizes. Vejamos algumas conexões 
diretas:

|Conceito de ML |Estrutura de álgebra linear|
|---------------|---------------------------|
|Um exemplo (amostra) |Vetor|
|Um conjunto de dados |Matriz|
|Distância entre amostras |Norma euclidiana|
|Regularização |Normas L1 e L2|
|Redução de dimensionalidade (PCA) |Autovalores e autovetores|
|Regressão linear |Solução de sistemas lineares|

Dominar a notação e as operações de álgebra linear é essencial para quem estuda ou trabalha com aprendizado de máquina e ciência de dados. Essa competência permite ler e entender descrições de algoritmos em livros, artigos e na web. Também permite descrever de forma concisa e precisa seus próprios métodos para outros profissionais.  

Outro ponto importante é a relação entre álgebra linear e estatística, especialmente estatística multivariada. A estatística usa intensamente a notação e as ferramentas da álgebra linear para descrever métodos. Temos como exemplo vetores de médias e de variâncias e matrizes de covariância para variáveis gaussianas múltiplas.

## Vetores e Escalares

Em álgebra linear, os conceitos de escalar e vetor são as unidades fundamentais. Um **escalar** é um único número 
real (ou complexo), como 3, -0,5, $\pi$, que representa magnitude sem direção. Exemplos de escalares comuns em aprendizado de máquina são: a taxa de aprendizado, o número 
de épocas de treinamento e a acurácia de um modelo.

Um **vetor** é um arranjo ordenado de escalares. O número de elementos, ou componentes, é chamado de dimensão ou dimensionalidade 
do vetor. Por exemplo, um indivíduo de 25 anos, com salário de R\$30,50 por hora e 5 anos de experiência pode ser 
representado pelo vetor de características $\mathbf{x} \in \mathbb{R}^{3}$:

$$\mathbf{x} = \begin{pmatrix} 25 & 30{,}5 & 5 \end{pmatrix}$$

Para denotar um vetor $\mathbf{v}$ com $n$ componentes de forma genérica, escrevemos:

$$
\mathbf{v} = \begin{pmatrix}
v_1 & v_2 & \cdots & v_n 
\end{pmatrix}
$$

Quando os elementos do vetor estão dipostos na horizontal, chamamos o vetor de vetor linha. Também podemos dispor os elementos de um vetor na vertical e, neste caso, o chamamos de vetor coluna:

$$
\mathbf{v} = \begin{pmatrix}
v_1 \\
v_2 \\
\vdots  \\
v_n
\end{pmatrix}
$$

Repare que, neste texto, vetores são denotados por meio de letras minúsculas grafadas em negrito e escalares são denotados por meio de letras minúsculas grafadas em itálico.

Em aprendizado de máquina, um vetor representa tipicamente uma amostra (um paciente com $n$ exames, uma casa com $n$ características) ou um conjunto de parâmetros (os pesos de um modelo).

O **vetor nulo**, denotado por $\mathbf{0}$, é o vetor em que todos os seus componentes são iguais a zero:

$$
\mathbf{0} = \begin{pmatrix}
0 & 0 & \cdots & 0
\end{pmatrix}
$$

## Vetores e sistemas de coordenadas

Um vetor bidimensional pode ser visto como um ponto no plano cartesiano (espaço $\mathbb{R}^{2}$) ou como uma seta que começa na origem do plano e termina no ponto indicado pelas coordenadas do vetor. Por exemplo, a Figura 1 ilustra os vetores $\mathbf{v} = \begin{pmatrix} 2 & 7 \end{pmatrix}$ e $\mathbf{w} = \begin{pmatrix} -6 & -1 \end{pmatrix}$ no plano cartesiano.

TODO: figura

De forma análoga, vetores com três dimensões podem ser traçados no espaço cartesiano, o $\mathbb{R}^{3}$, como ilustrado na Figura 2.

TODO: figura

DICA: É importante perceber que vetores podem ter uma, duas, três ou mais dimensões. Pode parecer estranho pensar em um vetor com 10 dimensões, mas do ponto de vista matemático isso é totalmente possível. Vetores com quatro ou mais dimensões são de difícil visualização, mas são comuns no contexto de aprendizado de máquina e ciência de dados.

## Norma de um vetor

A **norma** de um vetor é uma função que atribui um valor real não negativo ao 
vetor, quantificando seu comprimento, tamanho ou magnitude a partir da 
origem do espaço vetorial. Em ML, normas são comumente usadas na 
regularização de modelos e para normalizar vetores.

A **norma $L_1$**, também chamada de norma Manhattan, é a soma dos valores 
absolutos dos componentes de um vetor:

$$
\left\| \mathbf{x} \right\|_1 = \sum_{i=1}^{n}|x_i|=|x_1|+|x_2|+\cdots +|x_n|
$$

**Exemplo:** para $\mathbf{x} = \begin{pmatrix} -3 & 5 \end{pmatrix}$:

$\left\| \mathbf{x} \right\|_1 = |-3| + |5| = 3 + 5 = 8$

Geometricamente, a norma $L_1$ mede a distância percorrida ao longo de cada eixo do espaço cartesiano.

A **norma $L_2$**, ou norma Euclidiana, é a raiz quadrada da soma dos quadrados 
dos componentes do vetor:

$$
\left\| \mathbf{x} \right\|_2 = \sqrt{\sum_{i=1}^{n}x_i}=\sqrt{x_1^2 + x_2^2+ \cdots +x_n^2}
$$

**Exemplo:** para $\mathbf{x} = \begin{pmatrix} -3 & 5 \end{pmatrix}$:

$\left\| \mathbf{x} \right\|_2 = \sqrt{(-3)^2 + 5^2} = \sqrt{9 + 25} \approx 5{,}83 $

Geometricamente, a norma $L_2$ mede a distância em linha reta do ponto até a origem do espaço vetorial.

TODO: figura

EXERCÍCIOS DE FIXAÇÃO

**Questão 1**: Dado o vetor $\mathbf{x} = \begin{pmatrix} 10 & -3 & 4 & 0 \end{pmatrix}$, qual é a sua norma $L_1$?
- A) $2$
- B) $17$
- C) $\sqrt{11}$
- D) $11$

**Resposta Correta:** B
> **Justificativa:** A norma $L_1$ (norma Manhattan) é a soma dos valores absolutos de seus componentes: $\|\mathbf{x}\|_1 = |10| + |-3| + |4| + |0| = 10 + 3 + 4 + 0 = 17$.


**Questão 2**: Dado o vetor $\mathbf{x} = \begin{pmatrix} -2 & 1 & 3 \end{pmatrix}$, qual é o valor da sua norma $L_2$?
- A) $6$
- B) $\sqrt{14}$
- C) $14$
- D) $2$

**Resposta Correta:** B
> **Justificativa:** A norma $L_2$ (norma Euclidiana) é dada pela raiz quadrada da soma dos quadrados dos componentes: $\|\mathbf{x}\|_2 = \sqrt{(-2)^2 + 1^2 + 3^2} = \sqrt{4 + 1 + 9} = \sqrt{14}$.

## Operações com Vetores

As operações com vetores formam a base matemática para manipular conjuntos de dados, calcular previsões e atualizar parâmetros em modelos de aprendizado de máquina.

### Multiplicação de um Vetor por um Escalar
A multiplicação de um vetor $\mathbf{v} \in \mathbb{R}^n$ por um escalar $s \in \mathbb{R}$ consiste em multiplicar cada uma das componentes do vetor pelo valor do escalar, resultando em um novo vetor de mesma dimensão:

$$s \cdot \mathbf{v} = \begin{pmatrix} s \cdot v_1 & s \cdot v_2 & \dots & s \cdot v_n \end{pmatrix}$$


**Exemplo:** Considere os escalares $a = 3$, $b = -0{,}5$ e o vetor $\mathbf{v} = \begin{pmatrix} 2 & -4 \end{pmatrix}$.

$a \cdot \mathbf{v} = 3 \cdot \begin{pmatrix} 2 & -4 \end{pmatrix} = \begin{pmatrix} 3 \cdot 2 & 3 \cdot (-4) \end{pmatrix} = \begin{pmatrix} 6 & -12 \end{pmatrix}$

$b \cdot \mathbf{v} = (-0{,}5) \cdot \begin{pmatrix} 2 & -4 \end{pmatrix} = \begin{pmatrix} (-0{,}5) \cdot 2 & (-0{,}5) \cdot (-4) \end{pmatrix} = \begin{pmatrix} -1 & 2 \end{pmatrix}$

Um escalar positivo ($s > 0$) modifica a magnitude (comprimento) do vetor, amplificando-o (quando $s > 1$) ou encolhendo-o (quando $0 < s < 1$), enquanto mantém a sua direção e sentido inalterados. Um escalar negativo ($s < 0$), além de alterar a magnitude, inverte o sentido do vetor no espaço vetorial.

TODO: figura

### Divisão de um Vetor por um Escalar

A divisão de um vetor $\mathbf{v}$ por um escalar não nulo $s \neq 0$ é realizada dividindo cada componente de $\mathbf{v}$ por $s$, o que equivale matematicamente a multiplicar $\mathbf{v}$ pelo inverso do escalar ($1/s$):

$\frac{\mathbf{v}}{s} = \begin{pmatrix}\frac{v_1}{s} & \frac{v_2}{s} & \dots & \frac{v_n}{s} \end{pmatrix}$

**Exemplo:**
Sejam $\mathbf{v} = \begin{pmatrix} 6 & 8 \end{pmatrix}$ e $s = 2$:

$\frac{v}{2} = \begin{pmatrix}\frac{6}{2}, \frac{8}{2} \end{pmatrix} = \begin{pmatrix} 3 & 4 \end{pmatrix}$

### Adição de Vetores
A adição de dois vetores $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$ de mesma dimensão é realizada somando elemento a elemento:

$\mathbf{a} + \mathbf{b} = \begin{pmatrix} a_1 + b_1 & a_2 + b_2 & \dots & a_n + b_n \end{pmatrix}$

**Exemplo:**
Sejam $\mathbf{a} = \begin{pmatrix} 1 & 3 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 4 & -2 \end{pmatrix}$:

$\mathbf{a} + \mathbf{b} = \begin{pmatrix} 1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \end{pmatrix} = \begin{pmatrix} 1 + 4 & 3 + (-2) \end{pmatrix} = \begin{pmatrix} 5 & 1 \end{pmatrix}$

### Subtração de Vetores
A subtração entre dois vetores $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$ de mesma dimensão é calculada subtraindo elemento por elemento:

$\mathbf{a} - \mathbf{b} = \begin{pmatrix} a_1 - b_1 & a_2 - b_2 & \dots & a_n - b_n \end{pmatrix}$

**Exemplo:**
Sejam $\mathbf{a} = \begin{pmatrix} 1 & 3 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 4 & -2 \end{pmatrix}$:

$\mathbf{a} - \mathbf{b} = \begin{pmatrix} 1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \end{pmatrix} = \begin{pmatrix} 1 - 4 & 3 - (-2) \end{pmatrix} = \begin{pmatrix} -3 & 5 \end{pmatrix}$

TODO: figura

DICA: Repare que não é possível adicionar ou subtrair vetores com dimensões diferentes.

EXERCÍCIO DE FIXAÇÃO

**Questão 3**: Ao multiplicar o vetor $\mathbf{v} = \begin{pmatrix} 0 & 2 & -5 \end{pmatrix}$ pelo escalar $a = -4$, qual vetor é obtido?
- A) $\begin{pmatrix} -4 & -8 & 20\end{pmatrix}$
- B) $\begin{pmatrix} 0 & -8 & -20 \end{pmatrix}$
- C) $\begin{pmatrix} 0 & 8 & 20 \end{pmatrix}$
- D) $\begin{pmatrix} 0 & -8 & 20 \end{pmatrix}$

**Resposta Correta:** D
> **Justificativa:** A multiplicação por um escalar consiste em multiplicar cada componente do vetor pelo escalar: $(-4) \cdot \begin{pmatrix} 0 & 2 & -5 \end{pmatrix} = \begin{pmatrix} (-4) \cdot 0 & (-4) \cdot 2 & (-4) \cdot (-5) \end{pmatrix} = \begin{pmatrix} 0 & -8 & 20 \end{pmatrix}$.

**Questão 4**: Sejam $\mathbf{v} = \begin{pmatrix} 1 & 0 & -3 \end{pmatrix}$ e $s = 3$. Qual é o resultado da divisão $\frac{\mathbf{v}}{s}$?
- A) $\begin{pmatrix} \frac{1}{3} & 0 & -1 \end{pmatrix}$
- B) $\begin{pmatrix} 1,3 & -3 & 1 \end{pmatrix}$
- C) $\begin{pmatrix} 0,3 & 0 & 1 \end{pmatrix}$
- D) $\begin{pmatrix} \frac{1}{3} & 0 & 1 \end{pmatrix}$

**Resposta Correta:** A
> **Justificativa:** A divisão de um vetor por um escalar $s \neq 0$ divide cada componente por $s$: $\frac{\mathbf{v}}{3} = \begin{pmatrix} \frac{1}{3} & \frac{0}{3} & \frac{-3}{3} \end{pmatrix} = \begin{pmatrix} \frac{1}{3} & 0 & -1 \end{pmatrix}$.

**Questão 5**: Dados os vetores $\mathbf{a} = \begin{pmatrix} -2 & 5 & -3 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 0 & 3 & -1 \end{pmatrix}$, qual é o resultado da adição $\mathbf{a} + \mathbf{b}$?
- A) $\begin{pmatrix} 0 & 15 & -3 \end{pmatrix}$
- B) $\begin{pmatrix} 0 & 8 & - 4 \end{pmatrix}$
- C) $\begin{pmatrix} -2 & 8 & 4 \end{pmatrix}$
- D) $\begin{pmatrix} -2 & 8 & -2 \end{pmatrix}$

**Resposta Correta:** C
> **Justificativa:** A adição de vetores é feita somando componente a componente: $\mathbf{a} + \mathbf{b} = \begin{pmatrix} -2+0 & 5+3 & -3+(-1) \end{pmatrix} = \begin{pmatrix} -2 & 8 & -4 \end{pmatrix}$.

**Questão 6**: Dados os vetores $\mathbf{a} = \begin{pmatrix} -5 & 1 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 3 & 8 \end{pmatrix}$, qual é o resultado da subtração $\mathbf{a} - \mathbf{b}$?
- A) $\begin{pmatrix} -8 & -7 \end{pmatrix}$
- B) $\begin{pmatrix} 8 & 7 \end{pmatrix}$
- C) $\begin{pmatrix} 2 & 7 \end{pmatrix}$
- D) $\begin{pmatrix} 2 & 9 \end{pmatrix}$

**Resposta Correta:** A
> **Justificativa:** A subtração entre vetores é dada subtraindo componente a componente: $\mathbf{a} - \mathbf{b} = \begin{pmatrix} -5 - 3 & 1 - 8 \end{pmatrix} = \begin{pmatrix} -8 & -7 \end{pmatrix}$.

## Distância Euclidiana entre Vetores

A **distância euclidiana** entre dois vetores $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$ mede o comprimento do segmento de reta que conecta os dois pontos no espaço de coordenadas. Ela é definida como a norma $L_2$ do vetor diferença  $\mathbf{a} - \mathbf{b}$:

$d(\mathbf{a}, \mathbf{b}) = \left\| \mathbf{a} - \mathbf{b} \right\|_2 = \sqrt{\sum_{i=1}^{n}(a_i - b_i)}=\sqrt{(a_1 - b_1)^2 + (a_2 - b_2)^2+ \cdots +(a_n - b_n)^2}$

**Exemplo:**
Considere os vetores $\mathbf{a} = \begin{pmatrix} 1 & 2 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 4 & 6 \end{pmatrix}$:

$$
d(\mathbf{a}, \mathbf{b}) = \sqrt{(1 - 4)^2 + (2 - 6)^2} = \sqrt{(-3)^2 + (-4)^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

CURIOSIDADE: A distância euclidiana é comumente utilizada por algoritmos de aprendizado de máquina baseados em vizinhança, como o *k-Nearest Neighbors* (k-NN) e o *k-Means*.

EXERCÍCIO DE FIXAÇÃO

**Questão 7**: Para os vetores $\mathbf{x} = \begin{pmatrix} 3 & -2 & -1 \end{pmatrix}$ e $\mathbf{y} = \begin{pmatrix} 2 & -2 & 4 \end{pmatrix}$, qual é a distância Euclidiana $d(\mathbf{x}, \mathbf{y})$?
- A) $29$
- B) $\sqrt{29}$
- C) $25$
- D) $\sqrt{26}$

**Resposta Correta:** D
> **Justificativa:** A distância Euclidiana é $d(\mathbf{x}, \mathbf{y}) = \sqrt{(3 - 2)^2 + (-2 - (-2))^2 + (-1 - 4)^2} = \sqrt{(1)^2 + (0)^2 + (-5)^2} = \sqrt{1 + 25} = \sqrt{26}$.

## Produto Escalar

O **produto escalar**, ou produto interno, entre dois vetores de mesma dimensão $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$ de mesma dimensão é determinado pela soma dos produtos de suas componentes correspondentes, resultando em um único valor escalar:

$$
\mathbf{a} \cdot \mathbf{b} = \sum_{i=1}^n a_i b_i = a_1 b_1 + a_2 b_2 + \dots + a_n b_n
$$

**Exemplo:**
Sejam $\mathbf{a} = \begin{pmatrix} 1 & 3 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 4 & -2 \end{pmatrix}$:

$\mathbf{a} \cdot \mathbf{b} = \begin{pmatrix} 1 & 3 \end{pmatrix} \cdot \begin{pmatrix} 4 & -2 \end{pmatrix} = 1 \cdot 4 + 3 \cdot (-2) =  4 + (-6) = -2$

EXERCÍCIO DE FIXAÇÃO

**Questão 8**: Dados os vetores $\mathbf{a} = \begin{pmatrix} 9 & 10 & -2 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 0 & 5 & 4 \end{pmatrix}$, qual é o valor do produto escalar $\mathbf{a} \cdot \mathbf{b}$?
- A) $58$
- B) $42$
- C) $-58$
- D) $-10$

**Resposta Correta:** B
> **Justificativa:** O produto escalar é a soma dos produtos dos componentes correspondentes: $\mathbf{a} \cdot \mathbf{b} = 9 \cdot 0 + 10 \cdot 5 + (-2)\cdot 4 = 0 + 50 - 8 = 42$.

## Ângulo entre Dois Vetores
Observe o ângulo a figura abaixo e note que dois vetores quaisquer formam um ângulo com vértice na origem do plano.

TODO: figura

Sejam os vetores não-nulos $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$, o cosseno do ângulo $\theta$ formado por $\mathbf{a}$ e $\mathbf{b}$ pode ser calculado pela fórmula:

$$
\cos \theta = \frac{\mathbf{a} \cdot \mathbf{b}}{\left\| \mathbf{a} \right\|_2 \left\| \mathbf{b} \right\|_2}
$$

Uma vez calculado o $\cos \theta$, o ângulo $\theta$ é econtrado por meio de uma tabela de co-senos.

**Exemplo:**
Sejam $\mathbf{a} = \begin{pmatrix} -2 & -2 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 0 & -2 \end{pmatrix}$:

$\mathbf{a} \cdot \mathbf{b} = (-2) \cdot 0 + (-2) \cdot (-2) = 0 + 4 = 4$

$\left\| \mathbf{a} \right\|_2 = \sqrt{(-2)^2 + (-2)^2} = \sqrt{4 + 4} = \sqrt{8} = 2\sqrt{2}$

$\left\| \mathbf{b} \right\|_2 = \sqrt{0^2 + (-2)^2} = \sqrt{0 + 4} = \sqrt{4} = 2$

$\cos \theta = \frac{\mathbf{a} \cdot \mathbf{b}}{\left\| \mathbf{a} \right\|_2 \left\| \mathbf{b} \right\|_2} = \frac{4}{2\sqrt{2} \cdot 2} = \frac{4}{4\sqrt{2}} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$

$\theta = \text{arc cos} \frac{\sqrt{2}}{2} = 45^\circ$

DICA: Repare que caso os vetores possuam comprimento unitário ($\left\| \mathbf{a} \right\|_2 = 1$ e $\left\| \mathbf{b} \right\|_2 = 1$), o cosseno do ângulo entre eles é igual ao seu produto escalar.

EXERCÍCIO DE FIXAÇÃO:

**Questão 9**: Dados os vetores $\mathbf{a} = \begin{pmatrix} 1 & 4 \end{pmatrix}$ e $\mathbf{b} = \begin{pmatrix} 3 & 12 \end{pmatrix}$, qual é o ângulo $\theta$ entre eles?
- A) $0^\circ$
- B) $30^\circ$
- C) $45^\circ$
- D) $90^\circ$

**Resposta Correta:** A
> **Justificativa:** O cosseno é dado por $\cos \theta = \frac{\mathbf{a} \cdot \mathbf{b}}{\Vert{}\mathbf{a}\Vert{}_2 \Vert{}\mathbf{b}\Vert{}_2} =  \frac{1 \cdot 3 + 4 \cdot 12}{\sqrt{1^2 + 4^2} \cdot \sqrt{3^2 + 12^2}} = \frac{3 + 48}{\sqrt{17} \cdot \sqrt{153}} =\frac{51}{\sqrt{2601}} =\frac{51}{51} = 1$. Consultando uma tabela trigonométrica, verificamos que $\cos 0^\circ = 0$ e, portanto, $\theta = 0^\circ$.

## Ortogonalidade entre Vetores

Dois vetores $\mathbf{a}, \mathbf{b} \in \mathbb{R}^n$ são ditos **ortogonais** $(\mathbf{a} \perp \mathbf{b})$ se e somente se o produto escalar entre eles for igual a zero. Isto significa que $\mathbf{a}$ e $\mathbf{b}$ formam um ângulo de $90^\circ$.

Quando $\mathbf{a}$ e $\mathbf{b}$ são ortogonais e ambos possuem comprimento unitário ($\left\| \mathbf{a} \right\|_2 = 1$ e $\left\| \mathbf{b} \right\|_2 = 1$), eles são denominados **ortonormais**.

CURIOSIDADE: A ortogonalidade é fundamental para a análise de componentes principais (PCA), um algoritmo que tem como objetivo eliminar a redundância presente entre os componentes de um vetor.


## Similaridade de Cosseno

A **similaridade de cosseno** é uma métrica que usa o cosseno do ângulo entre dois vetores para avaliar o quão próximos dois vetores são semelhantes independentemente dos seus comprimentos. Por exemplo, na figura abaixo podemos dizer que, com base na similaridade do cosseno, o vetor $\mathbf{a}$ é mais similar ao vetor $\mathbf{b}$ do que ao vetor $\mathbf{c}$, visto que o ângulo $\alpha$ entre $\mathbf{a}$ e $\mathbf{b}$ é menor do que o ângulo $\beta$ entre $\mathbf{a}$ e $\mathbf{c}$.

TODO: figura

Por ser baseada no valor do cosseno, a similaridade de cosseno varia no intervalo $[-1; 1]$. Neste contexto, a similaridade é máxima quando o ângulo $\theta$ entre os vetores é igual a zero, o que resulta em $\cos \theta = 1$, significando que os vetores apontam na mesma direção. Por outro lado, vetores em direções opostas possuem $\cos \theta = -1$, como ilustrado no figura abaixo.

TODO: figura

CURIOSIDADE: A similaridade de cosseno é amplamente empregada em processamento de linguagem natural e em sistemas de recomendação. Quando textos ou itens são convertidos em vetores de atributos, o tamanho do documento altera a magnitude dos vetores, mas não o tópico de cada vetor. A similaridade de cosseno compara o conteúdo do texto independentemente da sua extensão.

**Exemplo:**
Sejam $\mathbf{a} = \begin{pmatrix} 1 & 3 \end{pmatrix}$, $\mathbf{b} = \begin{pmatrix} 2 & -2 \end{pmatrix}$ e $\mathbf{c} = \begin{pmatrix} 8 & 10 \end{pmatrix}$, vamos analisar as similaridades entre estes vetores.

Calculando a norma $L_2$ de cada vetor:

$$\Vert{}\mathbf{a}\Vert{}_2 = \sqrt{1^2 + 3^2} = \sqrt{1 + 9} = \sqrt{10}$$

$$\Vert{}\mathbf{b}\Vert{}_2 = \sqrt{2^2 + (-2)^2} = \sqrt{4 + 4} = \sqrt{8} $$

$$\Vert{}\mathbf{c}\Vert{}_2 = \sqrt{8^2 + 10^2} = \sqrt{64 + 100} = \sqrt{164}$$

Calculando os produtos escalares:

$$\mathbf{a} \cdot \mathbf{b} = 1 \cdot 2 + 3 \cdot(-2) = 2 - 6 = -4$$

$$\mathbf{a} \cdot \mathbf{c} = 1 \cdot 8 + 3 \cdot 10 = 8 + 30 = 38$$

$$\mathbf{b} \cdot \mathbf{c} = 2 \cdot 8 + (-2) \cdot 10 = 16 - 20 = -4$$

Calculando as similaridades de cosseno:

$$\text{Sim}(\mathbf{a}, \mathbf{b}) = \frac{\mathbf{a} \cdot \mathbf{b}}{\Vert{}\mathbf{a}\Vert{}_2 \Vert{}\mathbf{b}\Vert{}_2} = \frac{-4}{\sqrt{10} \sqrt{8}} = \frac{-4}{\sqrt{80}} = \frac{-4}{4\sqrt{5}} = -\frac{1}{\sqrt{5}} \approx -0{,}447$$

$$\text{Sim}(\mathbf{a}, \mathbf{c}) = \frac{\mathbf{a} \cdot \mathbf{c}}{\Vert{}\mathbf{a}\Vert{}_2 \Vert{}\mathbf{c}\Vert{}_2} = \frac{38}{\sqrt{10} \sqrt{164}} = \frac{38}{\sqrt{1640}} \approx 0{,}938$$

$$\text{Sim}(\mathbf{b}, \mathbf{c}) = \frac{\mathbf{b} \cdot \mathbf{c}}{\Vert{}\mathbf{b}\Vert{}_2 \Vert{}\mathbf{c}\Vert{}_2}  = \frac{-4}{\sqrt{8} \sqrt{164}} = \frac{-4}{\sqrt{1312}} \approx -0{,}110$$

Analisando os resultados:

* $\text{a}$ e $\text{b}$ possuem uma correlação negativa moderada ($\approx -0{,}447$), indicando direções quase opostas.
* $\text{a}$ e $\text{c}$ possuem alta similaridade de cosseno ($\approx 0{,}938$), indicando que apontam para direções bastante próximas.
* $\text{b}$ e $\text{c}$ apresentam uma similaridade próxima de zero ($\approx -0{,}110$), o que significa que são quase ortogonais (independentes) entre si.

## Conclusão

Nesta unidade, exploramos como a álgebra linear fornece os fundamentos matemáticos essenciais para o aprendizado de máquina e a ciência de dados. Compreendemos os conceitos de escalares e vetores, bem como suas interpretações geométricas nos espaços $\mathbb{R}^2$, $\mathbb{R}^3$ e em espaços de alta dimensão.

Analisamos o cálculo das normas $L_1$ e $L_2$, ferramentas cruciais na medição do tamanho de vetores e na aplicação de técnicas de regularização. Além disso, vimos como realizar as principais operações com vetores — como adição, subtração, multiplicação por escalar e produto escalar — e como elas se traduzem em operações diretas de manipulação de dados e parâmetros em modelos preditivos.

Por fim, estudamos métricas de distância e similaridade, tais como a distância euclidiana, o ângulo entre vetores, a ortogonalidade e a similaridade de cosseno. Entender essas relações geométricas é o que permite compreender como algoritmos baseados em vizinhança, reduções de dimensionalidade e modelos de processamento de linguagem natural lidam com representações vetoriais de dados no mundo real.

Com essa base conceitual consolidada, você está preparado para avançar no estudo de matrizes, transformações lineares e sistemas de equações, expandindo sua capacidade de compreender e implementar algoritmos de aprendizado de máquina.

## Referências

AGGARWAL, Charu C. **Linear Algebra and Optimization for Machine Learning**: A Textbook. Cham: Springer, 2020.

BROWNLEE, Jason. **Basics of Linear Algebra for Machine Learning**: Discover the Mathematical Language of Data in Python. [S. l.]: Machine Learning Mastery, 2018. E-book.

DEISENROTH, Marc Peter; FAISAL, A. Aldo; ONG, Cheng Soon. **Mathematics for Machine Learning**. Cambridge: Cambridge University Press, 2020. E-book. Disponível em: https://mml-book.github.io/. Acesso em: 2 out. 2026.

STRANG, Gilbert. Linear Algebra and Its Applications. 4th ed. Belmont: Brooks/Cole, 2006.