apeamento do Modelo Entidade- Relacionamento para o Modelo Relacional

 

Na construção de um modelo de dados, a primeira etapa é a construção do modelo conceitual, onde não existe nenhuma restrição do tipo de SGBD a ser utilizado e principal objetivo é o conhecimento dos dados e os seus relacionamentos.

A etapa seguinte é a definição do modelo lógico de acordo com o SGBD a ser utilizado. No caso, SGBD do tipo relacional.

No que segue apresentamos os principais princípios no mapeamento de um modelo entidade-relacionamento para o modelo relacional.

 

Entidades x Tabelas

Cada Entidade é mapeada como uma Tabela

 

Atributos simples x Campos

Atributos simples das Entidades são mapeados como campos das Tabelas

 

Identificador x Chave Primária

O Identificador de uma Entidade é também a chave primária da Tabela mapeada.

 

Atributos Multi-valorados

Numa entidade Cliente, o atributo telefone pode ser multi-valorado.

 

Uma tabela somente pode conter campos monovalorados. A solução é criar uma tabela para o atributo multi-valorado, tendo a chave primária formada pela composição da chave da tabela/entidade e pelo atributo multi-valorado.

Cliente (Código, nome)

Telefone Cliente (Código Cliente, telefone)

Os campos sublinhados formam a chave primária de cada tabela.

 

 

Atributos Compostos

Converter cada componente do atributo composto em uma coluna da tabela.

 

Mapeamento de Relacionamentos

Um relacionamento pode ser mapeado como uma nova tabela ou como atributos em uma das tabelas/entidades relacionadas, ou até mesmo pela fusão das 2 entidades em uma só tabela.

 

Mapeamento de Relacionamento 1:1

  

Exemplos:

 

Tipo do relacionamento: Opcional nos dois extremos.

Alternativa: adição de coluna como chave estrangeira em uma das duas tabelas.

 

 

Adição na Tabela Homem:

Homem ( Ident_H, Nome, Ident_conjuge, data, regime)

Mulher ( Ident_M, Nome)

 

Ident_conjuge é uma chave estrangeira que referencia a chave primária Ident_M na tabela Mulher.

 

Adição na Tabela Mulher:

Mulher ( Ident_M, Nome, Ident_conjuge, data, regime)

Homem ( Ident_H, Nome)

 

Nesta caso, Ident_conjuge é uma chave estrangeira que referencia a chave primária Ident_H na tabela Homem.

 

As duas alternativas são equivalentes.

 

Tipo do relacionamento: Obrigatório em um dos extremos.

Alternativa: fusão das tabelas

 

 

 A alternativa de adição de chave estrangeira em uma das tabelas também é aplicável. Nesse caso, o recomendável é que seja na tabela que obrigatoriamente tem que se relacionar com a outra (Cartão Magnético, no exemplo).

Correntista (CodCorrent, Nome)

Cartão Magnético (CodCartão, DataExp, CodCorrentCartão)

 CodCorrentCartâo é uma chave estrangeira que referencia a chave primária CodCorrent na tabela Correntista.

 

Mapeamento de Relacionamento 1:n

 

 

 A alternativa deve ser a adição de colunas (chave estrangeira) na tabela que está do lado n do relacionamento. Junto com ela devem também ser incluídas colunas que mapeiam os atributos do relacionamento.

  

 

  

Mapeamento de Relacionamento n:n

 

 

No modelo relacional não há possibilidade de implementar diretamente um relacionamento n:n.

Para implementar um relacionamento n:n deve ser criada uma tabela correspondente ao relacionamento, com duas chaves estrangeiras, cada uma referenciando uma das tabelas/entidades e mais os atributos presentes no relacionamento. A chave primária dessa terceira tabela será a composição das duas chaves estrangeiras.

 

 

 

Mapeamento de Entidades Especializadas

Se a especialização de uma entidade faz sentido no modelo conceitual ela tem que ser preservada no modelo lógico.

 

 

 Entidade Principal:

 Prestadores de Serviço ( CPF, nome, endereco)

 Entidades Especializadas: uma tabela para cada uma delas, tendo chave primária equivalente à chave primária da Entidade Principal.

 Horistas ( CPF Horista, custo hora, horas trabalho)

 Mensalistas (CPF Mensalista, Salario)

 

CPF Horista, além de ser chave primária de Horistas, também é uma chave estrangeira que referencia a chave primária CPF na tabela Prestadores de Serviço.

CPF Mensalista, além de ser chave primária de Mensalistas, também é uma chave estrangeira que referencia a chave primária CPF na tabela Prestadores de Serviço. 

 

Bibliografia

Cap 5, HEUSER, C. A. Projeto de bancos de dados. Porto Alegre: Sagra-Luzzatto, 2000.

 
