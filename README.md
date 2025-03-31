# 2i-crud

# Gerenciamento de Produtos em Base de Dados

Este projeto tem como objetivo fornecer uma estrutura para o gerenciamento de produtos em uma base de dados. O foco é no armazenamento, consulta e manipulação de dados de produtos, como preço edescrição.

## Índice

- [Sobre](#sobre)
- [Objetivo](#objetivo)
- [Estrutura do Banco de Dados](#estrutura-do-banco-de-dados)
- [Comandos SQL](#comandos-sql)
- [Tecnologias](#tecnologias)
- [Como Usar](#como-usar)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Sobre

Este projeto fornece uma estrutura simples para o **gerenciamento de produtos em um banco de dados relacional**. Ele pode ser usado como base para sistemas de controle de inventário, catálogos de produtos, ou qualquer aplicação que precise gerenciar dados de produtos em uma base de dados.

## Objetivo

O objetivo principal deste projeto é criar uma estrutura de banco de dados para armazenar informações de produtos e permitir operações como:

- Cadastro de novos produtos.
- Atualização de informações de produtos existentes.
- Exclusão de produtos.
- Consultas detalhadas sobre os produtos armazenados.

Este projeto não inclui uma interface gráfica ou aplicação web. Seu foco é no design do banco de dados e nas operações de SQL.

## Estrutura do Banco de Dados

O banco de dados está estruturado com a seguinte tabela de **produtos**:

```sql
CREATE TABLE produtos (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(255) NOT NULL,
  descricao TEXT,
  preco DECIMAL(10, 2) NOT NULL,
  quantidade_estoque INT NOT NULL,
  categoria VARCHAR(100),
  data_criacao TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
