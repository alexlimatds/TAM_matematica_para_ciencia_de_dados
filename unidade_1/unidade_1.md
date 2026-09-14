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

## Vetores e Escalares

Em álgebra linear, os conceitos de escalar e vetor são as unidades fundamentais. Um **escalar** é um único número 
real (ou complexo), como $$3$$, $$-0,5$$, $$\pi$$, e representa magnitude sem direção. Escalares são geralmente 
denotados por letras minúsculas. Em ML, exemplos de escalares são: a taxa de aprendizado ($$\alpha$$), o número 
de épocas, a acurácia de um modelo, etc.

Um **vetor** é um arranjo ordenado de escalares. O número de elementos, ou componentes, é chamado de dimensão ou dimensionalidade 
do vetor. Por exemplo, um indivíduo de 25 anos, com salário de R$30,50 por hora e 5 anos de experiência pode ser 
representado pelo vetor de características $$\textbf{x} \in \mathbb{R}^{3}$$:

$$\textbf{x} = \begin{pmatrix} 25 & 30,5 & 5 \end{pmatrix}$$

Para denotar um vetor $$\textbf{v}$$ com $$n$$ componentes de forma genérica, escrevemos:

$$
\textbf{v} = \begin{pmatrix}
v_1 & v_2 & \cdots & v_n 
\end{pmatrix}
$$

Quando os elementos do vetor estão dipostos na horizontal, chamamos o vetor de vetor linha. Também podemos dispor os elementos de um vetor na horizontal (vetor coluna):

$$
\textbf{v} = \begin{pmatrix}
v_1 \\
v_2 \\
\vdots  \\
v_n
\end{pmatrix}
$$

Repare que, neste texto, denotamos vetores por meio de letras minúsculas grafadas em negrito.

Em ML, um vetor representa tipicamente uma amostra (um paciente com $$n$$ exames, uma casa com $$n$$ características) ou um conjunto de parâmetros (os pesos de um modelo).

