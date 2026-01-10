# 🗄️ Estudos de SQL para Suporte Técnico Júnior

Este arquivo contém anotações de estudos sobre a **linguagem SQL**, com foco em uso prático no contexto de **Suporte Técnico / Help Desk / Suporte a Sistemas**.

O objetivo é compreender consultas, análise de dados e apoio ao diagnóstico de problemas em sistemas que utilizam banco de dados.

---

## 📚 Conceitos Básicos de Banco de Dados

- Banco de dados armazena informações de forma organizada
- SQL (Structured Query Language) é a linguagem utilizada para acessar os dados
- Muito presente em sistemas corporativos, ERPs e aplicações internas

---

## 🧩 Estrutura Básica de um Banco de Dados

Principais conceitos:

- **Banco de dados**
- **Tabelas**
- **Colunas (campos)**
- **Linhas (registros)**

---

## 🔍 Consultas Básicas (SELECT)

Utilização do comando `SELECT` para consulta de dados.


 - **SELECT * FROM clientes;**

Selecionando colunas específicas:

- **SELECT nome, email FROM clientes;**

---

## 🎯 Filtros com WHERE

Utilizado para retornar apenas registros específicos.

- **SELECT * FROM pedidos
WHERE status = 'aberto';**

*Uso comum no suporte:
Análise de registros
Validação de dados
Apoio a investigações de erro*

---

## 📊 Ordenação de Dados (ORDER BY)

- **SELECT * FROM chamados
ORDER BY data_abertura DESC;**

---

## 🔢 Limitação de Resultados (LIMIT)

- **SELECT * FROM logs
LIMIT 10;**

---

## 🔗 Relacionamento entre Tabelas (JOIN)
 
 Noções práticas de relacionamento entre tabelas.

- **SELECT clientes.nome, pedidos.id
FROM clientes
JOIN pedidos ON clientes.id = pedidos.cliente_id;**

---

## 🧠 Funções Básicas


Conhecimento em funções agregadas:

- **COUNT()**
- **SUM()**
- **AVG()**

- **SELECT COUNT(*) FROM chamados;**

---

## 🔍 Subconsultas (Conhecimento Atual)
Utilização de subconsultas para consultas mais elaboradas.
Exemplo:

 - **SELECT nome
FROM clientes
WHERE id IN (
    SELECT cliente_id
    FROM pedidos
    WHERE status = 'aberto'
);**

*Aplicação no suporte:*

*Análise de dados relacionados
Investigações mais detalhadas em sistemas
🧱 CTE – Common Table Expressions (Em Aprendizado)
Estudo em andamento sobre CTE, utilizadas para melhorar organização e legibilidade das consultas.
Exemplo básico:*

 - **WITH pedidos_abertos AS (
    SELECT cliente_id
    FROM pedidos
    WHERE status = 'aberto'
)
SELECT *
FROM clientes
WHERE id IN (SELECT cliente_id FROM pedidos_abertos);**

---

## 👁️ Views (Em Aprendizado)

Estudo introdutório sobre Views, utilizadas para criar consultas armazenadas.
Conceito:

View é uma consulta salva que pode ser reutilizada
Facilita leitura e padronização de dados

---

## 🛠️ Aplicação do SQL no Suporte Técnico

Uso do SQL para:

- **Consulta de dados em sistemas**
- **Validação de informações**
- **Apoio ao atendimento ao cliente**
- **Análise básica de erros e registros**

---

## 🔒 Boas Práticas

- **Utilizar apenas comandos de consulta quando não autorizado**
- **Conferir filtros antes de executar consultas**
- **Evitar alterações diretas em produção**
- **Atenção a dados sensíveis**

---

## 📌 Próximos Conteúdos a Evoluir

- **CTE (aprofundamento)**
- **Views (criação e manutenção)**
- **Otimização de consultas**
- **Índices**
- **Controle de permissões**

---

## 🧠 Observações Pessoais

- **SQL é uma ferramenta importante para suporte a sistemas**
- **Ajuda a entender melhor o funcionamento das aplicações**
- **Este conteúdo será atualizado conforme evolução nos estudos**

📅 Última atualização: Janeiro / 2026
