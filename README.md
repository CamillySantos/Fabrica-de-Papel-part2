# Módulo 2 - Fábrica de Papel - parte 2
O registro das atividades do custo que estou fazendo sobre SQL está relacionado a uma fábrica de papel onde estou aprendendo sobre diferentes formas de fazer pesquisas em Bancos de dados.

## Material de aula

O material disponibilizado pelo curso para entendermos sobre Banco de Dados e começar as pesquisas conforme as aulas.

[Fabrica de papel](https://github.com/CamillySantos/Fabrica-de-Papel/blob/main/PostgreSQL.sql)

## 1. Introdução ao JOIN

1. Tente extrair todos os dados da tabela de `accounts` (contas) e todos os dados da tabela de `orders` (pedidos_.

```
SELECT orders.*, accounts.*
FROM accounts
JOIN orders
ON orders.account_id = accounts.id;
```

2. Tente extrair `standard_qty` , `gloss_qty` e `poster_qty` da tabela de `orders` (pedidos) e o site e o `Primary_poc` da tabela de `accounts` (contas).

```
SELECT orders.standard_qty, orders.gloss_qty, 
          orders.poster_qty,  accounts.website, 
          accounts.primary_poc
FROM orders
JOIN accounts
ON orders.account_id = accounts.id
```

## 2. Prática 

![image](https://github.com/CamillySantos/Fabrica-de-Papel-part2/assets/105953740/5c009aa4-0296-41fd-b641-a348e35c86ed)

1. Usando o diagrama para ajudá-la. Se quiséssemos unir as tabelas `sales_reps` e `region`, como você faria isso?

```
ON region.id = sales_reps.region_id
```
