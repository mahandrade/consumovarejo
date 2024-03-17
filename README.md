# Consumo Cliente – Sistema de Varejo para Eletrônicos

O presente relatório apresenta o projeto do banco de dados SVE
(Sistema de Varejo para Eletrônicos). Especificamente, o relatório apresenta o
resultado das atividades de especificação do minimundo, análise de requisitos,
projeto conceitual, projeto lógico e projeto físico do SVE. 
As informações necessárias para a realização das atividades de modelagem foram coletadas a
partir de especificações textuais.
O banco de dados SVE foi concebido dentro do paradigma relacional utilizando como base o modelo relacional, sendo
constituído por um conjunto de entidades. Fisicamente, o banco de dados é composto por seis arquivos indexados com 
índice em cada um dos campos correspondentes às chaves primárias das tabelas de origem

# Requisitos Funcionais
Os variados grupos de clientes demandarão diferentes operações de manipulação de
dados sobre diferentes porções do banco de dados. O grupo Gerência demandará
atualização e recuperação de dados sobre praticamente todas os elementos do banco de
dados, uma vez que esse grupo será o responsável por manter os dados atualizados, dando
suporte aos outros grupos. O grupo vendedor demandará consultas de recuperação de
dados. O grupo cliente demandará consultas para atualização de seus dados cadastrais e
para manipulação de dados sobre suas compras. O grupo geral demandará recuperação de
dados sobre as compras, vendas, custos, cor, categoria e tipo de produto eletrônico. A
Tabela 1 apresenta as principais consultas que cada grupo de usuários demandará ao
sistema de banco de dados, bem como a frequência esperada de submissão (A para alta,
M para média e B para baixa.
Tabela 1: Frequência esperada de consultas por grupo de usuário
# Consulta Grupo Frequência
Q001 Listar todas as lojas cadastradas no sistema                 |Gerência  |M
| ------------------------------------------------------------------------------ |
Q002 Encontrar a loja com o maior número de vendas                |Geral     |B
| ----------------------------------------------------------------|--------------|
Q003 Listar todos os vendedores cadastrados no sistema            |Gerência  |B
| ----------------------------------------------------------------|--------------|
Q004 Encontrar o vendedor que mais vendeu no último mês           |Gerência  |M
| ----------------------------------------------------------------|--------------|
Q005 Listar todas as vendas realizadas no sistema                 |Vendedor  |A
| ----------------------------------------------------------------|--------------|
Q006 Encontrar as vendas realizadas entre duas datas específicas  |Vendedor  |A
| ----------------------------------------------------------------|--------------|
Q007 Inserir um novo produto na tabela de produtos                |Gerência  |A
| ----------------------------------------------------------------|--------------|
Q008 Listar todos os fornecedores cadastrados no sistema          |Gerência  |M
| ----------------------------------------------------------------|--------------|
Q009 Inserir um novo fornecedor na tabela de fornecedores         |Gerência  |A
| ----------------------------------------------------------------|--------------|
Q010 Encontrar a receita total de uma loja                        |Gerência  |M
| ----------------------------------------------------------------|--------------|
Q011 Listar vendas por vendedor (qual vendedor realizou a venda)  |Vendedor  |A
| ----------------------------------------------------------------|--------------|
Q012 Inserir um novo cliente no banco de dados                    |Geral     |B
| ----------------------------------------------------------------|--------------|
Q013 Listar clientes por vendedor                                 |Vendedor  |B
| ----------------------------------------------------------------|--------------|
Q014 Encontra os produtos que nunca foram vendidos                |Vendedor  |M
| ----------------------------------------------------------------|--------------|
Q015 Listar todos os clientes cadastrados no sistema              |Vendedor  |M
| ----------------------------------------------------------------|--------------|
Q016 Contar quantas compra foram efetuadas por cliente            |Vendedor  |M
| ----------------------------------------------------------------|--------------|
Q017 Visualizar compras realizadas por cliente                    |Cliente   |M
| ----------------------------------------------------------------|--------------|
Q018 Atualizar dados cadastrais do cliente                        |Cliente   |M



