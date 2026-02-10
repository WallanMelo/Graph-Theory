# Sistema de Recomendação

## DESCRIÇÃO


Uma rede social conecta as pessoas no formato de seguidores, onde uma pessoa A segue outra pessoa B, que não necessariamente a segue de volta. Essa rede social tem um mecanismo para mensurar o grau de afinidade desses relacionamentos, contando quantas vezes cada pessoa interagiu (curtiu ou comentou) postagens de cada pessoa que ela segue.

A mesma rede social oferece anúncios de produtos para empresas com as opções de curtir( voto positivo)  ou não curtir (voto negativo) cada produto, como uma forma de avaliar o que cada pessoa pensa de cada produto visualizado. Se um usuário visualiza o produto e não interaje, considera-se que ele deu um voto neutro para o produto.

Os estrategistas da rede social desejam aprimorar a forma como recomendam produtos para os seus usuários a partir das avaliações que seus contatos fizeram. 

Sugira um algoritmo que recomende k produtos para cada usuário baseando-se simultaneamente pelo grau de interação entre os contatos e pelo grau de avaliação dos produtos nas avaliações dos contatos da sua rede.

### DICAS:
Use a representação por Matriz de Adjacências para facilitar


## PEDE-SE:
O algoritmo de recomendação de produtos que retorne um dicionário contendo uma entrada para cada usuário e associada à essa chave a lista dos k produtos recomendados
O algoritmo deve receber como parâmetros:
A Matriz de Adjacências dos contatos entre os usuários
A Matriz de Adjacências das avaliações dos produtos pelo usuário
Um valor inteiro k, com o número de produtos a serem recomendados

#### Explique qual a estratégia adotada para encontrar os k produtos a serem recomendados 

**Resposta:** 

A estratégia adotada para encontrar os K produtos recomenddados baseia-se na ideia da influencia social ponderada, então as recomendações utilizam um comportamento de indicação de uma rede social onde a opinião de contatos com maior afinidade tem um peso maior, calculo que é feito atraves do Score = Somatorio(Afifnidade * Avaliação) ou seja utilizando as mqtrizes de contatos e avaliações

Isso significa que a opinião de um contato com alta afinidade (ex: peso 200) impacta muito mais o score final do que a opinião de um contato com baixa interação (ex: peso 1).

2. Filtro de Ineditismo:Para evitar recomendar produtos que o usuário já conhece, o algoritmo identifica os produtos já avaliados pelo usuário na matriz de compras e atribui a eles um valor infinitamente negativo ($- \infty$). Isso garante que, ao ordenar os resultados, apenas produtos inéditos ocupem as primeiras posições.3. Seleção dos K-Melhores:Por fim, o algoritmo ordena os scores resultantes do maior para o menor e seleciona os k índices de produtos com maior pontuação social acumulada, entregando uma lista personalizada para cada usuário no sistema.