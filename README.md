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
