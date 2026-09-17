# Unidade 1: Álgebra Linear, Vetores e Aprendizado de Máquina

## Objetivos

- Apresentar a relação entre álgebra linear e aprendizado de máquina;
- Compreender o que são vetores e escalares;
- Compreender a interpretação geométrica de vetores;
- Conhecer a utilidade da biblioteca NumPy e aprender como criar utilizá-la para cirar vetores
- Aprender como calcular normas de vetores.

## Introdução

A Álgebra Linear é a linguagem matemática por trás da maioria dos algoritmos de aprendizado de máquina. 
Neste texto, você verá o que são vetores e escalares, como interpretá-los geometricamente, como criá-los 
com NumPy em Python, e como calcular normas, sempre conectando cada conceito a aplicações em ML.

## Álgebra Linear e Aprendizado de Máquina

A **Álgebra Linear** é o ramo da matemática que estuda vetores, matrizes, espaços vetoriais e transformações 
lineares. Historicamente, surgiu da necessidade de resolver sistemas de equações lineares, mas hoje é uma das 
áreas mais fundamentais para praticamente todas as disciplinas científicas e de engenharia.

Podemos pensar na Álgebra Linear como a "matemática dos dados". Sempre que organizamos informações em tabelas, 
listas ou grades de números, estamos, na verdade, trabalhando com estruturas da Álgebra Linear. Por exemplo:

- Uma planilha com as notas de vários alunos em diferentes disciplinas é uma matriz.
- O vetor de consumo de energia elétrica ao longo das horas do dia é um vetor.
- O conjunto de pesos de uma rede neural treinada é composto por vetores e matrizes.

Um conceito central nessa área é o de **combinação linear**: a ideia de que podemos criar novos objetos a partir de 
outros, multiplicando-os por escalares e somando-os. Essa noção simples é a base de quase todos os algoritmos de 
Aprendizado de Máquina.

O **Aprendizado de Máquina** (Machine Learning, ML) constrói modelos matemáticos a partir de dados para realizar 
previsões. Esses dados são, quase sempre, representados como vetores e matrizes. Vejamos algumas conexões 
diretas:

|Conceito de ML |Estrutura de Álgebra Linear|
|---------------|---------------------------|
|Um exemplo (amostra) |Vetor|
|Um conjunto de dados |Matriz|
|Distância entre amostras |Norma euclidiana|
|Regularização |Normas L1 e L2|
|Redução de dimensionalidade (PCA) |Autovalores e autovetores|
|Regressão linear |Solução de sistemas lineares|

Dominar a notação e as operações de álgebra linear é essencial para quem estuda ou trabalha com aprendizado de máquina e ciência de dados. Essa competência permite ler e entender descrições de algoritmos em livros, artigos e na web. Também permite descrever de forma concisa e precisa seus próprios métodos para outros profissionais.  

Outro ponto importante é a relação entre álgebra linear e estatística, especialmente estatística multivariada. A estatística usa intensamente a notação e as ferramentas da álgebra linear para descrever métodos: vetores de médias e variâncias, matrizes de covariância para variáveis gaussianas múltiplas etc.

## Vetores e Escalares

Em álgebra linear, os conceitos de escalar e vetor são as unidades fundamentais. Um **escalar** é um único número 
real (ou complexo), como 3, -0,5, $`\pi`$, e representa magnitude sem direção. Escalares são geralmente 
denotados por letras minúsculas. Em ML, exemplos de escalares são: a taxa de aprendizado ($`\alpha`$), o número 
de épocas, a acurácia de um modelo, etc.

Um **vetor** é um arranjo ordenado de escalares. O número de elementos, ou componentes, é chamado de dimensão ou dimensionalidade 
do vetor. Por exemplo, um indivíduo de 25 anos, com salário de R$30,50 por hora e 5 anos de experiência pode ser 
representado pelo vetor de características $`\textbf{x} \in \mathbb{R}^{3}`$:

$$\textbf{x} = \begin{pmatrix} 25 & 30,5 & 5 \end{pmatrix}$$

Para denotar um vetor $\textbf{v}$ com $n$ componentes de forma genérica, escrevemos:

$$
\textbf{v} = \begin{pmatrix}
v_1 & v_2 & \cdots & v_n 
\end{pmatrix}
$$

Quando os elementos do vetor estão dipostos na horizontal, chamamos o vetor de vetor linha. Também podemos dispor os elementos de um vetor na horizontal e, neste caso, o chamamos de vetor coluna:

$$
\textbf{v} = \begin{pmatrix}
v_1 \\
v_2 \\
\vdots  \\
v_n
\end{pmatrix}
$$

Repare que, neste texto, denotamos vetores por meio de letras minúsculas grafadas em negrito.

Em ML, um vetor representa tipicamente uma amostra (um paciente com $n$ exames, uma casa com $n$ características) ou um conjunto de parâmetros (os pesos de um modelo).

### Vetor nulo

O **vetor nulo**, denotado por $\textbf{0}$, é o vetor em que todos os componentes são iguais a zero:

$$
\textbf{0} = \begin{pmatrix}
0 & 0 & \cdots & 0
\end{pmatrix}
$$

## Vetores e sistemas de coordenadas

Um vetor bidimensional pode ser visto como um ponto no plano cartesiano (espaço $\mathbb{R}^{2}$) ou como uma seta que começa na origem do plano e termina no ponto indicado pelas coordenadas do vetor. Por exemplo, a Figura 1 ilustra os vetores $`\textbf{v} = \begin{pmatrix} 2 & 7 \end{pmatrix}`$ e $`\textbf{w} = \begin{pmatrix} -6 & -1 \end{pmatrix}`$ no plano cartesiano.

TODO: figura

De forma análoga, vetores com três dimensões podem ser traçados no espaço cartesiano, o $`\mathbb{R}^{3}`$, como ilustrado na Figura 2.

TODO: figura

É importante perceber que vetores podem ter uma, duas, três ou mais dimensões. Pode parecer estranho pensar em um vetor com 10 dimensões, mas do ponto de vista matemático isso é totalmente possível. Vetores com quatro ou mais dimensões são de difícil visualização, mas são comuns no contexto de aprendizado de máquina e ciência de dados.

## Norma de um vetor

A **norma** de um vetor é uma função que atribui um valor real não negativo ao 
vetor, quantificando seu comprimento, tamanho ou magnitude a partir da 
origem do espaço vetorial. Em ML, normas são comumente usadas na 
regularização de modelos e para normalizar vetores.

A **norma L1**, também chamada de norma Manhattan, é a soma dos valores 
absolutos dos componentes de um vetor:

$$
\left\| \textbf{x} \right\|_1 = \sum_{i=1}^{n}|x_i|=|x_1|+|x_2|+\cdots +|x_n|
$$

**Exemplo:** para $`\textbf{x} = \begin{pmatrix} -3 & 5 \end{pmatrix}`$:

$\left\| \textbf{x} \right\|_1 = |-3| + |5| = 3 + 5 = 8$

Geometricamente, a norma L2 mede a distância percorrida ao longo de eixos ortogonais.

TODO: figura

A **norma L2**, ou norma Euclidiana, é raiz quadrada da soma dos quadrados 
dos componentes do vetor:

$$
\left\| \textbf{x} \right\|_2 = \sqrt{\sum_{i=1}^{n}x_i}=\sqrt{x_1^2 + x_2^2+ \cdots +x_n^2}
$$

**Exemplo:** para $`\textbf{x} = \begin{pmatrix} -3 & 5 \end{pmatrix}`$:

$\left\| \textbf{x} \right\|_2 = \sqrt{(-3)^2 + 5^2} = \sqrt{9 + 25} \approx 5,83 $

Geometricamente, a norma L2 mede a distância em linha reta do ponto até a origem do espaço vetorial.

TODO: figura

## Python e NumPy

Na computação, a aplicação prática da álgebra linear é chamada de **Álgebra Linear Numérica**. Ela lida com a 
execução eficiente de operações matriciais e com a precisão de ponto flutuante em computadores.
Python é a linguagem mais utilizada em Aprendizado de Máquina, e o **NumPy** (Numerical Python) é sua biblioteca 
fundamental para computação científica. O NumPy fornece o **ndarray**, uma estrutura eficiente para armazenar e 
manipular vetores e matrizes.

Por que não usar listas comuns do Python? Por três motivos principais:
- Eficiência: As operações são vetorizadas em C, sendo muito mais rápidas.
- Conveniência: Operações matemáticas são expressas de forma compacta.
- Compatibilidade: É a base de bibliotecas como SciPy, scikit-learn, TensorFlow e PyTorch.

### Introdução ao `ndarray` do NumPy

Em Aprendizado de Máquina, os arrays da biblioteca NumPy (denominados 
`ndarray` ou *N-dimensional array*) constituem a estrutura de dados primária 
para representação numérica e execução de operações de álgebra linear. 
O `ndarray` é um array de tamanho fixo alocado em memória que armazena 
elementos do mesmo tipo de dado, como números inteiros ou de ponto flutuante.

A forma mais direta de criar um array unidimensional é converter uma lista 
nativa do Python utilizando a função `array()`.

```python
import numpy as np # importando NumPy

minha_lista = [1.5, 2.8, 3]     # criando uma lista Python
vetor1 = np.array(minha_lista)  # criando um ndarray

# de forma mais direta
vetor2 = np.array([-3, 0, 9, 0.006])
```

Para inspecionar um array, o NumPy disponibiliza dois atributos fundamentais:
* `dtype`: indica o tipo de dado dos elementos contidos no array.
* `shape`: retorna uma tupla que descreve a extensão de cada dimensão.

No caso de um array unidimensional composto por 3 elementos de ponto 
flutuante, a tupla retornada por `a.shape` é **`(3,)`** e o tipo indicado em `a.dtype` é **`float64`**.

```python
v1 = np.array([2, 8, 9])
print(v1.shape) # (3,)
print(v1.dtype) # int64

v1 = np.array([6.9, 0.5])
print(v1.shape) # (2,)
print(v1.dtype) # float64
```

Para criar arrays unidimensionais com valores padrão, a biblioteca oferece 
funções como `ones()` e `zeros()`, que geram um array do tamanho 
especificado preenchido, respectivamente, com o valor 1 ou zero.

```python
uns = np.ones(3)     # [1., 1., 1.]
zeros = np.zeros(6)  # [0., 0., 0., 0., 0., 0.]
```

### Indexação de arrays unidimensionais

A leitura de elementos individuais em um array unidimensional utiliza o operador de colchetes `[]` e segue a **indexação baseada em zero**.

```python
v = np.array([92, -30, 54, 78, -64, 88])
print(v[0]) # 92
print(v[1]) # -30
print(v[2]) # 54
print(v[5]) # 88
```

Se um índice especificado ultrapassar os limites do array, o Python interrompe a execução e retorna um erro do tipo `IndexError`.

```python
v = np.array([92, -30, 54, 78, -64, 88])
print(v[8]) # IndexError: index 8 is out of bounds for axis 0 with size 6
```

### Indexação Negativa
O NumPy suporta **índices negativos**, permitindo recuperar elementos a partir do final do array. O índice **`-1`** acessa o último elemento, enquanto **`-2`** acessa o penúltimo, estendendo-se até **`-5`** para o primeiro elemento (em um array de 5 itens).

```python
v = np.array([92, -30, 54, 78, -64])
print(v[-1]) # -64
print(v[-2]) # 78
print(v[-3]) # 54
print(v[-4]) # -30
print(v[-5]) # 92
```

---

### Fatiamento (*Slicing*) de arrays unidimensionais

O **fatiamento** extrai uma subsequência de um array e é amplamente utilizado em aprendizado de máquina para separar variáveis ou conjuntos de dados. A sintaxe utiliza o operador de dois pontos no formato `array[de:até]`, selecionando os elementos a partir do índice `de` até o item anterior ao índice `até`.

Exemplos de Fatiamento:

* **Seleção completa**: utilizar apenas `:` seleciona todos os elementos do array unidimensional.
* **Subsequência inicial**: o fatiamento `[0:1]` inicia no índice 0 e para antes do índice 1, retornando um sub-array com apenas o primeiro elemento.
* **Fatiamento com índices negativos**: a instrução `data[-2:]` inicia no segundo elemento contado a partir do final e vai até o término da dimensão, retornando os dois últimos itens.

```python
v = np.array([92, -30, 54, 78, -64, 100, 88])
print(v[:])     # [92, -30, 54, 78, -64, 100, 88]
print(v[0:3])   # [92, -30, 54]
print(v[2:5])   # [54, 78, -64]
print(v[:2])    # [92, -30]
print(v[4:])    # [-64, 100, 88]
print(v[-2:])   # [100, 88]
print(v[-5:-2]) # [54, 78, -64]
```

### Cálculo de normas

NumPy provê a função `linalg.norm` para o cálculo de normas. O parâmetro `ord` indica o tipo da norma desejada.

```python
# calculando norma L1
x = np.array([3, -4, 2])
norma_l1 = np.linalg.norm(x, ord=1)
print(norma_l1) # 9.0

# calculando norma L2
norma_l2 = np.linalg.norm(x, ord=2)
print(norma_l2) # 5.385164807134504
```

TODO: funções de agregação

```python

```

## Conclusão

TODO