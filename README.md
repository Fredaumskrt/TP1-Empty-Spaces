# TP1-Empty-Spaces

O presente relatório descreve a implementação do controle de espaços dos registros excluídos
em um sistema CRUD (Create, Read, Update, Delete) genérico, conforme solicitado no primeiro
trabalho prático da disciplina. Este sistema foi desenvolvido com o objetivo de gerenciar
registros em um banco de dados, permitindo operações básicas de manipulação de dados.
O controle de espaços vazios de registros excluídos visa otimizar o uso de memória e melhorar a eficiência do sistema.
A estrutura do sistema é baseada em uma implementação de CRUD genérico,
onde cada registro é composto por três campos principais: lápide, indicador de tamanho do registro e vetor de bytes.
A lápide indica se o registro é válido ou excluído, o indicador de tamanho do
registro armazena o tamanho do vetor de bytes e o vetor de bytes contém os dados do registro.
O controle de espaços vazios de registros excluídos é realizado mediante a marcação desses espaços com um "*" no campo lápide. 
Esses espaços vazios são gerados durante as operações de exclusão de registro ou de alteração de registro que resulta no aumento do seu tamanho.
A marcação das lápides permite identificar facilmente os registros excluídos e reaproveitar esses espaços vazios quando necessário.
Foi desenvolvida uma rotina que permite o reaproveitamento dos espaços vazios de registros excluídos. Essa rotina
é avaliada toda vez que uma operação de inclusão de um novo registro ou de alteração de um registro com aumento
de tamanho é realizada. Nas operações de exclusão e de alteração, o código foi ajustado para permitir o controle dos espaços vazios.
Para garantir um uso eficiente dos espaços vazios, foram considerados os seguintes critérios:

Desperdício Aceitável: Foi definido um limite aceitável de desperdício de espaço, que pode ser expresso como uma porcentagem do espaço disponível
ou como uma quantidade máxima de desperdício em número de bytes.

Tamanho Mínimo do Espaço Vazio: Foi estabelecido um tamanho mínimo para os espaços vazios.
Se um espaço vazio for menor que esse tamanho mínimo, ele será incorporado ao registro anterior, evitando o desperdício de espaço.
A implementação do controle de espaços dos registros excluídos proporciona uma gestão mais eficiente da memória
e melhora o desempenho do sistema CRUD. Ao reaproveitar os espaços vazios,
conseguimos reduzir o desperdício de espaço e otimizar a utilização dos recursos disponíveis.
Os critérios estabelecidos para o reaproveitamento dos espaços vazios garantem um equilíbrio entre eficiência e complexidade do sistema.

1 - O que você considerou como perda aceitável para o reuso de espaços vazios, isto é, quais são os critérios para a gestão dos espaços vazios?
R:
2 - O código do CRUD com arquivos de tipos genéricos está funcionando corretamente? 
R: Sim, está funcionando conforme o modelo fornecedido pelo professor!
3 - O CRUD tem um índice direto implementado com a tabela hash extensível?
R:
4 - A operação de inclusão busca o espaço vazio mais adequado para o novo registro antes de acrescentá-lo ao fim do arquivo?
R:
5 - A operação de alteração busca o espaço vazio mais adequado para o registro quando ele cresce de tamanho antes de acrescentá-lo ao fim do arquivo?
R:
6 - As operações de alteração (quando for o caso) e de exclusão estão gerenciando os espaços vazios para que possam ser reaproveitados?
R:
7 - O trabalho está funcionando corretamente?
R: Sim, tirando a parte de hash que nos retorna 'null'
8 - O trabalho está completo?
R: Sim, está parcialmente completo, só a parte de hash que enfretamos um problema que infelizmente não conseguimos resolver, podemos analisar no teste que aparece um 'null', a lógica está implementada, porém com esse erro!
9 - O trabalho é original e não a cópia de um trabalho de um colega?
R: O trabalho é autêntico, não utilizando nenhuma parte do trabalho de colega nenhum. Utilizamos apenas os modelos e exemplos fornecidos pelo professor!
