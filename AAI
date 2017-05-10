CREATE TABLE loja
(
cod_loja smallint NOL NULL PRIMARY KEY,
nom_loja varchar(100) NOT NULL
)

CREATE TABLE ficha_venda
(
num_venda smallint NOT NULL PRIMARY KEY,
cod_loja smallint NOT NULL FOREIGN KEY REFERENCES loja (cod_loja),
nom_loja varchar(100) NOT NULL FOREIGN KEY REFERENCES loja (nom_loja),
data datetime NOT NULL DEFAULT getdate()
)

CREATE TABLE vendedor
(
cod_vendedor int NOT NULL PRIMARY KEY,
nome_vendedor varchar(100) NOT NULL
)

CREATE TABLE cidade
(
cod_cidade int NOT NULL PRIMARY KEY,
nom_cidade varchar(50) NOT NULL 
)

CREATE TABLE uf
(
sigla_uf varchar(2) NOT NULL PRIMARY KEY,
nom_uf varchar(50) NOT NULL
)

CREATE TABLE cliente
(
cpf varchar(11) NOT NULL PRIMARY KEY,
nom_cliente(100) NOT NULL,
endereço varchar(50) NOT NULL,
bairro varchar(50) NOT NULL, 
cep varchar(8) NOT NULL,
cod_cidade int NOT NULL FOREIGN KEY REFERENCES cidade (cod_cidade),
nom_cidade varchar(50) NOT NULL FOREIGN KEY REFERENCES cidade (nom_cidade)
sigla_uf varchar(2) NOT NULL FOREIGN KEY REFERENCES uf (sigla_uf),
nom_uf varchar(50) NOT NULL FOREIGN KEY REFERENCES uf (nom_uf)
)

CREATE TABLE marca
(
cod_marca smallint NOT NULL PRIMARY KEY,
nom_marca varchar(20) NOT NULL
)

CREATE TABLE modelo
(
cod_modelo smallint NOT NULL PRIMARY KEY,
nom_modelo varchar(20) NOT NULL
)

CREATE TABLE opcionais
(
cod_op smallint NOT NULL PRIMARY KEY,
nom_op varchar(50) NOT NULL
)

CREATE TABLE veiculo
(
placa varchar(7) NOT NULL PRIMARY KEY,
ano_fabricacao smallint NOT NULL,
chassi varchar(22) NOT NULL UNIQUE,
cod_marca smallint NOT NULL FOREIGN KEY REFERENCES marca (cod_marca),
nom_marca varchar(20) NOT NULL FOREIGN KEY REFERENCES marca (nom_marca),
cod_modelo smallint NOT NULL FOREIGN KEY REFERENCES modelo (cod_modelo),
nom_modelo varchar(20) NOT NULL FOREIGN KEY REFERENCES modelo (nom_modelo),
cod_op smallint NOT NULL FOREIGN KEY REFERENCES opcionais (cod_op),
nom_op varchar(50) NOT NULL FOREIGN KEY REFERENCES opcionais (nom_op),
valor_tab numeric(7,2) NOT NULL,
desconto numeric(2,2) NOT NULL,
valor_final numeric(7,2) NOT NULL,
)

CREATE TABLE item_pag
(
cod_item smallint NOT NULL PRIMARY KEY,
nom_item char(100) NOT NULL
)

CREATE TABLE forma_pagamento
(
cod_forma smallint NOT NULL PRIMARY KEY,
nom_forma varchar(50) NOT NULL
)

CREATE TABLE pagamento
(
seq smallint NOT NULL PRIMARY KEY,
item -> cod_item ||'-'||nom_item,
form_pag -> cod_forma||'-'||nom_forma,
valor_forma numeric (7,2) NOT NULL,
qtd_parcelas smallint NOT NULL,
valor_parcela numeric(5,2) NOT NULL,
valor_final numeric(7,2) NOT NULL
)
 

