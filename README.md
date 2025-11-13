-- =========================================

-- Banco de dados para Livraria / Pequeno comércio

-- =========================================

-- Criar tabela Produtos

CREATE TABLE IF NOT EXISTS Produtos (

id_produto INTEGER PRIMARY KEY AUTOINCREMENT,

nome TEXT NOT NULL,

preco REAL NOT NULL,

estoque INTEGER NOT NULL
);

-- Criar tabela Pedidos

CREATE TABLE IF NOT EXISTS Pedidos (

id_pedido INTEGER PRIMARY KEY AUTOINCREMENT,

id_produto INTEGER NOT NULL,

quantidade INTEGER NOT NULL,

data_pedido TEXT NOT NULL,

FOREIGN KEY (id_produto) REFERENCES Produtos(id_produto)
);

-- Inserir dados na tabela Produtos

INSERT INTO Produtos (nome, preco, estoque) VALUES ('Livro: Introdução ao SQL', 59.90, 10);

INSERT INTO Produtos (nome, preco, estoque) VALUES ('Livro: Programação em Python', 89.90, 5);

INSERT INTO Produtos (nome, preco, estoque) VALUES ('Livro: Fundamentos de Java', 75.50, 8);

-- Inserir dados na tabela Pedidos

INSERT INTO Pedidos (id_produto, quantidade, data_pedido) VALUES (1, 2, '2025-09-01');

INSERT INTO Pedidos (id_produto, quantidade, data_pedido) VALUES (2, 1, '2025-09-01');

INSERT INTO Pedidos (id_produto, quantidade, data_pedido) VALUES (3, 3, '2025-09-01');
