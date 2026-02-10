## Introdução

Uma nova companhia aérea está para se lançar no mercado de logística, e está em fase pré-operacional. Nesta fase a empresa está fazendo o planejamento do quanto  de infraestrutura (aeronaves) e serviços (pessoal), além de quais aeroportos, precisará contratar.

A empresa deseja passar, ao menos uma vez, por todos os estados do país todos os dias, entregando encomendas de qualquer aeroporto da capital de estado para qualquer aeroporto na capital de todos os outros estados em no máximo 48 horas.

#### Seguem mais alguns detalhes da operação:
* Uma rota é composta por um Aeroporto de Origem, uma sequência de aeroportos intermediários e um Aeroporto de Destino
* Cada aeronave faz uma rota (indo e voltando no mesmo dia)
* As encomendas são depositadas em um aeroporto de origem tendo como destino outro aeroporto.
* A mesma encomenda pode cruzar diferentes rotas, passando por diferentes aeronaves.
* Em cada aeroporto do Vôo os aviões pousam, abastecem, desembarcam as encomendas com destino a esse aeroporto ou outros aeroportos fora da rota do avião (mas que passam por aquele aeroporto) e embarcam as encomendas cujo destino é um dos próximos aeroportos na rota do avião.
* Os tempos de vôo também incluem os tempos gastos na decolagem e pouso, mas não incluem o tempo parado em terra, que é de 35 minutos por aeroporto.
* As aeronaves começam a operar às 07hs da manhã e voam até às 22hs.
* A autonoma de vôo das aeronaves operadas pela empresa é de no máximo 2 horas (120min). Todos os vôos maiores do que essa faixa de tempo precisam de escalas.
* Nos anexos dessa atividade vocês encontrarão uma planilha com os dados dos principais aeroportos brasileiros, um de cada estado, e as distâncias (medidas em minutos de vôo) entre eles.

### Questões

**A)** Analisando os dados dos aeroportos e suas conexões, qual a representação de grafos mais eficiente? Justifique.

**B)** Dentro da malha aérea, deve-se escolher os aeroportos para as aeronaves pernoitarem. Deve-se escolher o menor número possível de aeroportos, capaz de cobrir o maior número possível de conexões;
**B.1)** Detalhe as técnicas da Teoria dos Grafos que foram empregadas na análise da solução desse problema;
**B.2)** Detalhe as estratégias de algoritmos que foram empregadas na determinação dos aeroportos.

**C)** Lembrando que as rotas devem passar pelo mesmo aeroporto apenas 2 vezes ao dia, uma no percurso de ida, outro no percurso de volta, como determinar o menor número de rotas que contemple o todos os aeroportos?
**C.1)** Detalhe as técnicas da Teoria dos Grafos que foram empregadas na análise da solução desse problema;
**C.2)** Detalhe as estratégias de algoritmos que foram empregadas na determinação das rotas.

**D)** Como as equipes de terra serão pequenas, deve-se evitar ter duas aeronaves chegando ou saindo no mesmo aeroporto na mesma janela de tempo.
**D.1)** Como montar a tabela de horários de vôos para atender à essa requisição?  Descreva a estratégia de algoritmos empregada;
**D.2)** Quais técnicas da Teoria dos Grafos podem ser empregadas na análise da solução desse problema?

**Atenção:**
O trabalho pode ser feito em trios
Deve-se entregar um Google Colab com todos os algoritmos, dados e respostas das questões.
#### Referências para os dados:

#### Dados de tempo de viagem:
https://www.ibge.gov.br/geociencias/organizacao-do-territorio/redes-e-fluxos-geograficos/15797-ligacoes-aereas.html?=&t=acesso-ao-produto

#### Dados dos aeroportos:
https://www.anac.gov.br/acesso-a-informacao/dados-abertos/areas-de-atuacao/aerodromos/lista-de-aerodromos-publicos/aerodromospublicosv1.xls/view


|EQUIPE|
|[Clebson Santos](https://github.com/ClebTech)|
|[Victor Guedes](https://github.com/VictorGuedesFPIF)|
|[Wallan Melo](https://github.com/WallanMelo)|