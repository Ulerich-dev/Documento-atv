# Documento-atv

 ### 1. Entenda o problema

Leia o enunciado e pergunte:

* Qual problema o sistema pretende resolver?
* Quem vai utilizar o sistema?
* Quais tarefas essas pessoas realizam atualmente?

No seu caso, os problemas são:

* Controle feito em planilhas.
* Equipamentos alugados para dois clientes na mesma data.
* Equipamentos retornam danificados sem registro.
* Não há rastreabilidade das movimentações.
* Falta de controle do estoque.

Esses problemas já indicam funcionalidades que o sistema precisa ter.

---

### 2. Identifique os verbos do texto

Em muitos enunciados, os requisitos aparecem como ações.

Exemplo do seu texto:

* **Cadastrar** equipamentos
* **Consultar** equipamentos
* **Atualizar** informações
* **Excluir** equipamentos
* **Registrar** entradas
* **Registrar** saídas
* **Configurar** estoque mínimo
* **Gerar** alertas
* **Registrar** movimentações
* **Consultar** histórico

Cada verbo normalmente corresponde a um requisito funcional.

---

### 3. Pense nas necessidades do usuário

Pergunte:

> "O que o usuário precisa conseguir fazer no sistema?"

Por exemplo:

O usuário precisa:

* cadastrar um equipamento;
* editar um equipamento;
* excluir um equipamento;
* registrar uma locação;
* registrar uma devolução;
* saber quantos equipamentos existem;
* consultar o histórico;
* receber aviso de estoque baixo.

Cada uma dessas respostas vira um requisito funcional.

---

### 4. Transforme as necessidades em requisitos

Use uma estrutura simples:

> **O sistema deve permitir...**

Exemplos:

* O sistema deve permitir cadastrar equipamentos.
* O sistema deve permitir consultar equipamentos.
* O sistema deve permitir alterar informações dos equipamentos.
* O sistema deve permitir registrar entradas no estoque.
* O sistema deve permitir registrar saídas para locação.
* O sistema deve gerar alertas quando o estoque atingir a quantidade mínima.

---

### 5. Verifique se o requisito é uma funcionalidade

Faça a pergunta:

> **Isso é algo que o sistema faz?**

Se a resposta for **sim**, provavelmente é um requisito funcional.

Exemplos:

✔ O sistema deve emitir relatório. *(funcional)*

✔ O sistema deve permitir cadastrar usuários. *(funcional)*

✔ O sistema deve registrar quem realizou uma movimentação. *(funcional)*

Já estes são requisitos **não funcionais**:

* O sistema deve responder em até 2 segundos.
* O sistema deve funcionar 24 horas por dia.
* O sistema deve possuir interface intuitiva.
* O sistema deve utilizar banco de dados MySQL.

---

## Aplicando ao seu exercício

Trecho do enunciado:

> "Toda movimentação deverá registrar usuário responsável, data, tipo da movimentação e quantidade."

Pergunta:

**O que o sistema precisa fazer?**

Resposta:

* Registrar movimentações.
* Registrar o usuário responsável.
* Registrar a data.
* Registrar o tipo da movimentação.
* Registrar a quantidade.

Isso pode ser representado por um ou mais requisitos funcionais, por exemplo:

* **RF09** – O sistema deve registrar todas as movimentações de entrada e saída de equipamentos.
* **RF10** – O sistema deve armazenar o usuário responsável, data, tipo e quantidade de cada movimentação.

---

### Dica prática

Uma técnica simples para identificar requisitos funcionais é destacar no enunciado todas as ações (verbos). Em seguida, transforme cada uma em uma frase iniciada por **"O sistema deve..."**. Na maioria dos trabalhos acadêmicos de Engenharia de Software e Análise de Sistemas, esse método permite identificar praticamente todos os requisitos funcionais presentes no problema.



Com base na contextualização e no desafio apresentados, segue uma lista de **Requisitos Funcionais (RF)** com suas respectivas descrições.

| Código   | Requisito Funcional                   | Descrição                                                                                                                                                                                                       |
| -------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RF01** | Cadastrar equipamentos                | O sistema deve permitir o cadastro de novos equipamentos, informando dados como nome, marca, modelo, categoria, potência, material, peso, dimensões, cor, quantidade disponível e quantidade mínima em estoque. |
| **RF02** | Consultar equipamentos                | O sistema deve permitir a consulta dos equipamentos cadastrados, exibindo todas as suas informações e a quantidade disponível em estoque.                                                                       |
| **RF03** | Pesquisar equipamentos                | O sistema deve permitir a pesquisa de equipamentos por nome, categoria, marca, modelo ou outros critérios de busca.                                                                                             |
| **RF04** | Atualizar cadastro de equipamentos    | O sistema deve permitir a alteração das informações dos equipamentos já cadastrados.                                                                                                                            |
| **RF05** | Excluir equipamentos                  | O sistema deve permitir a exclusão de equipamentos cadastrados, desde que não existam movimentações vinculadas ou conforme as regras definidas pelo sistema.                                                    |
| **RF06** | Registrar entrada de equipamentos     | O sistema deve permitir o registro da entrada de equipamentos no estoque, atualizando automaticamente a quantidade disponível.                                                                                  |
| **RF07** | Registrar saída de equipamentos       | O sistema deve permitir o registro da saída de equipamentos para locação, reduzindo automaticamente a quantidade disponível em estoque.                                                                         |
| **RF08** | Controlar disponibilidade             | O sistema deve impedir que sejam registradas saídas quando a quantidade solicitada for maior que a disponível, evitando dupla locação dos mesmos equipamentos.                                                  |
| **RF09** | Registrar histórico de movimentações  | O sistema deve armazenar todas as movimentações realizadas, registrando usuário responsável, data, tipo da movimentação (entrada ou saída), equipamento e quantidade movimentada.                               |
| **RF10** | Consultar histórico de movimentações  | O sistema deve permitir a consulta do histórico completo de movimentações dos equipamentos para fins de rastreabilidade.                                                                                        |
| **RF11** | Configurar estoque mínimo             | O sistema deve permitir definir uma quantidade mínima de estoque para cada equipamento cadastrado.                                                                                                              |
| **RF12** | Emitir alerta de estoque mínimo       | O sistema deve gerar um alerta quando a quantidade disponível de um equipamento atingir ou ficar abaixo da quantidade mínima configurada.                                                                       |
| **RF13** | Controlar usuários responsáveis       | O sistema deve identificar o usuário responsável por cada movimentação realizada no sistema.                                                                                                                    |
| **RF14** | Registrar devolução de equipamentos   | O sistema deve permitir registrar o retorno dos equipamentos após a locação, atualizando o estoque disponível.                                                                                                  |
| **RF15** | Registrar avarias                     | O sistema deve permitir registrar quando um equipamento retornar danificado, armazenando informações sobre a ocorrência para controle e manutenção.                                                             |
| **RF16** | Visualizar equipamentos indisponíveis | O sistema deve informar quando um equipamento estiver indisponível para locação por falta de estoque ou por estar danificado.                                                                                   |
| **RF17** | Gerar relatórios de estoque           | O sistema deve permitir a emissão de relatórios contendo os equipamentos cadastrados, quantidades disponíveis e situação do estoque.                                                                            |
| **RF18** | Gerar relatórios de movimentações     | O sistema deve permitir emitir relatórios das entradas, saídas e devoluções realizadas em determinado período.                                                                                                  |

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

