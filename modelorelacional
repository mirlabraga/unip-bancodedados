** Modelo Relacional

 

No Modelo Relacional todos os dados ficam armazenados em tabelas do tipo linha x coluna.

 

Tabela é um conjunto não ordenado de linhas (tuplas, na terminologia acadêmica)

Cada linha é composta por uma série de campos (valor de atributo na terminologia acadêmica)

Cada campo é identificado por um nome de campo (nome de atributo, na terminologia acadêmica)

 

O conjunto de valores de um campo forma uma coluna da tabela. Para cada coluna da tabela deve ser definido o seu domínio de valores, que é o universo de valores possíveis para a mesma.

 

            Empregado

 

Código

Nome

Cod Departamento

Categ Funcional

145

Jose Silva

D1

A4

152

Antonio Souza

D2

A1

198

Maria Oliveira

D1

A2

176

Carlos Silva

D3

A1

 

 

Tabela com dados de empregados.

 

Cada linha representa uma tupla

As linhas de uma tabela não têm ordenação - a ordem de recuperação é arbitrária, a menos que uma ordenação seja especificada na instrução de consulta

Não existem linhas duplicadas

Não é possível referenciar linhas de uma tabela por posição

Os valores de campo de uma tabela são atômicos e monovalorados

As consultas podem ser feitas por qualquer critério envolvendo os campos de uma ou mais linhas

            Dependente de Empregado

Código Empregado

Nro

Nome

145

1

Jose Silva Jr

145

2

Antonio Silva

198

1

Joaquim Oliveira

176

1

Carlos Silva Jr

176

2

Marcos Silva

176

3

Antonio Silva

Tabela com os Dependentes dos Empregados

 

- Chave Candidata:

Campo ou conjunto de campos da tabela cujo valor identifica de forma única cada linha da tabela e é mínimo nessa condição. 

 

A exigência de mínimo é que todos os campos sejam efetivamente necessários para garantir o requisito de unicidade dos valores da chave.

Toda tabela, por não possuir linhas duplicadas, tem ao menos uma chave candidata.

 

No exemplo acima, o campo Código é uma chave candidata, assumindo que não pode haver repetição de valor de código.

Ainda que não existam dois nomes iguais na tabela acima, não se pode assumir o campo Nome como uma chave candidata, por que este é um valor próprio das pessoas que sejam contratadas como empregados e poderão ser incluídos novos empregados com nomes iguais aos já existentes.

 

Se a tabela Empregado tivesse as colunas CPF e PIS, cujos valores são únicos para cada pessoa, e esses campos sempre tivessem valor em todas as linhas, cada um deles também seria uma chave candidata.

 As chaves candidatas também são chamadas chaves alternativas.

 

A tabela Dependente de Empregado tem como chave candidata o par
(Código Empregado, Nro). Esse par é mínimo por que os dois valores são necessários para identificar uma linha da tabela.

 

- Chave Primária

Toda tabela tem uma Chave Primária.

A chave primária de uma tabela é uma das suas chaves candidatas.

Qualquer chave candidata, ou chave alternativa, pode ser escolhida para ser a chave primária de uma tabela.

 

Na tabela Empregado acima, a única chave candidata é o campo Código, logo Código é a Chave Primária da tabela Empregado.

 

Na tabela Dependente de Empregado a chave primária é o par (Código Empregado, Nro).

 

Se considerarmos a mesma tabela Empregado com os campos CPF e PIS, ela terá três chaves candidatas: Código, CPF e PIS.

Nesse caso, qualquer uma das três pode ser escolhida para ser a chave primária da tabela. Não existe nenhuma regra para determinar qual delas tem que ser a escolhida, porém essa escolha tem que ser feita com critério por que mudar a chave primária de uma tabela em um modelo de dados pronto pode ser um processo bastante complexo.

 

Entre os critérios a analisar na escolha da chave primária entra o conceito de chave estrangeira, a ser apresentado a seguir.

 

- Chave Estrangeira

           

Chave Estrangeira é uma coluna ou conjunto de colunas de uma tabela cujo domínio de valores são os valores da chave primária de uma tabela.

 

A associação entre chave primária e chave estrangeira é o recurso que existe no modelo Relacional para implementar o relacionamento entre tabelas.

 

Na tabela Dependente de Empregado o campo Código Empregado é uma chave estrangeira que referencia a chave primária Código da tabela Empregado.

 

Representação Gráfica do Modelo Relacional

 

Na representação do modelo relacional o único objeto que pode ser representado são as tabelas, que são representadas utilizando retângulos.

 

O relacionamento entre tabelas, determinado pela presença de uma chave estrangeira é representado por uma linha, com uma indicação do lado onde está a chave estrangeira.

 

- Tabela:

 

 

Chave estrangeira opcional:

 

 

 
Chave estrangeira obrigatória (não nula):

 

 
 

Exemplos:

 

Tabela Empregado possui uma chave estrangeira que referencia a chave primária de Departamento, indicando o Departamento onde trabalha o Empregado. Como a chave estrangeira está representada como opcional, indica que um Empregado pode não estar relacionado a nenhum Departamento.

 

A chave estrangeira estabelece um relacionamento 1:n entre as tabelas. Usando a notação de cardinalidade do modelo entidade-relacionamento, o relacionamento acima é do tipo,  (0,1):(0,n), ou seja, opcional nos dois extremos.

 

 

 

Dois relacionamentos estabelecidos por chaves estrangeiras. A tabela Participa_Proj possui duas chaves estrangeiras, uma referenciando a chave primária de Engenheiro e outra referenciando a chave primária de Projeto. Ambas são obrigatórias.

O relacionamentos Engenheiro (1:n) Participa_Proj   e Participa_Proj (n:1) Projeto estabelecem, de forma indireta, um relacionamento n:n entre Engenheiro e Projeto.

No modelo relacional não podem ser representados diretamente relacionamentos n:n.

 

 

Modelo Relacional – Restrições de Integridade Lógica

Um sistema de informação somente tem valor se os dados que apresenta refletem corretamente a realidade representada. Assim, uma das maiores preocupações daqueles que trabalham com informação é a integridade dos dados.

Dizer que os dados em um banco de dados estão íntegros é dizer que eles estão exatamente como se pressupôs que deveriam estar quando se fez a análise de dados e se construiu o modelo de dados.

Um SGBD possui mecanismos que ajudam a garantir tanto a integridade lógica, que é aquela estabelecida pela modelagem de dados, quanto a integridade física, que é garantir que o que se encontra no banco de dados e dali se recupera é exatamente aquilo que ali se colocou.

Para garantir a integridade lógica dos dados os SGBD relacionais possuem mecanismos que implementam restrições de integridade que são regras de integridade dos dados declaradas na especificação do modelo de dados e garantidas automaticamente pelo SGBD.

Os tipos de integridade de dados declarativas são:

Integridade de Domínio

Na definição de cada coluna de uma tabela é definido o tipo e tamanho de dado (numérico, alfanumérico, data, hora, etc) aceito na coluna. Também podem ser definidas regras de controle de valor baseados em fórmulas ou conjunto de valores, por ex., (masc, fem), (sim, não).

Integridade de Vazio ou Nulo

No Modelo Relacional existe a possibilidade de definir se os campos em uma linha da tabela podem ficar vazios, sem nenhum valor. Um campo que não possa ficar vazio é um campo obrigatório. Um campo que possa ficar vazio é um campo opcional nas ocorrências da tabela.

 

Vazio ou Nulo é diferente de zero ou em branco, que são valores.

Campos que compõem a chave primária de uma tabela não podem ser nulos.

 

Integridade de Chave Primária

A chave primária de uma tabela obedece as seguintes regras de integridade:

sempre possui valor

o valor da chave primária é único na tabela

Integridade de Chave Candidata - Unicidade

Não há nos SGBDs uma definição específica para chave candidata, porém as chaves candidatas podem ser definidas com a restrição de ter valor único.

Integridade Referencial

A integridade referencial é estabelecida pela definição de uma chave estrangeira em uma tabela.

 

Exemplo:

Tabelas:

Departamento (Código, Nome)

Empregado (Matricula, Nome, CPF, Cargo, Cod_Departamento)

O campo Cod_Departamento em Empregado é uma chave estrangeira que referencia a chave primária de Departamento.



 

 

 

 

As seguintes regras de integridade referencial serão automaticamente controladas pelo SGBD:

Para simplificar e generalizar os conceitos, as tabelas serão relacionadas serão referenciadas por:

Tabela Mãe: tabela onde está a chave primária referenciada (Departamento, no exemplo)

Tabela Filho: tabela onde está a chave estrangeira (Empregado, no exemplo)

 

Inclusão na tabela Filho: o valor da chave estrangeira tem que existir na chave primária em uma das linhas da tabela Mãe. Se a chave estrangeira for opcional (aceitar nulo), como no exemplo, ela pode ficar nula.

Exclusão na tabela Mãe: somente poderá ser feita se a chave primária da linha a ser excluída não estiver referenciada por nenhuma linha na tabela Filho

Alteração da chave primária da tabela Mãe: somente poderá ser feita se a chave primária da linha a ser excluída não estiver referenciada por nenhuma linha na tabela Filho

Outras operações de inclusão, alteração ou exclusão nas duas tabelas podem ser realizadas sem restrições.

 

Integridades Semânticas

Além das restrições de integridade declarativas, garantidas automaticamente pelos SGBDs, um banco de dados pode ter restrições de integridade que dependam das condições e de outros valores existentes no banco de dados.

Por exemplo:

o salário de um empregado não pode ser maior do que o de outro empregado que exerça a mesma função mas que trabalha há mais tempo na empresa

um empregado somente pode ser designado motorista de um certo tipo de veículo se possuir a devida habilitação

Esse tipo de restrição não pode ser definida diretamente na declaração do banco de dados exigindo que seja feita programação específica de controle, que tanto pode ser feita nos programas dos sistemas aplicativos como também podem ser programadas nos próprios SGBDs.

 

Bibliografia

Cap 4, HEUSER, C. A. Projeto de bancos de dados. Porto Alegre: Sagra-Luzzatto, 2000.
