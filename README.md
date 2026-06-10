# Banco-de-dados-

CREATE DATABASE biblioteca;
USE biblioteca;


CREATE TABLE autores (
    id_autor INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL
);


CREATE TABLE editoras (
    id_editora INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL
);


CREATE TABLE clientes (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    telefone VARCHAR(20)
);


create table livros(
    id_livro int auto_increment primary key,
    titulo varchar(150) not null,
    id_editora int,
    id_autor int,
    foreign key(id_editora) references editoras(id_editora),
    foreign key(id_autor) references autores(id_autor)
);

create table estoque(
id_estoque int auto_increment primary key,
quantidade int not null,
id_livro int,
foreign key(id_livro) references livros(id_livro)
);

insert into autores(nome) values('Machado de Assis');
insert into editoras(nome) values('Editora rocca');
insert into clientes (nome, telefone) values('Anna Silva','9999-1111');

insert into 
