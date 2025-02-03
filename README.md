-- 📙 **Guia de SQL para Iniciantes**

---

# 📋 **Índice**

1. [Introdução](#introdução)
2. [Exemplo de Comando SQL](#exemplo-de-comando-sql)
3. [Exemplo de Consulta com DISTINCT](#exemplo-de-consulta-com-distinct)
4. [Exemplo com Duas Condições no WHERE](#exemplo-com-duas-condições-no-where)
5. [Exemplo de Consulta com Datas](#exemplo-de-consulta-com-datas)
6. [Conclusão](#conclusão)

---

# 🌟 **Introdução**

Um **banco de dados** é um local onde informações são armazenadas de forma organizada para serem acessadas, gerenciadas e atualizadas facilmente.

O **SQL** (*Structured Query Language*) é a linguagem usada para se comunicar com **bancos de dados relacionais**. Ele permite **buscar**, **inserir**, **atualizar** e **excluir** dados de forma estruturada.

---

# 📂 **Exemplo de Comando SQL**

### 🔹 Buscar o ano, cargo e sigla de uma tabela chamada `funcionarios`
```sql
SELECT ano, cargo, sigla 
FROM funcionarios;
```

### 🔹 Buscar apenas os funcionários da cidade de **Rio de Janeiro**
```sql
SELECT ano, cargo, sigla 
FROM funcionarios 
WHERE cidade = 'Rio de Janeiro';
```

### 🔹 Limitar a consulta aos **5 primeiros resultados**
```sql
SELECT ano, cargo, sigla 
FROM funcionarios 
WHERE cidade = 'Rio de Janeiro' 
LIMIT 5;
```

---

# 📌 **Exemplo de Consulta com DISTINCT**

### 🔹 Listar todas as **cidades** onde houve pedidos, sem duplicatas
```sql
SELECT DISTINCT cidade 
FROM pedidos;
```

### 🔹 Listar os **nomes dos clientes únicos** que fizeram pedidos
```sql
SELECT DISTINCT nome_cliente 
FROM pedidos;
```

---

# 🔍 **Exemplo com Duas Condições no WHERE**

### 🔹 Buscar funcionários que sejam **Gerentes** e trabalhem na cidade de **São Paulo**
```sql
SELECT nome, cargo, cidade 
FROM funcionarios 
WHERE cargo = 'Gerente' 
AND cidade = 'São Paulo';
```

### 🔹 Buscar funcionários que sejam **Gerentes** ou que trabalhem em **São Paulo**
```sql
SELECT nome, cargo, cidade 
FROM funcionarios 
WHERE cargo = 'Gerente' 
OR cidade = 'São Paulo';
```

| Operador | Descrição |
|----------|-------------|
| **AND**  | Retorna apenas os registros que atendem **às duas condições** ao mesmo tempo. |
| **OR**   | Retorna os registros que atendem **pelo menos uma** das condições. |

---

# 🗓️ **Exemplo de Consulta com Datas**

### 🔹 Buscar **vendas após o ano de 2020**
```sql
SELECT id_venda, data_venda, valor 
FROM vendas 
WHERE data_venda > '2020-12-31';
```

### 🔹 Vendas a partir de **2022 (inclusive)**
```sql
SELECT * 
FROM vendas 
WHERE data_venda >= '2022-01-01';
```

### 🔹 Vendas entre **2021 e 2023**
```sql
SELECT * 
FROM vendas 
WHERE data_venda BETWEEN '2021-01-01' AND '2023-12-31';
```

### 🔹 Se a data estiver armazenada apenas como **ano**
```sql
SELECT * 
FROM vendas 
WHERE ano_venda > 2020;
```

---

# ✅ **Conclusão**

Este guia fornece exemplos práticos e claros para iniciar o uso do SQL em bancos de dados relacionais. 🚀 Se precisar de mais detalhes, explore mais operadores e funções SQL para aprimorar suas consultas!

---

> **Dica:** Use este guia como referência rápida sempre que precisar criar ou ajustar consultas SQL! 📅
