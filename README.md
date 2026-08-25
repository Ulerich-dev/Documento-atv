# Documento-atv

 Requisitos Funcionais 
 Mapear as pessoas e processos atuais
Identifique quem vai usar o sistema no dia a dia, quem vai gerenciar e quem vai extrair relatórios. Entenda como o trabalho é feito hoje e onde estão os erros ou atrasos.

Coletar as informações
Converse com os futuros usuários por meio de entrevistas simples, observe o trabalho deles na prática e analise as planilhas ou papéis usados atualmente.

Transformar problemas em ações do sistema
Traduza as dificuldades relatadas em tarefas que o software precisa executar:

Se o problema for alugar o mesmo item duas vezes, o requisito é verificar a disponibilidade em tempo real e bloquear datas duplicadas.

Se o problema for o somiço de itens, o requisito é registrar o usuário, data e hora de cada movimentação.

Se o problema for a falta de estoque, o requisito é emitir alertas quando a quantidade atingir um nível mínimo.

Organizar em frases diretas
Escreva cada funcionalidade de forma clara, no formato:
"O sistema deve [ação do sistema] para [finalidade do usuário]."

Validar e priorizar
Mostre a lista de funcionalidades para quem vai usar o sistema para confirmar se tudo está correto. Em seguida, separi o que é indispensável para o sistema funcionar do que pode ser desenvolvido em etapas futuras.

create database Rental_db;

create table Usuario(
id serial primary key,
nome varchar(30) not null,
login int not null,
senha varchar(8) not null 
);

create type tipo_enum as enum('Entrada', 'Saída');

create table Movimentacao(
id serial primary key,
tipo tipo_enum not null,
data date not null,
quantidade int not null,
equipamento_id int not null,
foreign key (equipamento_id) references equipamento(id),
usuario_id int not null,
foreign key (usuario_id) references usuario(id)
);

create table equipamento( 
id serial primary key,
nome varchar(30) not null,
marca varchar(30) not null,
modelo varchar(30) not null,
quantidade int not null,
estoque_minimo int not null,
categoria_id int not null,
foreign key (categoria_id) references categoria(id)
);
	
create table categoria(
id serial primary key,
nome varchar(30) not null
);	

alter table usuario 
alter column login type varchar(50);


insert into usuario (nome, login, senha)
values ('julia', 'juliademachado@', '1234'),
('maria', 'mariaclre@','12345'),
('lara','flordeliz@','123456');

#fazer o insert do equipamento primeiro antes de fazer o insert da movimentação

insert into equipamento (nome, marca, modelo, quantidade, estoque_minimo, categoria_id )
values('Notebook', 'Dell', 'Inspiron 15', 10, 1, 1),
('Monitor', 'Samsung', 'T350', 15, 2, 2),
('Teclado', 'Logitech', 'K120', 20, 3, 3);

insert into Movimentacao (tipo, data, quantidade, equipamento_id, usuario_id)
values('Entrada','2024-08-01', '12', 4, 1),
('Saída','2025-07-02','13', 5, 2),
('Saída', '2026-06-03','14', 6, 3);

INSERT INTO categoria (nome)
VALUES
('Informática'),
('Periféricos'),
('Eletrônicos');

