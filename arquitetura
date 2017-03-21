# Arquitetura (Aula 3)

Modelos de Implementação de BD
1 - Modelo Hierárquico:Modelo hierárquico consiste numa colecção de registos em os dados 
se encontram relacionados entre si, através de ligações. Numa base de dados hierárquica 
pode fazer-se uma navegação de registo em registo, subindo ou descendo na estrutura hieárquica.
 

2 - Modelo em Rede (Network): É o modelo de dados que eliminou o conceito de hierarquia, 
permitindo que um mesmo registro estivesse envolvido em várias associações
 

3 - Modelo Relacional

** As propriedades ACID (atomicidade, consistência, isolamento e durabilidade)
são fundamentais nos bancos de dados, sejam os relacionais ou os orientados a documentos.
Então, também é valido tratarmos desse assunto referente aos bancos relacionais, em um contexto geral.

Atualmente os sistemas de informação suportam vários usuários. O banco de dados tem que garantir
a confiabilidade nas transações, haja vista que muitas podem ocorrer concorrentemente.

4 -O que é uma transação?
Uma transação é um programa em execução que forma uma unidade lógica de processamento no banco de dados. 
Uma transação inclui uma ou mais operações de acesso ao banco de dados — englobam operações de inserção, 
exclusão, alteração ou recuperação. 

6 - Por que a Restauração (Recuperação) é Necessária? O sistema deverá garantir que: (1) todas as operações 
na transação foram completadas com sucesso e seu efeito será gravado permanentemente no banco de dados ou (2) a transação 
não terá nenhum efei¬to sobre o banco de dados ou sobre quaisquer outras transações.

7 -	Atomicidade

A propriedade de atomicidade garante que as transações sejam atômicas (indivisíveis). A transação será executada totalmente ou não será executada.

8 -	Consistência

A propriedade de consistência garante que o banco de dados passará de uma forma consistente para outra forma consistente.

9 -	Isolamento

A propriedade de isolamento garante que a transação não será interferida por nenhuma outra transação concorrente.

10 - Durabilidade

A propriedade de durabilidade garante que o que foi salvo, não será mais perdido.

LINGUAGEM DE PROGRAMAÇÃO DE BANCO DE DADOS
DDL: Data Definition Language - Define o esquema do BD. - descreve as estruturas de dados do esquema, às vezes 
chamada de metadados, e a armazena em um dicionário de dados. 
 DCL: Data Control Language – Realiza controle do BD 
 DML: Data Manipulation Language – Realiza acesso ao BD para consultas e atualizações 
SQL: Structure Query Language Linguagem de programação de SGBDR que engloba: DDL, DCL e DML

RESTRIÇÕES DE INTEGRIDADE
Restrições de Integridade mais complexas: - unicidade de itens de dados; 
integridade referencial - uma instância de uma tabela que referencia outra tabela 
Ex. Existência de Dependentes em função de Funcionários. - restrições derivadas da semântica dos dados 
Ex.: um aluno não pode matricular-se na mesma disciplina mais de uma vez. - validação de dados 
Ex.: CPF, CNPJ, RG formatos; data de entrega menor que data da compra.

CAPACIDADE DE RECUPERAÇÃO
Backup/Restore: responsável por assegurar que o BD seja restaurado para seu estado anterior à falha,
recuperação de incidentes. • Load/Unload de dados: carga/descarga de objetos do BD, a partir de arquivos de dados. 
• Recovery automático: garante que as falhas ocorridas no processamento das transações 
não sejam propagadas aos objetos persistentes (quebra de integridade) SGBD deve prover 
facilidades para restaurar o banco de dados em caso de falha de hardware ou de software, ou mesmo falha da aplicação.

Modelo Conceitual: requerem uma representação abstrata, independente dos detalhes de armazenamento dos dados, que possa ser entendido por usuários finais. categoria de alto nível: próximo de como os usuários finais percebem os dados (como negócios da empresa)  Modelo Lógico: categoria de nível intermediário: pode ser entendido pelos usuários técnicos, mas não muito distante da forma de armazenamento dos dados  
Modelo Físico: descreve a organização dos arquivos do banco de dados e estrutura de dados, métodos de acesso, regras de integridade , etc

MODELO LÓGICO

Conhecidos como Modelos de Implementação
Modelo Relacional ou Diagrama Relacional – (DR) 
Descrevem dados por meio de estruturas de registros 
São classificados de acordo com o tipo de estrutura e as operações em que se baseiam.
 
DER 

GERÊNCIA DE TRANSAÇÕES DE BD
