# 2ª Lista de Exercícios de Grafos


## Questão 1
### HIPERCUBOS:
Um hipercubo é um grafo não-orientado G = {V,E}, onde os vértices de V são strings binárias de tamanho S. Dois vértices i,j ∈ V estão conectados se, e somente se, as strings representadas por i e j diferem em somente um dígito. Por exemplo: 

O 1-hipercubo é o grafo G = {V,E}, tal que V = {0,1} e E = {(0,1)}
O 2-hipercubo é o grafo G = {V,E}, tal que V = { '00', '01', '10', '11' } e E = { ('00', '01'), ('00', '10'), ('11', '01'), ('11', '10') }

**a)** Crie um algoritmo que aceite um parâmetro S crie hipercubos de tamanho S, gerando o conjuntos V e E do hipercubo.
**b)** Ache e explique uma fórmula fechada para calcular o número de vértices de um hipercubo cujos vértices são strings de tamanho S
**c)** Ache e explique uma fórmula fechada para calcular o número de arestas de um hipercubo cujos vértices são strings de tamanho S

**Respostas**
a) Algoritmo para gerar V e E
O algoritmo utiliza a técnica de gerar todas as combinações binárias para os vértices e, para as arestas, verifica a Distância de Hamming (quantos bits são diferentes) entre cada par.

b) Fórmula para o número de vértices (|V|)
A fórmula fechada é: |V| = 2^s
Explicação: Cada posição da string binária de tamanho S tem 2 opções de valores (0 ou 1). Pelo Princípio Fundamental da Contagem, para S posições independentes, temos 2 x 2 x ... 2x (S vezes), resultando em 2^S combinações únicas.

c) Fórmula para o número de arestas (|E|)A fórmula fechada é: |E| = S * 2^s-1
Explicação: Cada um dos $2^S$ vértices está conectado a exatamente $S$ vizinhos (pois podemos inverter qualquer um dos $S$ bits para criar um novo vizinho). Se multiplicarmos o número de vértices pelo seu grau, temos $S \cdot 2^S$. Como o grafo é não-orientado, cada aresta foi contada duas vezes (uma para cada ponta). Dividindo por 2, chegamos a (s*2^s)/2 = S * 2^s-1.


## Questão 2
### JOGO DA VELHA:
O cada situação possível de um jogo da velha pode ser representado por uma string de 9 posições, cada posição representando uma das 9 casas do tabuleiro e cada casa pode ter um dos seguintes valores:
: Casa vazia
x: Casa ocupada por um x
o: Casa ocupada por um o
**a)** Gere o grafo de SEMI-hipercubo de todas jogadas possíveis do Jogo da Velha a partir do vértice inicial '---------'. O "semi" significa que ele não será um hipercubo perfeito, pois dois vértices para serem vizinhos não bastam ter um dígito diferente, mas um dígito diferente de um jogador diferente (ou seja: uma jogada 'x' deve ser seguida por uma jogada 'o' para serem vizinhos, e vice versa)
**b)** Modifique o algoritmo de Árvores Geradoras para criar, a partir do hipercubo anterior, uma árvore de todas as próximas jogadas possíveis a partir de uma jogada inicial.

**Resposta**
a) Grafo de SEMI-hipercubo
O algoritmo represenetado pela função gerar_grafo_velha, gera o grafo respeitando a alternância de turnos  

b) Algoritmo de Árvore Geradora
Para criar a árvore de todas as jogadas a partir de um estado inicial, adaptamos a Busca em Largura (BFS). Note que, para ser uma árvore de jogadas, não reusamos estados visitados em ramos diferentes se quisermos a árvore de decisão completa, mas para uma Árvore Geradora simples do grafo, usamos um conjunto de visitados: